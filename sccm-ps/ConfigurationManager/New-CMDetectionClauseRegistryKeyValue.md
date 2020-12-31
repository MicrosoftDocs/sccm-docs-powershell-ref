---
description: Create a detection method clause for a registry key value.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/26/2020
schema: 2.0.0
title: New-CMDetectionClauseRegistryKeyValue
---

# New-CMDetectionClauseRegistryKeyValue

## SYNOPSIS

Create a detection method clause for a registry key value.

## SYNTAX

### Value
```
New-CMDetectionClauseRegistryKeyValue -ExpressionOperator <RegistryValueRuleExpressionOperator>
 -Hive <RegistryRootKey> [-Is64Bit] -KeyName <String> -PropertyType <SettingDataType> -ValueName <String>
 -ExpectedValue <String[]> [-Value] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseRegistryKeyValue -Hive <RegistryRootKey> [-Is64Bit] -KeyName <String>
 -PropertyType <SettingDataType> -ValueName <String> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a clause in a detection method on an application. This clause is a rule for a registry key value to indicate the presence of an application.

To detect the existence of a registry key instead of a value, use the [New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md) cmdlet.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this detection clause object to either the **AddDetectionClause** or **RemoveDetectionClause** parameters.

To group detection clauses, use the **GroupDetectionClauses** parameter on the deployment type cmdlets.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Detect the existence of a registry value

This example creates a clause to detect the existence of the Git for Windows current version value.

```powershell
$regClause = New-CMDetectionClauseRegistryKeyValue -Hive LocalMachine -KeyName "SOFTWARE\GitForWindows" -PropertyType String -ValueName "CurrentVersion" -Existence

Set-CMMsiDeploymentType -ApplicationName "Git for Windows" -DeploymentTypeName "Install" -AddDetectionClause $regClause
```

### Example 2: Compare a version value in the registry

This example creates a clause to compare the version of Microsoft 365 in the registry to be greater than or equal to `16.0.10730.20304`.

```powershell
$clause = New-CMDetectionClauseRegistryKeyValue -Hive LocalMachine -KeyName 'Software\Microsoft\Office\ClickToRun\Configuration' -PropertyType Version -ValueName 'VersionToReport' -Value -ExpectedValue '16.0.10730.20304' -ExpressionOperator GreaterEquals

Set-CMMsiDeploymentType -ApplicationName "Microsoft 365" -DeploymentTypeName "Install" -AddDetectionClause $clause
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

When you add this parameter, the registry key value must exist on the target system to indicate presence of this application.

Instead of just existence, to evaluate a rule for the data of this registry key value, use the **Value** parameter.

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

When you add the **Value** parameter, use **ExpectedValue** with **PropertyType** and **ExpressionOperator**. When you use these parameters, the registry key value must satisfy the rule to indicate the presence of this application. This **ExpectedValue** parameter specifies the value to compare against the registry key value.

The value to compare depends upon the specified **PropertyType**.

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

When you add the **Value** parameter, use **ExpressionOperator** with **PropertyType** and **ExpectedValue**. When you use these parameters, the registry key value must satisfy the rule to indicate the presence of this application. This **ExpressionOperator** parameter specifies the operator to compare the registry key value with the expected value.

```yaml
Type: RegistryValueRuleExpressionOperator
Parameter Sets: Value
Aliases:
Accepted values: IsEquals, NotEquals, GreaterThan, LessThan, Between, GreaterEquals, LessEquals, OneOf, NoneOf, BeginsWith, NotBeginsWith, EndsWith, NotEndsWith, Contains, NotContains

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

Specify the registry hive where the key exists. Use the **KeyName** parameter to specify the key name. Use the **ValueName** parameter to specify the registry key value.

For example, the following PowerShell command translates to the following parameter values:

```powershell
Get-ItemProperty 'HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion' | Select-Object CurrentVersion
```

|Parameter|Value|
|---------|---------|
|**Hive**|`LocalMachine`|
|**KeyName**|`'SOFTWARE\Microsoft\Windows NT\CurrentVersion'`|
|**ValueName**|`CurrentVersion`|

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

Add this parameter to indicate that this registry key is associated with a 32-bit application on 64-bit systems.

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

Specify the name of the registry key that must exist to indicate the presence of this application. Use the **Hive** parameter to specify the registry hive where this key should exist. Use the **ValueName** parameter to specify the registry key value.

For example, the following PowerShell command translates to the following parameter values:

```powershell
Get-ItemProperty 'HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion' | Select-Object CurrentVersion
```

|Parameter|Value|
|---------|---------|
|**Hive**|`LocalMachine`|
|**KeyName**|`'SOFTWARE\Microsoft\Windows NT\CurrentVersion'`|
|**ValueName**|`CurrentVersion`|

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

When you add the **Value** parameter, use **PropertyType** with **ExpressionOperator** and **ExpectedValue**. When you use these parameters, the registry key value must satisfy the rule to indicate the presence of this application. This **PropertyType** parameter specifies the data type of the registry key value.

For example, you set this parameter to `Version`, set **ExpressionOperator** to `IsEquals`, and **ExpectedValue** to `1.48.1.0`. The rule then checks the specified registry key value to have that same version.

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

When you add the **Value** parameter, the registry key value must satisfy the rule to indicate the presence of this application. Use this parameter with the following parameters: **ExpectedValue**, **ExpressionOperator**, and **PropertyType**.

Instead of evaluating a rule, to just check that the registry key value exists, use the **Existence** parameter.

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

Specify the registry key value that indicates the presence of the application. Use the **Hive** parameter to specify the registry hive, and **KeyName** to specify the registry key.

For example, the following PowerShell command translates to the following parameter values:

```powershell
Get-ItemProperty 'HKLM:\SOFTWARE\Microsoft\Windows NT\CurrentVersion' | Select-Object CurrentVersion
```

|Parameter|Value|
|---------|---------|
|**Hive**|`LocalMachine`|
|**KeyName**|`'SOFTWARE\Microsoft\Windows NT\CurrentVersion'`|
|**ValueName**|`CurrentVersion`|

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

[New-CMDetectionClauseDirectory](New-CMDetectionClauseDirectory.md)

[New-CMDetectionClauseFile](New-CMDetectionClauseFile.md)

[New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)

[New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)
