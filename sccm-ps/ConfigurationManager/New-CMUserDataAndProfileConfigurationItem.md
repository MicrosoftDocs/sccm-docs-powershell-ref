---
author: aczechowski
description: Creates a user data and profile configuration item.
external help file: AdminUI.PS.Dcm.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMUserDataAndProfileConfigurationItem
titleSuffix: Configuration Manager
---

# New-CMUserDataAndProfileConfigurationItem

## SYNOPSIS
Creates a user data and profile configuration item.

## SYNTAX

```
New-CMUserDataAndProfileConfigurationItem -Name <String> [-Description <String>]
 -ConfigureFolderRedirection <Boolean> -ConfigureOfflineFile <Boolean> -ConfigureRoamingUserProfile <Boolean>
 [-DeviceType <DeviceType>] [-Desktop <FolderRedirectionType>] [-StartMenu <FolderRedirectionType>]
 [-Document <FolderRedirectionType>] [-Music <FolderRedirectionType>] [-Video <FolderRedirectionType>]
 [-Favorite <FolderRedirectionType>] [-Contact <FolderRedirectionType>] [-Download <FolderRedirectionType>]
 [-Link <FolderRedirectionType>] [-Search <FolderRedirectionType>] [-SavedGame <FolderRedirectionType>]
 [-AppDataRoaming <FolderRedirectionType>] [-Picture <FolderRedirectionType>] [-UseSpecifiedLocation <Boolean>]
 [-SpecifiedLocation <String>] [-ManageAdvancedSetting <Boolean>] [-GrantExclusiveRight <Boolean>]
 [-MoveContent <Boolean>] [-LeaveFolderNewLocation <Boolean>] [-MoveCachedFolder <Boolean>]
 [-UseCommonAlert <Boolean>] [-ErrorDays <Int32>] [-WarningDays <Int32>] [-EnableOfflineFile <Boolean>]
 [-BackgroundSynchronization <SynchronizationType>] [-FileSynchronization <SynchronizationType>]
 [-OfflineFile <String[]>] [-EnableSlowLink <Boolean>] [-SlowLink <Int32>] [-SyncMins <Int32>]
 [-DisableWorkOffline <Boolean>] [-DisableMakeOffline <Boolean>] [-LimitDisk <Int32>]
 [-AllowAllDevice <Boolean>] [-ExcludeProfile <String[]>] [-SyncDirectory <String[]>]
 [-ManageSlowLink <Boolean>] [-DetectSlowLinkDisabled <Boolean>] [-Timeout <Int32>]
 [-ConnectionTransferRate <Int32>] [-SlowLinkUIEnabled <Boolean>] [-WaitForNetworkSec <Int32>]
 [-AccessPolicy <Boolean>] [-OwnerCheckDisabled <Boolean>] [-AddAdminGroupToRupEnabled <Boolean>]
 [-AllowCrossForestUserPolicy <Boolean>] [-TempProfileLogonBlocked <Boolean>]
 [-OnlyAllowLocalProfile <Boolean>] [-SynchronizationPolicy <Boolean>] [-SpecifyTime <String>]
 [-SpecifyTimeMin <Int32>] [-DeleteRoamingCacheEnabled <Boolean>] [-DeleteProfileOlderDays <Int32>]
 [-ForceUnloadDisabled <Boolean>] [-ProfileUploadDisabled <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMUserDataAndProfileConfigurationItem** cmdlet creates a user data and profile configuration item that can apply to Windows 8 computers.
A configuration item can manage folder redirection, offline folders, and roaming user profiles.
You can modify settings for an existing configuration item by using the Set-CMUserDataAndProfileConfigurationItem cmdlet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Specify folder redirection
```
PS XYZ:\> New-CMUserDataAndProfileConfigurationItem -ConfigureFolderRedirection $True -ConfigureOffineFile $True -ConfigureRoamingUserProfile $True -Name "CMUserDataProfileCI07" -FolderRedirectionUserConfigurationForDesktop RedirectToRemote -SpecifiedLocation "\\Server017\Shared" -UseSpecifiedLocation $True
```

This command creates a configuration item named CMUserDataProfileCI07.
This configuration item manages folder redirection, offline folders, and roaming user profiles.
The command specifies redirect to remote for the Desktop folder.
The command includes a specified location and includes the *UseSpecifiedLocation* parameter with a value of $True.

### Example 2: Specify settings for a configuration item
```
PS XYZ:\> New-CMUserDataAndProfileConfigurationItem -ConfigureFolderRedirection $True -ConfigureOffineFile $True -ConfigureRoamingUserProfile $True -Name "CMUserDataProfileCI27" -AccessPolicy $True -AddAdminGroupToRUPEnabled $True -AllowAllDevice $False -AllowCrossForestUserPolicy $True -BackgroundSynchronization NotConfigured -ConnectionTransferRate 300 -DeleteProfileOlderDays 300 -DeleteRoamingCacheEnabled $True -Description "Configuration item for off-site staff." -DetectSlowLinkDisabled $False -DeviceType OnlyOnPrimaryDevices -DisableMakeOffline $True -DisableWorkOffline $True -EnableOfflineFile $True -EnableSlowLink $True -ErrorDays 200 -ExcludeList "MiscFolder" -FileSynchronization Enabled -FolderRedirectionUserConfigurationForAppDataRoaming RedirectToLocal -FolderRedirectionUserConfigurationForContacts RedirectToRemote -FolderRedirectionUserConfigurationForDesktop RedirectToRemote -FolderRedirectionUserConfigurationForDocuments RedirectToRemote -FolderRedirectionUserConfigurationForDownloads RedirectToLocal -FolderRedirectionUserConfigurationForFavorites RedirectToLocal -FolderRedirectionUserConfigurationForLinks RedirectToRemote -FolderRedirectionUserConfigurationForMusic RedirectToLocal -FolderRedirectionUserConfigurationForPictures RedirectToRemote -FolderRedirectionUserConfigurationForSavedGames RedirectToRemote -FolderRedirectionUserConfigurationForSearches RedirectToLocal -FolderRedirectionUserConfigurationForStartMenu RedirectToLocal -FolderRedirectionUserConfigurationForVideos RedirectToRemote -ForceUnloadDisabled $True -GrantExclusiveRight $False -LeaveFolderNewLocation $True -LimitDisk 1024  -ManageAdvancedSetting $True -ManageSlowLink $True -MoveCachedFolder $True -MoveContent $False -OfflineFile "\\Server78\MiscShared" -OnlyAllowLocalProfiles $True -OwnerCheckDisabled $True -ProfileUploadDisabled $True -SlowLink 350 -SlowLinkUIEnabled $True -SpecifiedLocation "\\Server221\Part17" -SpecifyTimeInterval 120  -SynchronizationInterval 1200 -SynchronizationList "\\Server221\Part17" -SynchronizationPolicy $True -TempProfileLogonBlocked $True -TimeOut 130 -UseCommonAlert $True -UseSpecifiedLocation $True -WaitForNetworkInSeconds 300 -WarningDays 100
```

This command creates a configuration item named CMUserDataProfileCI27.
This configuration item manages folder redirection, offline folders, and roaming user profiles.
Like the previous example, this command specifies folder redirection settings, this time for several folders.
The command includes other settings for folder redirection, offline folders, and roaming user profiles.

## PARAMETERS

### -AccessPolicy
Indicates whether this configuration item manages profile access settings for roaming profiles.

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

### -AddAdminGroupToRupEnabled
Indicates whether to grant the Administrators group access to roaming profile folders.

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

### -AllowAllDevice
Indicates whether to allow roaming profiles on all devices.
If this value is $False, roaming profiles apply only to the primary device for a user.

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

### -AllowCrossForestUserPolicy
Indicates whether to permit user policies to roam across Active Directory forests that have a trust relationship with the current forest.

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

### -AppDataRoaming
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForAppDataRoaming
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackgroundSynchronization
Specifies a background synchronization type for a file in offline mode.
The acceptable values for this parameter are: Disabled, Enabled, and NotConfigured.

```yaml
Type: SynchronizationType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigureFolderRedirection
Indicates whether the configuration item includes settings for folder redirection.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigureOfflineFile
Indicates whether the configuration item includes settings for offline folders.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigureRoamingUserProfile
Indicates whether the configuration item includes settings for roaming user profiles.

```yaml
Type: Boolean
Parameter Sets: (All)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionTransferRate
Specifies a connection transfer rate.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Contact
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForContacts, Contacts
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteProfileOlderDays
Specifies the number of days to keep a user profile since the last time someone used it.
A computer deletes an older profile when it restarts.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteRoamingCacheEnabled
Indicates whether to delete cached copies of roaming user profiles.
The default for this parameter is $False.

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

### -Description
Specifies a description for the configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Desktop
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForDesktop
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DetectSlowLinkDisabled
Indicates whether to disable slow link detection.

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

### -DeviceType
Specifies the applicability of folder redirection for user devices.
The acceptable values for this parameter are:

- FolderRedirectionOnAnyDeviceCachingOnPrimaryDevicesOnly.
Folder redirection for any user device, but caching only on the primary device for a user.
- OnAnyDevice.
Folder redirection and caching on any device.
- OnlyOnPrimaryDevices.
Folder redirection and caching on the primary device for a user.

```yaml
Type: DeviceType
Parameter Sets: (All)
Aliases:
Accepted values: OnAnyDevice, OnlyOnPrimaryDevices, FolderRedirectionOnAnyDeviceCachingOnPrimaryDevicesOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableMakeOffline
Indicates whether users can disable the **Make Available Offline** command.

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

### -DisableWorkOffline
Indicates whether users can disable the **Work Offline** command.

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

### -Document
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForDocuments, Documents
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Download
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForDownloads, Downloads
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableOfflineFile
Indicates whether this configuration item enables use of offline files.

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

### -EnableSlowLink
Indicates whether the configuration enables work with offline files over a slow link.

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

### -ErrorDays
Specifies the number of days to wait before the profile creates an error.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExcludeProfile
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ExcludeList

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Favorite
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForFavorites, Favorites
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSynchronization
Specifies a file synchronization type for metered networks for work in offline mode.
The acceptable values for this parameter are: Disabled, Enabled, and NotConfigured.

```yaml
Type: SynchronizationType
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceUnloadDisabled
Indicates whether to disable forced unload of a user profile at logoff.
The default value for this parameter is $False.

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

### -GrantExclusiveRight
Indicates whether to grant the user exclusive permissions to a redirected folder.

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

### -LeaveFolderNewLocation
Indicates whether to leave the folder in the redirected location in the event you remove this configuration item.

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

### -LimitDisk
Specifies a limit, in megabytes, for the disk space used for offline files.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Link
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForLinks, Links
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageAdvancedSetting
Indicates whether this configuration item manages advanced settings for folder redirection.
Specify values for any of the following parameters:

- *GrantExclusiveRight*
- *MoveContent*
- *LeaveFolderNewLocation*
- *MoveCachedFolder*

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

### -ManageSlowLink
Indicates whether this profile item manages slow links.

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

### -MoveCachedFolder
Indicates whether to move the cached folder when the path updates on the server.

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

### -MoveContent
Indicates whether to move the contents of redirected folders to the new location.

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

### -Music
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForMusic
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfflineFile
Specifies an array of Administrative user assigned offline folders, as UNC paths as follows: \\\\server\share\%UserName%.

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

### -OnlyAllowLocalProfile
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: OnlyAllowLocalProfiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OwnerCheckDisabled
Indicates whether the configuration item does not check for ownership of roaming profile folders.

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

### -Picture
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForPictures, Pictures
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProfileUploadDisabled
Indicates whether to disable uploading of profiles.

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

### -SavedGame
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForSavedGames, SavedGames
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Search
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForSearches, Searches
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SlowLink
Specifies a value for a slow link.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SlowLinkUIEnabled
Indicates whether to enable user logon prompt to allow profile download when a device detects a slow link.

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

### -SpecifiedLocation
Specifies a specified location.

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

### -SpecifyTime
Specifies a time for background upload of the user hive.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: 12:00 AM, 1:00 PM, 2:00 PM, 3:00 PM, 4:00 PM, 5:00 PM, 6:00 PM, 7:00 PM, 8:00 PM, 9:00 PM, 10:00 PM, 11:00 PM, 12:00 PM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SpecifyTimeMin
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SpecifyTimeInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartMenu
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForStartMenu
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncDirectory
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SynchronizationList, SyncDirectories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SynchronizationInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SynchronizationPolicy
Indicates whether to use a synchronization policy.

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

### -TempProfileLogonBlocked
Indicates whether to block users from logging on by using a temporary profile.

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

### -Timeout
Specifies a timeout value.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseCommonAlert
Indicates whether to use common alerts.

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

### -UseSpecifiedLocation
Indicates whether to use the specified location referred to by the *SpecifiedLocation* parameter.

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

### -Video
```yaml
Type: FolderRedirectionType
Parameter Sets: (All)
Aliases: FolderRedirectionUserConfigurationForVideos, Videos
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForNetworkSec
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WaitForNetworkInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WarningDays
Specifies the number of days to wait before the profile creates a warning.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMUserDataAndProfileConfigurationItem](Set-CMUserDataAndProfileConfigurationItem.md)


