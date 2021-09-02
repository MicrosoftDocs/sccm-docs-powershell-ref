---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/04/2020
online version:
schema: 2.0.0
---

# Set-CMOneDriveBusinessProfile

## SYNOPSIS

Configure a OneDrive for Business profile policy.

## SYNTAX

### ByName (Default)
```
Set-CMOneDriveBusinessProfile [-AddSupportedPlatform <IResultObject[]>] [-ClearSupportedPlatform]
 [-Description <String>] [-KnownFolderMoveOption <MoveKnownFolderOptionType>] -Name <String>
 [-NewName <String>] [-O365TenantId <String>] [-PreventRedirectKnownFolders <Boolean>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-ShowNotification <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMOneDriveBusinessProfile [-AddSupportedPlatform <IResultObject[]>] [-ClearSupportedPlatform]
 [-Description <String>] -Id <Int32> [-KnownFolderMoveOption <MoveKnownFolderOptionType>] [-NewName <String>]
 [-O365TenantId <String>] [-PreventRedirectKnownFolders <Boolean>] [-RemoveSupportedPlatform <IResultObject[]>]
 [-ShowNotification <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
Set-CMOneDriveBusinessProfile [-AddSupportedPlatform <IResultObject[]>] [-ClearSupportedPlatform]
 [-Description <String>] -InputObject <IResultObject> [-KnownFolderMoveOption <MoveKnownFolderOptionType>]
 [-NewName <String>] [-O365TenantId <String>] [-PreventRedirectKnownFolders <Boolean>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-ShowNotification <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Configure a OneDrive for Business profile policy. Use this policy to move Windows known folders to OneDrive for Business. These folders include Desktop, Documents, and Pictures. In each profile, you can specify settings for moving the Windows known folders. For more information on OneDrive for Business, see [Redirect and move Windows known folders to OneDrive](/onedrive/redirect-known-folders).

For more information on this Configuration Manager policy, see [OneDrive for Business profiles](/mem/configmgr/compliance/deploy-use/onedrive-profile).

## EXAMPLES

### Example 1

```powershell
$Plats2 = Get-CMSupportedPlatform -Name "All Windows 10 *" -Fast -Platform "X64"

Set-CMOneDriveBusinessProfile -Name "ODfB policy" -ClearSupportedPlatform -AddSupportedPlatform $Plats2 -O365TenantId "05d683b9-caed-4eea-b229-45f72b89ca05" -KnownFolderMoveOption SilentlyMove -ShowNotification $true -PreventRedirectKnownFolders $true
```

## PARAMETERS

### -AddSupportedPlatform

Specify a supported platform object to which this policy is applicable. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearSupportedPlatform

Add this parameter to clear the current list of supported platforms.

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

### -Description

Specify an optional description for the OneDrive for Business policy to better identify it.

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

### -Id

Specify the **CI ID** of the OneDrive for Business policy to configure. The format is a five- to seven-digit number, for example `403823`.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CI_ID, CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a OneDrive for Business policy object to configure. To get this object, use the [Get-CMOneDriveBusinessProfile](Get-CMOneDriveBusinessProfile.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: OneDriveBusinessPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KnownFolderMoveOption

Specify how you want to move the known folders to OneDrive:

- `PromptToMove`: Prompt users to move Windows known folders to OneDrive. The user sees a wizard to move their files. If they choose to postpone or decline moving their folders, OneDrive periodically reminds them.
- `SilentlyMove`: Silently move Windows known folders to OneDrive. When this policy applies to the device, the OneDrive client automatically redirects the known folders to OneDrive for Business.

```yaml
Type: MoveKnownFolderOptionType
Parameter Sets: (All)
Aliases: OneDriveKnownFolderMoveOption
Accepted values: PromptToMove, SilentlyMove

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the OneDrive for Business policy to configure.

```yaml
Type: String
Parameter Sets: ByName
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

To rename this OneDrive for Business policy, specify a new name.

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

### -O365TenantId

Specify your Microsoft 365 tenant ID. [Find your Microsoft 365 tenant ID](/onedrive/find-your-office-365-tenant-id).

```yaml
Type: String
Parameter Sets: (All)
Aliases: AADTenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreventRedirectKnownFolders

Set this parameter to `$true` to prevent users from redirecting their Windows known folders back to their PC. It disables the option in OneDrive for Business on the client for users to move these folders back to the device.

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

### -RemoveSupportedPlatform

Specify a supported platform object to remove from this policy. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShowNotification

When you use `SilentlyMove` for the **KnownFolderMoveOption** parameter, if you set this parameter to `$true`, the OneDrive client notifies the user after it moves their folders.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy
## NOTES

## RELATED LINKS

[Get-CMOneDriveBusinessProfile](Get-CMOneDriveBusinessProfile.md)

[New-CMOneDriveBusinessProfile](New-CMOneDriveBusinessProfile.md)

[OneDrive for Business profiles](/mem/configmgr/compliance/deploy-use/onedrive-profile)
