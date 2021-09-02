---
description: Changes configuration settings of OS upgrade packages.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: Set-CMOperatingSystemInstaller
---

# Set-CMOperatingSystemInstaller

## SYNOPSIS
Changes configuration settings of OS upgrade packages.

## SYNTAX

### SetById (Default)
```
Set-CMOperatingSystemInstaller [-CopyToPackageShareOnDistributionPoint <Boolean>]
 [-CustomPackageShareName <String>] [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>] -Id <String>
 [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>] [-MulticastTransferOnly <Boolean>]
 [-NewName <String>] [-PassThru] [-Path <String>] [-PersistContentInCache <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-Reload]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMOperatingSystemInstaller [-CopyToPackageShareOnDistributionPoint <Boolean>]
 [-CustomPackageShareName <String>] [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>]
 -InputObject <IResultObject> [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru] [-Path <String>]
 [-PersistContentInCache <Boolean>] [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-Reload]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMOperatingSystemInstaller [-CopyToPackageShareOnDistributionPoint <Boolean>]
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

The **Set-CMOperatingSystemInstaller** cmdlet changes configuration settings of one or more OS upgrade packages in Configuration Manager.
An OS upgrade package contains all the files that Configuration Manager needs to install a Windows OS on a reference computer.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change settings for an OS upgrade package by using a name

This command changes configuration settings of the OS upgrade package named Win8x64.
The command renames the OS upgrade package, adds a version and description, and specifies the path to the installation source files of the OS upgrade package.

```powershell
Set-CMOperatingSystemInstaller -Name "Win8x64" -NewName "OsiWin8x64" -Version "I20B" -Description "Dept02 Sys Install" -Path "\\Win2k3X64contoso\Public\OSD\win8x64"
```

### Example 2: Add an OS upgrade package to a security scope by using a name

This command adds membership to the security scope named SecScope02 for the OS upgrade package named InstPkg01.

```powershell
Set-CMOperatingSystemInstaller -SecurityScopeAction AddMembership -SecurityScopeName "SecScope02" -Name "InstPkg01"
```

### Example 3: Remove an OS upgrade package from a security scope

This command removes membership to the security scope named SecScope02 for the OS upgrade package named InstPkg01.

```powershell
Set-CMOperatingSystemInstaller -SecurityScopeAction RemoveMembership -SecurityScopeName "SecScope02" -Name "InstPkg01"
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
Specifies a description for the OS upgrade package.

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

### -Id
Specifies an array of IDs of OS upgrade packages.

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
Specifies a CMOperatingSystemInstaller object.
To obtain a CMOperatingSystemInstaller object, use the [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md) cmdlet.

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
Specifies the name of an OS upgrade package.

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
Specifies the new name of an OS upgrade package.

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
Specifies the network path to the installation source files of an OS upgrade package.

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
Specifies the version of an OS upgrade package.

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

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[New-CMOperatingSystemInstaller](New-CMOperatingSystemInstaller.md)

[Remove-CMOperatingSystemInstaller](Remove-CMOperatingSystemInstaller.md)
