---
description: Changes configuration settings of operating system images.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMOperatingSystemImage
---

# Set-CMOperatingSystemImage

## SYNOPSIS
Changes configuration settings of operating system images.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMOperatingSystemImage -InputObject <IResultObject> [-NewName <String>] [-Path <String>]
 [-Version <String>] [-Description <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMOperatingSystemImage -Id <String> [-NewName <String>] [-Path <String>] [-Version <String>]
 [-Description <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMOperatingSystemImage -Name <String> [-NewName <String>] [-Path <String>] [-Version <String>]
 [-Description <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMOperatingSystemImage** cmdlet changes configuration settings of one or more operating system images in Microsoft System Center Configuration Manager.
Operating system images are .wim format files and represent a compressed collection of reference files and folders that System Center Configuration Manager requires to successfully install and configure an operating system on a computer.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Change settings for an operating system image by using an ID
```
PS XYZ:\> Set-CMOperatingSystemImage -Id "Cm10004f" -NewName "Microsoft Windows 8 (x64)" -Version "I20C" -Description "Dept02 Sys Image" -Path "\\Contoso\Public\OSD\win8x64.wim"
```

This command changes configuration settings of the operating system image that has the ID Cm10004f.
The command renames the operating system image, adds a version and description, and specifies the path to the installation source files of the operating system image.

### Example 2: Add an operating system image to a security scope by using a name
```
PS XYZ:\> Set-CMOperatingSystemImage -SecurityScopeAction AddMembership -SecurityScopeName "SecScope02" -Name "ImagePkg01"
```

This command adds membership to the security scope named SecScope02 for the operating system image named ImagePkg01.

### Example 3: Remove an operating system image from a security scope
```
PS XYZ:\> Set-CMOperatingSystemImage -SecurityScopeAction RemoveMembership -SecurityScopeName "SecScope02" -Name "ImagePkg01"
```

This command removes membership from the security scope named SecScope02 for the operating system image named ImagePkg01.

## PARAMETERS

### -CopyToPackageShareOnDistributionPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CopyToPackageShareOnDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomPackageShareName
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

### -Description
Specifies a description for the operating system image.

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

### -DisconnectUserFromDistributionPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointMins
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPointsMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointRetryCount
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPointsRetries

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointUpdateSchedule
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableBinaryDeltaReplication
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
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

### -Id
Specifies an array of IDs of operating system images.

```yaml
Type: String
Parameter Sets: SetById
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a CMOperatingSystemImage object.
To obtain a CMOperatingSystemImage object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MulticastAllow
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MulticastEncrypt
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MulticastTransferOnly
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of an operating system image.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies the new name of an operating system image.

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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -Path
Specifies the network path to the operating system image source .wim file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistContentInCache
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestageBehavior
```yaml
Type: PrestageBehavior
Parameter Sets: (All)
Aliases:
Accepted values: ManualCopy, DownloadDelta, OnDemand

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Specifies a change for the priority of the deployment type.
Valid values are: Increase and Decrease.

```yaml
Type: Priority
Parameter Sets: (All)
Aliases:
Accepted values: High, Medium, Low

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendToPreferredDistributionPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: SendToPreferredDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies the version of the operating system image.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[New-CMOperatingSystemImage](New-CMOperatingSystemImage.md)

[Remove-CMOperatingSystemImage](Remove-CMOperatingSystemImage.md)

[Get-CMOperatingSystemImageUpdateSchedule](Get-CMOperatingSystemImageUpdateSchedule.md)
