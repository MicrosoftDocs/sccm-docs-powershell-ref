---
description: Validate content on a distribution point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2020
schema: 2.0.0
title: Invoke-CMContentValidation
---

# Invoke-CMContentValidation

## SYNOPSIS

Validate content on a distribution point.

## SYNTAX

### SearchByValueMandatory_Application (Default)
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DisableContentDependencyDetection]
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_Application
```
Invoke-CMContentValidation -ApplicationId <String[]> [-CollectionName <String[]>]
 [-DisableContentDependencyDetection] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory_Application
```
Invoke-CMContentValidation -ApplicationName <String[]> [-CollectionName <String[]>]
 [-DisableContentDependencyDetection] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory_BootImage
```
Invoke-CMContentValidation -BootImageId <String[]> [-CollectionName <String[]>]
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_BootImage
```
Invoke-CMContentValidation -BootImageName <String[]> [-CollectionName <String[]>]
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_DeploymentPackage
```
Invoke-CMContentValidation [-CollectionName <String[]>] -DeploymentPackageId <String[]>
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_DeploymentPackage
```
Invoke-CMContentValidation [-CollectionName <String[]>] -DeploymentPackageName <String[]>
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_DriverPackage
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -DriverPackageId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_DriverPackage
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -DriverPackageName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_OperatingSystemImage
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemImage <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_OperatingSystemImage
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemImageId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_OperatingSystemImage
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemImageName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_OperatingSystemInstaller
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemInstallerId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_OperatingSystemInstaller
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemInstallerName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_Package
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -PackageId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_Package
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -PackageName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_TaskSequence
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -TaskSequenceId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_TaskSequence
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -TaskSequenceName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to validate content on a distribution point. When you validate the content, Configuration Manager makes sure that the entire set of files transferred successfully to the distribution point. For more information, see [Deploy and manage content in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/deploy-and-manage-content#validate-content).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Validate content for an application

This command validates the content for the application named **Dictionary** one the distribution point named **DPServer01**.

```powershell
Invoke-CMContentValidation -ApplicationName "Dictionary" -DistributionPointName "DPServer01"
```

## PARAMETERS

### -ApplicationId

Specify an array of application IDs to validate. These IDs are GUIDs as strings.

By default, Configuration Manager also validates the content for dependent applications. To disable this behavior, use the **DisableContentDependencyDetection** parameter.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_Application
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName

Specify an array of application names to validate.

By default, Configuration Manager also validates the content for dependent applications. To disable this behavior, use the **DisableContentDependencyDetection** parameter.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_Application
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId

Specify an array of boot image IDs to validate. For example, `"XYZ00015"`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_BootImage
Aliases: BootImageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageName

Specify an array of boot image names to validate.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_BootImage
Aliases: BootImageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify an array of Configuration Manager collection names. Use this collection to target the distribution points on which to validate the content.

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

### -DeploymentPackageId

Specify an array of software update deployment package IDs to validate. For example, `"XYZ00016"`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_DeploymentPackage
Aliases: DeploymentPackageIds, SoftwareUpdatesPackageId, SoftwareUpdatesPackageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentPackageName

Specify an array of software update deployment package names to validate.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_DeploymentPackage
Aliases: DeploymentPackageNames, SoftwareUpdatesPackageName, SoftwareUpdatesPackageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableContentDependencyDetection

Add this parameter to not automatically validate content for dependent apps.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByValueMandatory_Application, SearchByIdMandatory_Application, SearchByNameMandatory_Application
Aliases: DisableDetectAssociatedContentDependencies

Required: False
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

### -DistributionPointGroupName

Specify an array of distribution point group names on which to validate the content.

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

### -DistributionPointName

Specify an array of distribution point names on which to validate the content.

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

### -DriverPackageId

Specify an array of driver package IDs to validate. For example, `"XYZ00017"`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_DriverPackage
Aliases: DriverPackageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName

Specify an array of driver package names to validate.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_DriverPackage
Aliases: DriverPackageNames

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

### -InputObject

Specify an object type to validate. To get these objects, use one of the following cmdlets:

- [Get-CMApplication](Get-CMApplication.md) for an application
- [Get-CMPackage](Get-CMPackage.md) for a legacy package
- [Get-CMBootImage](Get-CMBootImage.md) for a boot image
- [Get-CMDeploymentPackage](Get-CMDeploymentPackage.md) for a software update deployment package
- [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) for the content in a software update group
- [Get-CMDriverPackage](Get-CMDriverPackage.md) for a driver package
- [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) for an OS image
- [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md) for an OS upgrade package
- [Get-CMTaskSequence](Get-CMTaskSequence.md) for the content referenced by a task sequence

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Application, Package, BootImage, DeploymentPackage, SoftwareUpdatePackage, DriverPackage, ImagePackage, OperatingSystemInstaller, TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -OperatingSystemImage

Specify an OS image object to validate. To get this object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_OperatingSystemImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageId

Specify an array of OS image IDs to validate. For example, `"XYZ00018"`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_OperatingSystemImage
Aliases: OperatingSystemImageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageName

Specify an array of OS image names to validate.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_OperatingSystemImage
Aliases: OperatingSystemImageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerId

Specify an array of OS upgrade package IDs to validate. For example, `"XYZ00019"`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_OperatingSystemInstaller
Aliases: OperatingSystemInstallerIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemInstallerName

Specify an array of OS upgrade package names to validate.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_OperatingSystemInstaller
Aliases: OperatingSystemImageInstallerNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId

Specify an array of legacy package IDs to validate. For example, `"XYZ00020"`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_Package
Aliases: PackageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName

Specify an array of legacy package names to validate.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_Package
Aliases: PackageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId

Specify an array of task sequence IDs to validate referenced content. For example, `"XYZ00021"`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_TaskSequence
Aliases: TaskSequenceIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify an array of task sequence names to validate referenced content.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_TaskSequence
Aliases: TaskSequenceNames

Required: True
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

[Get-CMApplication](Get-CMApplication.md)

[Get-CMDeploymentPackage](Get-CMDeploymentPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[Remove-CMContentDistribution](Remove-CMContentDistribution.md)

[Start-CMContentDistribution](Start-CMContentDistribution.md)

[Update-CMDistributionPoint](Update-CMDistributionPoint.md)
