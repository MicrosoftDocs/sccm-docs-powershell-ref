---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
online version:
schema: 2.0.0
---

# Remove-CMSoftwareUpdateFromPackage

## SYNOPSIS

Remove an update from a software update package.

## SYNTAX

### ById_Id (Default)
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateId <String[]> -SoftwareUpdatePackageId <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObject_Id
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdate <IResultObject[]> -SoftwareUpdatePackageId <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObject_Name
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdate <IResultObject[]> -SoftwareUpdatePackageName <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObject_Object
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdate <IResultObject[]> -SoftwareUpdatePackage <IResultObject>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById_Name
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateId <String[]> -SoftwareUpdatePackageName <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById_Object
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateId <String[]> -SoftwareUpdatePackage <IResultObject>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName_Id
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateName <String[]> -SoftwareUpdatePackageId <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName_Name
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateName <String[]> -SoftwareUpdatePackageName <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName_Object
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateName <String[]> -SoftwareUpdatePackage <IResultObject>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove the specified software update from a package.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove an update and refresh the content

This example first gets the ID of a software update.
It then gets a software update package by its ID.
The last command removes the update from the package. It refreshes the content on the distribution point, and doesn't prompt for confirmation.

```powershell
$SU0 = "Bing Bar 7.1 (KB2673770)"
$SU0_ID = ( Get-CMSoftwareUpdate -Name $SU0 -Fast ).CI_ID

$suppkg1 = Get-CMSoftwareUpdateDeploymentPackage -Id "XYZ0000C"

Remove-CMSoftwareUpdateFromPackage -SoftwareUpdatePackageId $suppkg1.PackageID -SoftwareUpdateId $SU0_ID -RefreshDistributionPoint -Force
```

### Example 2: Remove two updates but don't refresh the content

This example first defines the names of two software updates.
It then gets a software update package by its ID.
The last command removes both software updates from the package. Since this command doesn't include the **Force** parameter, it prompts for confirmation. Since it doesn't include the **RefreshDistributionPoint** parameter, you need to manually update the content on distribution points.

```powershell
$SU1 = "Bing Bar 7.1 (KB2673771)"
$SU2 = "Bing Bar 7.1 (KB2673772)"

$suppkg1 = Get-CMSoftwareUpdateDeploymentPackage -Id "XYZ0000C"

Remove-CMSoftwareUpdateFromPackage -SoftwareUpdatePackage $suppkg1 -SoftwareUpdateName ($SU1, $SU2)
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

### -Force

Add this parameter to run the command without asking for confirmation.

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

### -RefreshDistributionPoint

Add this parameter to update the package content on the distribution points. If you don't include this parameter, you need to manually update distribution points. For more information, see [Manage distributed content](/mem/configmgr/core/servers/deploy/configure/deploy-and-manage-content#bkmk_manage).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RefreshDistributionPointAfterRemoveSoftwareUpdateFromPackage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdate

Specify an array of software update objects to remove from the package. To get this object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: ByObject_Id, ByObject_Name, ByObject_Object
Aliases: SoftwareUpdates

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateId

Specify an array of IDs for software updates to remove from the package. This value is the **CI_ID** of the update, for example `1584792`.

```yaml
Type: String[]
Parameter Sets: ById_Id, ById_Name, ById_Object
Aliases: SoftwareUpdateIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName

Specify an array of names for software updates to remove from the package.

```yaml
Type: String[]
Parameter Sets: ByName_Id, ByName_Name, ByName_Object
Aliases: SoftwareUpdateNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SoftwareUpdatePackage

Specify a software update package object from which to remove the updates. To get this object, use the [Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByObject_Object, ById_Object, ByName_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdatePackageId

Specify a software update package ID from which to remove the updates. This value is a standard package ID, for example `XYZ0035E`.

```yaml
Type: String
Parameter Sets: ById_Id, ByObject_Id, ByName_Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdatePackageName

Specify a software update package name from which to remove the updates.

```yaml
Type: String
Parameter Sets: ByObject_Name, ById_Name, ByName_Name
Aliases:

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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)

[New-CMSoftwareUpdateDeploymentPackage](Set-CMSoftwareUpdateDeploymentPackage.md)

[Set-CMSoftwareUpdateDeploymentPackage](Set-CMSoftwareUpdateDeploymentPackage.md)

[Remove-CMSoftwareUpdateDeploymentPackage](Remove-CMSoftwareUpdateDeploymentPackage.md)

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)

[Save-CMSoftwareUpdate](Save-CMSoftwareUpdate.md)
