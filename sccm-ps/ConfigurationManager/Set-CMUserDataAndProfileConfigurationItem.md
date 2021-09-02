---
description: Modifies a user data and profile configuration item.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMUserDataAndProfileConfigurationItem
---

# Set-CMUserDataAndProfileConfigurationItem

## SYNOPSIS
Modifies a user data and profile configuration item.

## SYNTAX

### SetByValue (Default)
```
Set-CMUserDataAndProfileConfigurationItem [-AccessPolicy <Boolean>] [-AddAdminGroupToRupEnabled <Boolean>]
 [-AllowAllDevice <Boolean>] [-AllowCrossForestUserPolicy <Boolean>] [-AppDataRoaming <FolderRedirectionType>]
 [-BackgroundSynchronization <SynchronizationType>] [-BackgroundUploadHour <Int32>]
 [-ConfigureFolderRedirection <Boolean>] [-ConfigureOfflineFile <Boolean>]
 [-ConfigureRoamingUserProfile <Boolean>] [-ConnectionTransferRate <Int32>] [-Contact <FolderRedirectionType>]
 [-DeleteProfileOlderDays <Int32>] [-DeleteRoamingCacheEnabled <Boolean>] [-Desktop <FolderRedirectionType>]
 [-DetectSlowLink <Boolean>] [-DeviceType <DeviceType>] [-DisableMakeOffline <Boolean>]
 [-DisableWorkOffline <Boolean>] [-Document <FolderRedirectionType>] [-Download <FolderRedirectionType>]
 [-EnableOfflineFile <Boolean>] [-EnableSlowLink <Boolean>] [-ErrorDays <Int32>] [-ExcludeList <String[]>]
 [-Favorite <FolderRedirectionType>] [-FileSynchronization <SynchronizationType>]
 [-ForceUnloadDisabled <Boolean>] [-GrantExclusiveRight <Boolean>] [-InputObject] <IResultObject>
 [-LeaveFolderNewLocation <Boolean>] [-LimitDisk <Int32>] [-Link <FolderRedirectionType>]
 [-ManageAdvancedSetting <Boolean>] [-ManageSlowLink <Boolean>] [-MoveCachedFolder <Boolean>]
 [-MoveContent <Boolean>] [-Music <FolderRedirectionType>] [-OfflineFile <String[]>]
 [-OnlyAllowLocalProfile <Boolean>] [-OwnerCheckDisabled <Boolean>] [-Picture <FolderRedirectionType>]
 [-ProfileUploadDisabled <Boolean>] [-SavedGame <FolderRedirectionType>] [-Search <FolderRedirectionType>]
 [-SlowLink <Int32>] [-SlowLinkUIEnabled <Boolean>] [-SpecifiedLocation <String>] [-SpecifyTime <String>]
 [-SpecifyTimeMin <Int32>] [-StartMenu <FolderRedirectionType>] [-SynchronizationList <String[]>]
 [-SynchronizationPolicy <Boolean>] [-SyncMins <Int32>] [-TempProfileLogonBlocked <Boolean>] [-TimeOut <Int32>]
 [-UseCommonAlert <Boolean>] [-UseSpecifiedLocation <Boolean>] [-Video <FolderRedirectionType>]
 [-WaitForNetworkSec <Int32>] [-WarningDays <Int32>] [-Description <String>] [-Digest <ConfigurationItem>]
 [-DigestPath <String>] [-DigestXml <String>] [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMUserDataAndProfileConfigurationItem [-AccessPolicy <Boolean>] [-AddAdminGroupToRupEnabled <Boolean>]
 [-AllowAllDevice <Boolean>] [-AllowCrossForestUserPolicy <Boolean>] [-AppDataRoaming <FolderRedirectionType>]
 [-BackgroundSynchronization <SynchronizationType>] [-BackgroundUploadHour <Int32>]
 [-ConfigureFolderRedirection <Boolean>] [-ConfigureOfflineFile <Boolean>]
 [-ConfigureRoamingUserProfile <Boolean>] [-ConnectionTransferRate <Int32>] [-Contact <FolderRedirectionType>]
 [-DeleteProfileOlderDays <Int32>] [-DeleteRoamingCacheEnabled <Boolean>] [-Desktop <FolderRedirectionType>]
 [-DetectSlowLink <Boolean>] [-DeviceType <DeviceType>] [-DisableMakeOffline <Boolean>]
 [-DisableWorkOffline <Boolean>] [-Document <FolderRedirectionType>] [-Download <FolderRedirectionType>]
 [-EnableOfflineFile <Boolean>] [-EnableSlowLink <Boolean>] [-ErrorDays <Int32>] [-ExcludeList <String[]>]
 [-Favorite <FolderRedirectionType>] [-FileSynchronization <SynchronizationType>]
 [-ForceUnloadDisabled <Boolean>] [-GrantExclusiveRight <Boolean>] [-LeaveFolderNewLocation <Boolean>]
 [-LimitDisk <Int32>] [-Link <FolderRedirectionType>] [-ManageAdvancedSetting <Boolean>]
 [-ManageSlowLink <Boolean>] [-MoveCachedFolder <Boolean>] [-MoveContent <Boolean>]
 [-Music <FolderRedirectionType>] [-OfflineFile <String[]>] [-OnlyAllowLocalProfile <Boolean>]
 [-OwnerCheckDisabled <Boolean>] [-Picture <FolderRedirectionType>] [-ProfileUploadDisabled <Boolean>]
 [-SavedGame <FolderRedirectionType>] [-Search <FolderRedirectionType>] [-SlowLink <Int32>]
 [-SlowLinkUIEnabled <Boolean>] [-SpecifiedLocation <String>] [-SpecifyTime <String>] [-SpecifyTimeMin <Int32>]
 [-StartMenu <FolderRedirectionType>] [-SynchronizationList <String[]>] [-SynchronizationPolicy <Boolean>]
 [-SyncMins <Int32>] [-TempProfileLogonBlocked <Boolean>] [-TimeOut <Int32>] [-UseCommonAlert <Boolean>]
 [-UseSpecifiedLocation <Boolean>] [-Video <FolderRedirectionType>] [-WaitForNetworkSec <Int32>]
 [-WarningDays <Int32>] [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-Id] <Int32> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMUserDataAndProfileConfigurationItem [-AccessPolicy <Boolean>] [-AddAdminGroupToRupEnabled <Boolean>]
 [-AllowAllDevice <Boolean>] [-AllowCrossForestUserPolicy <Boolean>] [-AppDataRoaming <FolderRedirectionType>]
 [-BackgroundSynchronization <SynchronizationType>] [-BackgroundUploadHour <Int32>]
 [-ConfigureFolderRedirection <Boolean>] [-ConfigureOfflineFile <Boolean>]
 [-ConfigureRoamingUserProfile <Boolean>] [-ConnectionTransferRate <Int32>] [-Contact <FolderRedirectionType>]
 [-DeleteProfileOlderDays <Int32>] [-DeleteRoamingCacheEnabled <Boolean>] [-Desktop <FolderRedirectionType>]
 [-DetectSlowLink <Boolean>] [-DeviceType <DeviceType>] [-DisableMakeOffline <Boolean>]
 [-DisableWorkOffline <Boolean>] [-Document <FolderRedirectionType>] [-Download <FolderRedirectionType>]
 [-EnableOfflineFile <Boolean>] [-EnableSlowLink <Boolean>] [-ErrorDays <Int32>] [-ExcludeList <String[]>]
 [-Favorite <FolderRedirectionType>] [-FileSynchronization <SynchronizationType>]
 [-ForceUnloadDisabled <Boolean>] [-GrantExclusiveRight <Boolean>] [-LeaveFolderNewLocation <Boolean>]
 [-LimitDisk <Int32>] [-Link <FolderRedirectionType>] [-ManageAdvancedSetting <Boolean>]
 [-ManageSlowLink <Boolean>] [-MoveCachedFolder <Boolean>] [-MoveContent <Boolean>]
 [-Music <FolderRedirectionType>] [-OfflineFile <String[]>] [-OnlyAllowLocalProfile <Boolean>]
 [-OwnerCheckDisabled <Boolean>] [-Picture <FolderRedirectionType>] [-ProfileUploadDisabled <Boolean>]
 [-SavedGame <FolderRedirectionType>] [-Search <FolderRedirectionType>] [-SlowLink <Int32>]
 [-SlowLinkUIEnabled <Boolean>] [-SpecifiedLocation <String>] [-SpecifyTime <String>] [-SpecifyTimeMin <Int32>]
 [-StartMenu <FolderRedirectionType>] [-SynchronizationList <String[]>] [-SynchronizationPolicy <Boolean>]
 [-SyncMins <Int32>] [-TempProfileLogonBlocked <Boolean>] [-TimeOut <Int32>] [-UseCommonAlert <Boolean>]
 [-UseSpecifiedLocation <Boolean>] [-Video <FolderRedirectionType>] [-WaitForNetworkSec <Int32>]
 [-WarningDays <Int32>] [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-Name] <String> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMUserDataAndProfileConfigurationItem** cmdlet modifies a user data and profile configuration item that can apply to Windows 8 computers.
A configuration item can manage folder redirection, offline folders, and roaming user profiles.
You can create a configuration item by using the [New-CMUserDataAndProfileConfigurationItem](New-CMUserDataAndProfileConfigurationItem.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a configuration item
```
PS XYZ:\> Set-CMUserDataAndProfileConfigurationItem -Name "CMUDaPCI001" -NewName "CMUDaPCI0073" -ConfigureFolderRedirection $False -ConfigureOffineFile $False -ConfigureRoamingUserProfile $False -Description "User data and profile configuration information"
```

This command modifies the configuration item named CMUDaPCI001, changing its name to CMUDaPCI0073.
The command also sets values for whether the configuration item specifies folder redirection, offline folders, and roaming profiles, and it provides a description for the configuration item.

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
Aliases: FolderRedirectionUserConfigurationForApplicationData, FolderRedirectionUserConfigurationForAppDataRoaming
Accepted values: RedirectToRemote, RedirectToLocal, DoNotManage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackgroundSynchronization
Specifies a background synchronization type for file in offline mode.

The acceptable values for this parameter are:

- Disabled
- Enabled
- NotConfigured

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

### -BackgroundUploadHour
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

### -ConfigureFolderRedirection
Indicates whether the configuration item includes settings for folder redirection.

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

### -ConfigureOfflineFile
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ConfigureOffineFile

Required: False
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

Required: False
Position: Named
Default value: None
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

### -DetectSlowLink
Indicates whether to detect slow links.

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

### -Digest
```yaml
Type: ConfigurationItem
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DigestPath
```yaml
Type: String
Parameter Sets: (All)
Aliases: DesiredConfigurationDigestPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DigestXml
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

### -ExcludeList
Specifies an array of folders.
The configuration item excludes these folders from roaming profiles.

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
The acceptable values for this parameter are:

- Disabled
- Enabled
- NotConfigured

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

### -Id
Specifies an array of IDs for user data and profile configuration items.

```yaml
Type: Int32
Parameter Sets: SetById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a user data and profile configuration item object.
To obtain a configuration item object, use the [Get-CMUserDataAndProfileConfigurationItem](Get-CMUserDataAndProfileConfigurationItem.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LeaveFolderNewLocation
Indicates whether to leave the folder in the redirected location in the event that you remove this configuration item.

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
Specifies an array of names of user data and profile configuration items.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the configuration item.

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
Indicates whether to enable the user logon prompt to allow profile download when a device detects a slow link.

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

### -SynchronizationList
Specifies an array of folders.
The configuration item specifies these subfolders of Appdata\Roaming to synchronize only at logon and logoff.

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

### -TimeOut
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
### Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItem
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMUserDataAndProfileConfigurationItem](New-CMUserDataAndProfileConfigurationItem.md)
