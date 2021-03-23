---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/04/2020
online version:
schema: 2.0.0
---

# New-CMMicrosoftEdgeBrowserProfiles

## SYNOPSIS

Create a policy to manage Microsoft Edge Legacy browser settings.

## SYNTAX

```
New-CMMicrosoftEdgeBrowserProfiles [-AllowAddressBarDropDown <EdgeBrowserSettingType>]
 [-AllowAutoFill <EdgeBrowserSettingType>] [-AllowCookies <EdgeBrowserSettingType>]
 [-AllowDeveloperTools <EdgeBrowserSettingType>] [-AllowDoNotTrack <EdgeBrowserSettingType>]
 [-AllowExtensions <EdgeBrowserSettingType>] [-AllowPasswordManager <EdgeBrowserSettingType>]
 [-AllowPopups <EdgeBrowserSettingType>] [-AllowSearchSuggestions <EdgeBrowserSettingType>]
 [-AllowSmartScreen <EdgeBrowserSettingType>] [-ClearBrowsingDataOnExit <EdgeBrowserSettingType>]
 [-Description <String>] -Name <String> [-PreventOverrideFiles <EdgeBrowserSettingType>]
 [-PreventPromptOverride <EdgeBrowserSettingType>] [-SendIntranetTrafficToIE <EdgeBrowserSettingType>]
 [-SetEdgeBrowserAsDefault <EdgeBrowserAsDefaultSettingType>] -SupportedPlatform <IResultObject[]>
 [-SyncFavoritesIEAndEdge <EdgeBrowserSettingType>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to manage Microsoft Edge Legacy browser settings. This policy only applies to clients on Windows 10, version 1703 or later, and Microsoft Edge Legacy version 45 and earlier. For more information, see [Configure Microsoft Edge Legacy settings in Configuration Manager](/mem/configmgr/compliance/deploy-use/browser-profiles). This article also includes more details on the specific policy settings.

For more information on managing Microsoft Edge version 77 or later with Configuration Manager, see [Deploy Microsoft Edge, version 77 and later](/mem/configmgr/apps/deploy-use/deploy-edge). For more information on configuring policies for Microsoft Edge version 77 or later, see [Microsoft Edge - Policies](/DeployEdge/microsoft-edge-policies).

## EXAMPLES

### Example 1

```powershell
$os1 = Get-CMSupportedPlatform -Name "*Windows*10*" -Fast

New-CMMicrosoftEdgeBrowserProfiles -Name "Edge1" -SupportedPlatform $os1 -AllowAddressBarDropDown Allow -AllowAutoFill Allow -AllowCookies Allow -AllowDeveloperTools Allow -AllowDoNotTrack Allow -AllowExtensions Allow -AllowPasswordManager Allow -AllowPopups Allow -AllowSearchSuggestions Allow -AllowSmartScreen Allow -ClearBrowsingDataOnExit Allow -Description "Edge1" -PreventOverrideFiles Allow -PreventPromptOverride Allow -SendIntranetTrafficToIE Allow -SetEdgeBrowserAsDefault Configured -SyncFavoritesIEAndEdge Allow
```

## PARAMETERS

### -AllowAddressBarDropDown

Configure the setting to **Allow address bar drop-down**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowAutoFill

Configure the setting to **Allow autofill**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowCookies

Configure the setting to **Allow cookies**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDeveloperTools

Configure the setting to **Allow Developer Tools**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowDoNotTrack

Configure the setting to **Allow Do Not Track headers**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowExtensions

Configure the setting to **Allow extensions**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPasswordManager

Configure the setting to **Allow password manager**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPopups

Configure the setting to **Allow pop-up blocker**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSearchSuggestions

Configure the setting to **Allow search suggestions in address bar**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases: AllowSearchSuggestionsinAddressBar
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSmartScreen

Configure the Microsoft Defender SmartScreen setting to **Allow SmartScreen**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearBrowsingDataOnExit

Configure the setting to **Allow clear browsing data on exit**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description for the browser profile policy.

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

### -Name

Specify a name for the browser profile policy.

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

### -PreventOverrideFiles

Configure the Microsoft Defender SmartScreen setting: **Users can override SmartScreen prompt for files**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases: PreventSmartScreenPromptOverrideForFiles
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreventPromptOverride

Configure the Microsoft Defender SmartScreen setting: **Users can override SmartScreen prompt for sites**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases: PreventSmartScreenPromptOverride
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendIntranetTrafficToIE

Configure the setting to **Allow send intranet traffic to Internet Explorer**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases: SendIntranetTrafficToInternetExplorer
Accepted values: Allow, NotAllow, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetEdgeBrowserAsDefault

Configure the setting to **Set Microsoft Edge browser as default**. If you configure this setting, Configuration Manager configures the Windows 10 default app setting for web browser to Microsoft Edge Legacy.

```yaml
Type: EdgeBrowserAsDefaultSettingType
Parameter Sets: (All)
Aliases:
Accepted values: Configured, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportedPlatform

Specify a supported platform object to which this policy is applicable. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncFavoritesIEAndEdge

Configure the setting to **Allow sync favorites between Microsoft browsers**.

```yaml
Type: EdgeBrowserSettingType
Parameter Sets: (All)
Aliases: SyncFavoritesBetweenIEAndMicrosoftEdge
Accepted values: Allow, NotAllow, NotConfigured

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

### None

## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Get-CMMicrosoftEdgeBrowserProfiles](Get-CMMicrosoftEdgeBrowserProfiles.md)

[Set-CMMicrosoftEdgeBrowserProfiles](Set-CMMicrosoftEdgeBrowserProfiles.md)

[Configure Microsoft Edge Legacy settings in Configuration Manager](/mem/configmgr/compliance/deploy-use/browser-profiles)
