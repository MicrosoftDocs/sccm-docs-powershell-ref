---
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMMicrosoftEdgeBrowserProfiles

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ById (Default)
```
Set-CMMicrosoftEdgeBrowserProfiles -Id <Int32> [-NewName <String>] [-PassThru]
 [-SupportedPlatform <IResultObject[]>] [-AllowAddressBarDropDown <EdgeBrowserSettingType>]
 [-AllowAutoFill <EdgeBrowserSettingType>] [-AllowCookies <EdgeBrowserSettingType>]
 [-AllowDeveloperTools <EdgeBrowserSettingType>] [-AllowDoNotTrack <EdgeBrowserSettingType>]
 [-AllowExtensions <EdgeBrowserSettingType>] [-AllowPasswordManager <EdgeBrowserSettingType>]
 [-AllowPopups <EdgeBrowserSettingType>] [-AllowSearchSuggestions <EdgeBrowserSettingType>]
 [-AllowSmartScreen <EdgeBrowserSettingType>] [-ClearBrowsingDataOnExit <EdgeBrowserSettingType>]
 [-Description <String>] [-PreventOverrideFiles <EdgeBrowserSettingType>]
 [-PreventPromptOverride <EdgeBrowserSettingType>] [-SendIntranetTrafficToIE <EdgeBrowserSettingType>]
 [-SetEdgeBrowserAsDefault <EdgeBrowserAsDefaultSettingType>]
 [-SyncFavoritesIEAndEdge <EdgeBrowserSettingType>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValue
```
Set-CMMicrosoftEdgeBrowserProfiles -InputObject <IResultObject> [-NewName <String>] [-PassThru]
 [-SupportedPlatform <IResultObject[]>] [-AllowAddressBarDropDown <EdgeBrowserSettingType>]
 [-AllowAutoFill <EdgeBrowserSettingType>] [-AllowCookies <EdgeBrowserSettingType>]
 [-AllowDeveloperTools <EdgeBrowserSettingType>] [-AllowDoNotTrack <EdgeBrowserSettingType>]
 [-AllowExtensions <EdgeBrowserSettingType>] [-AllowPasswordManager <EdgeBrowserSettingType>]
 [-AllowPopups <EdgeBrowserSettingType>] [-AllowSearchSuggestions <EdgeBrowserSettingType>]
 [-AllowSmartScreen <EdgeBrowserSettingType>] [-ClearBrowsingDataOnExit <EdgeBrowserSettingType>]
 [-Description <String>] [-PreventOverrideFiles <EdgeBrowserSettingType>]
 [-PreventPromptOverride <EdgeBrowserSettingType>] [-SendIntranetTrafficToIE <EdgeBrowserSettingType>]
 [-SetEdgeBrowserAsDefault <EdgeBrowserAsDefaultSettingType>]
 [-SyncFavoritesIEAndEdge <EdgeBrowserSettingType>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMMicrosoftEdgeBrowserProfiles -Name <String> [-NewName <String>] [-PassThru]
 [-SupportedPlatform <IResultObject[]>] [-AllowAddressBarDropDown <EdgeBrowserSettingType>]
 [-AllowAutoFill <EdgeBrowserSettingType>] [-AllowCookies <EdgeBrowserSettingType>]
 [-AllowDeveloperTools <EdgeBrowserSettingType>] [-AllowDoNotTrack <EdgeBrowserSettingType>]
 [-AllowExtensions <EdgeBrowserSettingType>] [-AllowPasswordManager <EdgeBrowserSettingType>]
 [-AllowPopups <EdgeBrowserSettingType>] [-AllowSearchSuggestions <EdgeBrowserSettingType>]
 [-AllowSmartScreen <EdgeBrowserSettingType>] [-ClearBrowsingDataOnExit <EdgeBrowserSettingType>]
 [-Description <String>] [-PreventOverrideFiles <EdgeBrowserSettingType>]
 [-PreventPromptOverride <EdgeBrowserSettingType>] [-SendIntranetTrafficToIE <EdgeBrowserSettingType>]
 [-SetEdgeBrowserAsDefault <EdgeBrowserAsDefaultSettingType>]
 [-SyncFavoritesIEAndEdge <EdgeBrowserSettingType>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AllowAddressBarDropDown
{{ Fill AllowAddressBarDropDown Description }}

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
{{ Fill AllowAutoFill Description }}

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
{{ Fill AllowCookies Description }}

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
{{ Fill AllowDeveloperTools Description }}

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
{{ Fill AllowDoNotTrack Description }}

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
{{ Fill AllowExtensions Description }}

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
{{ Fill AllowPasswordManager Description }}

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
{{ Fill AllowPopups Description }}

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
{{ Fill AllowSearchSuggestions Description }}

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
{{ Fill AllowSmartScreen Description }}

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
{{ Fill ClearBrowsingDataOnExit Description }}

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

### -Description
{{ Fill Description Description }}

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
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill Id Description }}

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: MicrosoftEdgeBrowserPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

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
{{ Fill NewName Description }}

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
{{ Fill PassThru Description }}

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

### -PreventOverrideFiles
{{ Fill PreventOverrideFiles Description }}

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
{{ Fill PreventPromptOverride Description }}

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
{{ Fill SendIntranetTrafficToIE Description }}

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
{{ Fill SetEdgeBrowserAsDefault Description }}

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
{{ Fill SupportedPlatform Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncFavoritesIEAndEdge
{{ Fill SyncFavoritesIEAndEdge Description }}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
