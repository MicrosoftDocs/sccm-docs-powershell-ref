---
description: Changes configuration settings of OS images.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: Set-CMOperatingSystemImage
---

# Set-CMOperatingSystemImage

## SYNOPSIS
Changes configuration settings of OS images.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMOperatingSystemImage [-CopyToPackageShareOnDistributionPoint <Boolean>]
 [-CustomPackageShareName <String>] [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>]
 -InputObject <IResultObject> [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru] [-Path <String>]
 [-PersistContentInCache <Boolean>] [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-Reload]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMOperatingSystemImage [-CopyToPackageShareOnDistributionPoint <Boolean>]
 [-CustomPackageShareName <String>] [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>] -Id <String>
 [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>] [-MulticastTransferOnly <Boolean>]
 [-NewName <String>] [-PassThru] [-Path <String>] [-PersistContentInCache <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-Reload]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMOperatingSystemImage [-CopyToPackageShareOnDistributionPoint <Boolean>]
 [-CustomPackageShareName <String>] [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>]
 [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>] [-MulticastTransferOnly <Boolean>] -Name <String>
 [-NewName <String>] [-PassThru] [-Path <String>] [-PersistContentInCache <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-Reload]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMOperatingSystemImage** cmdlet changes configuration settings of one or more OS images in Configuration Manager.
OS images are .wim format files and represent a compressed collection of reference files and folders that Configuration Manager requires to successfully install and configure an OS on a computer.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change settings for an OS image by using an ID

This command changes configuration settings of the OS image that has the ID Cm10004f.
The command renames the OS image, adds a version and description, and specifies the path to the installation source files of the OS image.

```powershell
Set-CMOperatingSystemImage -Id "Cm10004f" -NewName "Microsoft Windows 8 (x64)" -Version "I20C" -Description "Dept02 Sys Image" -Path "\\Contoso\Public\OSD\win8x64.wim"
```

### Example 2: Add an OS image to a security scope by using a name

This command adds membership to the security scope named SecScope02 for the OS image named ImagePkg01.

```powershell
Set-CMOperatingSystemImage -SecurityScopeAction AddMembership -SecurityScopeName "SecScope02" -Name "ImagePkg01"
```

### Example 3: Remove an OS image from a security scope

This command removes membership from the security scope named SecScope02 for the OS image named ImagePkg01.

```powershell
Set-CMOperatingSystemImage -SecurityScopeAction RemoveMembership -SecurityScopeName "SecScope02" -Name "ImagePkg01"
```

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
Specifies a description for the OS image.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Can't combine with **DisableWildcardHandling**.

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
Specifies an array of IDs of OS images.

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
Specifies the name of an OS image.

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
Specifies the new name of an OS image.

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

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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
Specifies the network path to the OS image source .wim file.

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

### -Reload

Applies to version 2006 and later. If you change the image properties using an external tool, use this option to reload the information in the site database.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ReloadImage

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
Specifies the version of the OS image.

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

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[New-CMOperatingSystemImage](New-CMOperatingSystemImage.md)

[Remove-CMOperatingSystemImage](Remove-CMOperatingSystemImage.md)

[Get-CMOperatingSystemImageUpdateSchedule](Get-CMOperatingSystemImageUpdateSchedule.md)
