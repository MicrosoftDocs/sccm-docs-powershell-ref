---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: CB1B6D39-7EE5-449E-92A5-357AD8F68922
online version: https://go.microsoft.com/fwlink/?linkid=834117
schema: 2.0.0
---

# Invoke-CMContentValidation

## SYNOPSIS
Validates packages on a distribution point.

## SYNTAX

### SearchByValueMandatory_Application (Default)
```
Invoke-CMContentValidation [-CollectionName <String[]>] [-DisableContentDependencyDetection]
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMContentValidation -InputObject <IResultObject> [-CollectionName <String[]>]
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
The **Invoke-CMContentValidation** cmdlet validates one or more packages on a distribution point.
Validating the content ensures that the entire set of files transferred successfully to the distribution point.

## EXAMPLES

### Example 1: Validate content for an application
```
PS C:\>Invoke-CMContentValidation -ApplicationName "Dict.app" -DistributionPointName "DPServer01"
```

This command validates the package for the application named Dict.app one the distribution point named DPServer01.

## PARAMETERS

### -ApplicationId
Specifies an array of application IDs.
These IDs are GUIDs as strings.

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
Specifies an array of application names.

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
Specifies an array of IDs of boot images.

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
Specifies an array of names of boot images.

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
Specifies the name of a Configuration Manager collection.

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
Specifies an array of IDs of deployment packages.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_DeploymentPackage
Aliases: DeploymentPackageIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentPackageName
Specifies an array of names of deployment packages.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_DeploymentPackage
Aliases: DeploymentPackageNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableContentDependencyDetection
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
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
Specifies the name of a distribution point group.

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
Specifies the name of a distribution point that is associated with the content.

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
Specifies an array of IDs of driver packages.

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
Specifies an array of names of driver packages.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
Specifies an operating system image object.
To get a **CMOperatingSystemImage** object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

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
Specifies an array of IDs of operating system images.

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
Specifies an array of names of operating system images.

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
Specifies an array of IDs of operating system installers.

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
Specifies an array of names of operating system installers.

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
Specifies an array of IDs of packages.

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
Specifies an array of names of packages.

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
Specifies an array of IDs of task sequences.

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
Specifies an array of names of task sequences.

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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Get-CMDeploymentPackage](Get-CMDeploymentPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)

[Start-CMContentDistribution](Start-CMContentDistribution.md)


