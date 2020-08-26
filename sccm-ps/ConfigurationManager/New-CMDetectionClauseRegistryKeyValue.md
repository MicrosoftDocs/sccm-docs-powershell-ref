---
description: Create a detection clause for a registry key in a configuration item or app detection method.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/26/2020
schema: 2.0.0
title: New-CMDetectionClauseRegistryKeyValue
---

# New-CMDetectionClauseRegistryKeyValue

## SYNOPSIS

Create a detection clause for a registry key in a configuration item or app detection method.

## SYNTAX

### Value
```
New-CMDetectionClauseRegistryKeyValue -ExpressionOperator <RuleExpressionOperator> -Hive <RegistryRootKey>
 [-Is64Bit] -KeyName <String> -PropertyType <SettingDataType> -ValueName <String> -ExpectedValue <String[]>
 [-Value] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseRegistryKeyValue -Hive <RegistryRootKey> [-Is64Bit] -KeyName <String>
 -PropertyType <SettingDataType> -ValueName <String> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a detection clause for a registry key in a configuration item or app detection method.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Detect the existence of a registry value

This example creates a clause to detect the existence of the Configuration Manager client logging registry key, and saves it in a variable **$regClause**.

```powershell
$regClause = New-CMDetectionClauseRegistryKeyValue -Hive LocalMachine -KeyName "SOFTWARE\Microsoft\CCM\Logging\@Global" -Existence -PropertyType String -ValueName "LogEnabled"
```

### Example 2: Create multiple clauses for an MSI app deployment type

This example creates two file clauses and one registry clause, and then uses them to add an MSI deployment type to an app.

```powershell
$cla1=New-CMDetectionClauseFile -FileName "filetest" -PropertyType Size -ExpectedValue 123 -ExpressionOperator IsEquals -Path "C:\" -Value -Is64Bit
$cla2=New-CMDetectionClauseFile -FileName "foldertest" -PropertyType DateCreated -ExpectedValue (Get-Date) -ExpressionOperator LessThan -Path "C:\" -Value
$cla3=New-CMDetectionClauseRegistryKey -Hive ClassesRoot -KeyName "aaa"
$logic1=$cla1.Setting.LogicalName
$logic2=$cla2.Setting.LogicalName
$logic3=$cla3.Setting.LogicalName
Add-CMMsiDeploymentType -AddDetectionClause $cla1,$cla2,$cla3 -ApplicationName "app" -DeploymentTypeName "dt" -InstallCommand "mycommand" -ContentLocation “\\server\sources\Orca.msi” -GroupDetectionClauses $logic1,$logic2 -DetectionClauseConnector {LogicalName=$logic2;Connector="or"},{LogicalName=$logic3;Connector="or"}
```

## PARAMETERS

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Existence

Add this parameter to create an existential rule type. For the setting to comply, the registry key value exists on the client.

Alternatively, use the **-Value** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: Existence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedValue

Specify an array of strings to compare the value. The value to compare depends upon the specified **PropertyType**.

```yaml
Type: String[]
Parameter Sets: Value
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator

For the **ExpectedValue**, specify the comparison operator.

```yaml
Type: RuleExpressionOperator
Parameter Sets: Value
Aliases:
Accepted values: IsEquals, NotEquals, GreaterThan, GreaterEquals, LessThan, LessEquals, Between, OneOf, NoneOf, BeginsWith, EndsWith, NotEndsWith, Contains, NotContains

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Hive

Specify which registry hive has the key value to assess for compliance on clients. For the proper format, see the **Accepted values**.

```yaml
Type: RegistryRootKey
Parameter Sets: (All)
Aliases: RegistryHive
Accepted values: ClassesRoot, CurrentConfig, CurrentUser, LocalMachine, Users

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit

Add this parameter to specify that this registry key value is associated with a 64-bit application.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyName

Specify the registry key path that contains the value to assess for compliance on clients. Use the **-Hive** parameter to specify the registry hive, and **-ValueName** to specify the registry key value.

For example, `SOFTWARE\Microsoft\CCM\Logging\@Global`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyType

Specify the property to compare and assess for compliance. Use the **-ExpectedValue** parameter to specify the value of this property, and the **-ExpressionOperator** parameter to specify the means of comparison.

```yaml
Type: SettingDataType
Parameter Sets: (All)
Aliases:
Accepted values: Version, Integer, String

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

Add this parameter to check compliance of a property value. Alternatively, use the **-Existence** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: Value
Aliases: ValueRule

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueName

Specify the registry key value to assess for compliance on clients. Use the **-Hive** parameter to specify the registry hive, and **-ValueName** to specify the registry key value.

For example, `LogEnabled`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RegistryValueName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
