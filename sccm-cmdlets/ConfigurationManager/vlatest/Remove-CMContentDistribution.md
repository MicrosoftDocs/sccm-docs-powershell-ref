---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834011
schema: 2.0.0
ms.assetid: 1851328A-D7D3-40E2-B3D5-7EA9454B5D02
---

# Remove-CMContentDistribution

## SYNOPSIS
Removes packages from a distribution point.

## SYNTAX

### SearchByValueMandatory_Application (Default)
```
Remove-CMContentDistribution [-Force] -Application <IResultObject> [-CollectionName <String[]>]
 [-DisableContentDependencyDetection] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory_Application
```
Remove-CMContentDistribution [-Force] -ApplicationId <String[]> [-CollectionName <String[]>]
 [-DisableContentDependencyDetection] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory_Application
```
Remove-CMContentDistribution [-Force] -ApplicationName <String[]> [-CollectionName <String[]>]
 [-DisableContentDependencyDetection] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByValueMandatory_BootImage
```
Remove-CMContentDistribution [-Force] -BootImage <IResultObject> [-CollectionName <String[]>]
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_BootImage
```
Remove-CMContentDistribution [-Force] -BootImageId <String[]> [-CollectionName <String[]>]
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_BootImage
```
Remove-CMContentDistribution [-Force] -BootImageName <String[]> [-CollectionName <String[]>]
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_DeploymentPackage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] -DeploymentPackage <IResultObject>
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_DeploymentPackage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] -DeploymentPackageId <String[]>
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_DeploymentPackage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] -DeploymentPackageName <String[]>
 [-DistributionPointGroupName <String[]>] [-DistributionPointName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_DriverPackage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -DriverPackage <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_DriverPackage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -DriverPackageId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_DriverPackage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -DriverPackageName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_OperatingSystemImage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemImage <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_OperatingSystemImage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemImageId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_OperatingSystemImage
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemImageName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_OperatingSystemInstaller
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemInstaller <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_OperatingSystemInstaller
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemInstallerId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_OperatingSystemInstaller
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -OperatingSystemInstallerName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_Package
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -Package <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_Package
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -PackageId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_Package
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -PackageName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory_TaskSequence
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -TaskSequence <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_TaskSequence
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -TaskSequenceId <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_TaskSequence
```
Remove-CMContentDistribution [-Force] [-CollectionName <String[]>] [-DistributionPointGroupName <String[]>]
 [-DistributionPointName <String[]>] -TaskSequenceName <String[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMContentDistribution** cmdlet removes one or more packages from a distribution point.

## EXAMPLES

### Example 1: Remove a driver package from a distribution point
```
PS C:\>Remove-CMContentDistribution -DriverPackageID "PCP00019" -DistributionPointName "distribution-server.contoso.com"
```

This command removes the driver package PCO00019 from the distribution point distribution-server.contoso.com.

## PARAMETERS

### -Application
Specifies a Configuration Manager application object.
To get a **CMApplication** object, use the [Get-CMApplication](./Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_Application
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Specifies an array of application IDs.

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

### -BootImage
Specifies a boot image object.
To get a **CMBootImage** object, use the Get-CMBootImage cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_BootImage
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

### -DeploymentPackage
Specifies a deployment package object.
To get a **CMDeploymentPackage** object, use the Get-CMDeploymentPackage cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_DeploymentPackage
Aliases: 

Required: True
Position: Named
Default value: None
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
Indicates that wildcard handling is disabled.

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
Specifies the name of a distribution point that is associated with the deployment package.

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

### -DriverPackage
Specifies a driver package object.
To get a **CMDriverPackage** object, use the Get-CMDriverPackage cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_DriverPackage
Aliases: 

Required: True
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

### -Force
Forces the command to run without asking for user confirmation.

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
Indicates that wildcard handling is enabled.

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

### -OperatingSystemImage
Specifies a **CMOperatingSystemImage** object.
To get a **CMOperatingSystemImage** object, use the Get-CMOperatingSystemImage cmdlet.

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

### -OperatingSystemInstaller
Specifies an operating system installer object.
To get a **CMOperatingSystemInstaller** object, use the Get-CMOperatingSystemInstaller cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_OperatingSystemInstaller
Aliases: 

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

### -Package
Specifies a package object.
To get a **CMPackage** object, use the Get-CMPackage cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_Package
Aliases: 

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

### -TaskSequence
Specifies a task sequence object.
To get a **CMTaskSequence** object, use the Get-CMTaskSequence cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_TaskSequence
Aliases: 

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

[Get-CMApplication](./Get-CMApplication.md)

[Get-CMBootImage](./Get-CMBootImage.md)

[Get-CMDeploymentPackage](./Get-CMDeploymentPackage.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)

[Get-CMOperatingSystemImage](./Get-CMOperatingSystemImage.md)

[Get-CMOperatingSystemInstaller](./Get-CMOperatingSystemInstaller.md)

[Get-CMPackage](./Get-CMPackage.md)

[Get-CMTaskSequence](./Get-CMTaskSequence.md)

[Invoke-CMContentValidation](./Invoke-CMContentValidation.md)

[Start-CMContentDistribution](./Start-CMContentDistribution.md)


