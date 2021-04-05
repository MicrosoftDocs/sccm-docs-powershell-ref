---
description: Create a detection method clause for a registry key.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
schema: 2.0.0
title: New-CMDetectionClauseRegistryKey
---

# New-CMDetectionClauseRegistryKey

## SYNOPSIS

Create a detection method clause for a registry key.

## SYNTAX

```
New-CMDetectionClauseRegistryKey [-Existence] -Hive <RegistryRootKey> [-Is64Bit] -KeyName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a clause in a detection method on an application. This clause is a rule for a registry key to indicate the presence of an application.

To detect a registry value instead of a key, use the [New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md) cmdlet.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this detection clause object to either the **AddDetectionClause** or **RemoveDetectionClause** parameters.

To group detection clauses, use the **GroupDetectionClauses** parameter on the deployment type cmdlets.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create multiple clauses for an MSI app deployment type

This example creates two file clauses and one registry clause, and then uses them to add an MSI deployment type to an app.

```powershell
$cla1=New-CMDetectionClauseFile -FileName "filetest" -PropertyType Size -ExpectedValue 123 -ExpressionOperator IsEquals -Path "C:\" -Value -Is64Bit
$cla2=New-CMDetectionClauseFile -FileName "foldertest" -PropertyType DateCreated -ExpectedValue (Get-Date) -ExpressionOperator LessThan -Path "C:\" -Value
$cla3=New-CMDetectionClauseRegistryKey -Hive ClassesRoot -KeyName "aaa"
$logic1=$cla1.Setting.LogicalName
$logic2=$cla2.Setting.LogicalName
$logic3=$cla3.Setting.LogicalName

Add-CMMsiDeploymentType -AddDetectionClause $cla1,$cla2,$cla3 -ApplicationName "app" -DeploymentTypeName "dt" -InstallCommand "mycommand" -ContentLocation "\\server\sources\Orca.msi" -GroupDetectionClauses $logic1,$logic2 -DetectionClauseConnector {LogicalName=$logic2;Connector="or"},{LogicalName=$logic3;Connector="or"}
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

This parameter is implied and optional.

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

Specify the registry hive where the key exists. Use the **KeyName** parameter to specify the key name.

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

Specify the name of the registry key that must exist to indicate the presence of this application. Use the **Hive** parameter to specify the registry hive where this key should exist.

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

[New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)

[New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)
