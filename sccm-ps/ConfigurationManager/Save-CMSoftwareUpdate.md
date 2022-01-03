---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
schema: 2.0.0
title: Save-CMSoftwareUpdate
---

# Save-CMSoftwareUpdate

## SYNOPSIS

Save software updates to update groups and packages.

## SYNTAX

### SearchByNameMandatory (Default)
```
Save-CMSoftwareUpdate -DeploymentPackageName <String> [-Location <String>] [-RetryCount <UInt32>]
 [-RetryDelaySec <UInt32>] [-SoftwareUpdateLanguage <String[]>] -SoftwareUpdateName <String[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_UpdateGroup
```
Save-CMSoftwareUpdate -DeploymentPackageName <String> [-Location <String>] [-RetryCount <UInt32>]
 [-RetryDelaySec <UInt32>] -SoftwareUpdateGroupId <String[]> [-SoftwareUpdateLanguage <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_UpdateGroup
```
Save-CMSoftwareUpdate -DeploymentPackageName <String> [-Location <String>] [-RetryCount <UInt32>]
 [-RetryDelaySec <UInt32>] -SoftwareUpdateGroupName <String[]> [-SoftwareUpdateLanguage <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_UpdateGroup
```
Save-CMSoftwareUpdate -DeploymentPackageName <String> [-Location <String>] [-RetryCount <UInt32>]
 [-RetryDelaySec <UInt32>] -SoftwareUpdateGroup <IResultObject> [-SoftwareUpdateLanguage <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Save-CMSoftwareUpdate -DeploymentPackageName <String> [-Location <String>] [-RetryCount <UInt32>]
 [-RetryDelaySec <UInt32>] -SoftwareUpdateId <String[]> [-SoftwareUpdateLanguage <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Save-CMSoftwareUpdate -DeploymentPackageName <String> [-Location <String>] [-RetryCount <UInt32>]
 [-RetryDelaySec <UInt32>] -SoftwareUpdate <IResultObject> [-SoftwareUpdateLanguage <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to save one or more software updates to update groups and deployment packages.

You can specify one or more software updates associated with deployment packages.
You can also specify the download source location of updates and the language of the software updates.
Languages determine which summary details a software update synchronizes and the file languages to be downloaded for software updates.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Save a software update and add a language to it

This command saves the software update named **Cumulative Update for Windows 10 (KB3095020)** for the deployment package named **Package01**. It also adds **English** to its array of languages.

```powershell
Save-CMSoftwareUpdate -SoftwareUpdateName "Cumulative Update for Windows 10 (KB3095020)" -DeploymentPackageName "Package01" -SoftwareUpdateLanguage "English"
```

### Example 2: Save a software update from a software update group

This command gets the software update group object named **TestSUgroup10** and uses the pipeline operator to pass the object to **Save-CMSoftwareUpdate**, which saves the software update with the package name **Package01**.

```powershell
Get-CMSoftwareUpdateGroup -Name "TestSUgroup10" | Save-CMSoftwareUpdate -DeploymentPackageName "Package01"
```

### Example 3: Save a software update from a software update group and specify a source location to download from

This command gets the software update group object named **TestSUgroup10** and uses the pipeline operator to pass the object to **Save-CMSoftwareUpdate**, which saves the software update from the file share **Updates** on **Server01** with the package name **Package01**.

```powershell
Get-CMSoftwareUpdateGroup -Name "TestSUgroup10" Save-CMSoftwareUpdate -Location "\\Server01\Updates" -DeploymentPackageName "Package01"
```

## PARAMETERS

### -DeploymentPackageName

Specify the name of a deployment package.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Location

Specify a download source location for software updates.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetryCount

Specify an integer value for the number of times to retry downloading the update.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetryDelaySec

Specify an integer value for the number of seconds to wait before retrying.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdate

Specify a software update object to save. To get this object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroup

Specify a software update group object. To get this object, use the [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_UpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId

Specify an array of IDs of software update groups.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_UpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName

Specify an array of names of software update groups.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_UpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId

Specify an array of IDs of software updates.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateLanguage

Specify an array of software update languages.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName

Specify an array of software update names.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdate](Set-CMSoftwareUpdate.md)

[Sync-CMSoftwareUpdate](Sync-CMSoftwareUpdate.md)

[Remove-CMSoftwareUpdateFromPackage](Remove-CMSoftwareUpdateFromPackage.md)
