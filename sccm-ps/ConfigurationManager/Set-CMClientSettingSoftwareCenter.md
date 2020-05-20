---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMClientSettingSoftwareCenter

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingSoftwareCenter [-EnableCustomize <Boolean>] [-CompanyName <String>] [-ColorScheme <Color>]
 [-LogoFilePath <String>] [-HideUnapprovedApplication <Boolean>] [-HideInstalledApplication <Boolean>]
 [-HideApplicationCatalogLink <Boolean>] [-EnableApplicationsTab <Boolean>] [-EnableUpdatesTab <Boolean>]
 [-EnableOperatingSystemsTab <Boolean>] [-EnableStatusTab <Boolean>] [-EnableComplianceTab <Boolean>]
 [-EnableOptionsTab <Boolean>] [-ClearCustomTab] [-RemoveCustomTabName <String[]>]
 [-AddCustomTab <SoftwareCenterTabItem[]>] [-SetVisibleTabName <String[]>] [-SetInvisibleTabName <String[]>]
 [-SelectCustomTabName <String>] [-SelectBuiltInTab <BuiltInTab>] [-SelectTabIndex <Int32>]
 [-MoveSelectedTabToIndex <Int32>] [-SelectedTabNewName <String>] [-SelectedTabNewUrl <Uri>]
 [-CustomTabName <String>] [-CustomTabUrl <Uri>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingSoftwareCenter [-EnableCustomize <Boolean>] [-CompanyName <String>] [-ColorScheme <Color>]
 [-LogoFilePath <String>] [-HideUnapprovedApplication <Boolean>] [-HideInstalledApplication <Boolean>]
 [-HideApplicationCatalogLink <Boolean>] [-EnableApplicationsTab <Boolean>] [-EnableUpdatesTab <Boolean>]
 [-EnableOperatingSystemsTab <Boolean>] [-EnableStatusTab <Boolean>] [-EnableComplianceTab <Boolean>]
 [-EnableOptionsTab <Boolean>] [-ClearCustomTab] [-RemoveCustomTabName <String[]>]
 [-AddCustomTab <SoftwareCenterTabItem[]>] [-SetVisibleTabName <String[]>] [-SetInvisibleTabName <String[]>]
 [-SelectCustomTabName <String>] [-SelectBuiltInTab <BuiltInTab>] [-SelectTabIndex <Int32>]
 [-MoveSelectedTabToIndex <Int32>] [-SelectedTabNewName <String>] [-SelectedTabNewUrl <Uri>]
 [-CustomTabName <String>] [-CustomTabUrl <Uri>] [-DefaultSetting] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingSoftwareCenter [-EnableCustomize <Boolean>] [-CompanyName <String>] [-ColorScheme <Color>]
 [-LogoFilePath <String>] [-HideUnapprovedApplication <Boolean>] [-HideInstalledApplication <Boolean>]
 [-HideApplicationCatalogLink <Boolean>] [-EnableApplicationsTab <Boolean>] [-EnableUpdatesTab <Boolean>]
 [-EnableOperatingSystemsTab <Boolean>] [-EnableStatusTab <Boolean>] [-EnableComplianceTab <Boolean>]
 [-EnableOptionsTab <Boolean>] [-ClearCustomTab] [-RemoveCustomTabName <String[]>]
 [-AddCustomTab <SoftwareCenterTabItem[]>] [-SetVisibleTabName <String[]>] [-SetInvisibleTabName <String[]>]
 [-SelectCustomTabName <String>] [-SelectBuiltInTab <BuiltInTab>] [-SelectTabIndex <Int32>]
 [-MoveSelectedTabToIndex <Int32>] [-SelectedTabNewName <String>] [-SelectedTabNewUrl <Uri>]
 [-CustomTabName <String>] [-CustomTabUrl <Uri>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddCustomTab
{{ Fill AddCustomTab Description }}

```yaml
Type: SoftwareCenterTabItem[]
Parameter Sets: (All)
Aliases: AddCustomTabs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearCustomTab
{{ Fill ClearCustomTab Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearAllCustomTabs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ColorScheme
{{ Fill ColorScheme Description }}

```yaml
Type: Color
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompanyName
{{ Fill CompanyName Description }}

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

### -CustomTabName
{{ Fill CustomTabName Description }}

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

### -CustomTabUrl
{{ Fill CustomTabUrl Description }}

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSetting
{{ Fill DefaultSetting Description }}

```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

Required: True
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

### -EnableApplicationsTab
{{ Fill EnableApplicationsTab Description }}

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

### -EnableComplianceTab
{{ Fill EnableComplianceTab Description }}

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

### -EnableCustomize
{{ Fill EnableCustomize Description }}

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

### -EnableOperatingSystemsTab
{{ Fill EnableOperatingSystemsTab Description }}

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

### -EnableOptionsTab
{{ Fill EnableOptionsTab Description }}

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

### -EnableStatusTab
{{ Fill EnableStatusTab Description }}

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

### -EnableUpdatesTab
{{ Fill EnableUpdatesTab Description }}

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

### -HideApplicationCatalogLink
{{ Fill HideApplicationCatalogLink Description }}

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

### -HideInstalledApplication
{{ Fill HideInstalledApplication Description }}

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

### -HideUnapprovedApplication
{{ Fill HideUnapprovedApplication Description }}

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

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LogoFilePath
{{ Fill LogoFilePath Description }}

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

### -MoveSelectedTabToIndex
{{ Fill MoveSelectedTabToIndex Description }}

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

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

Required: True
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

### -RemoveCustomTabName
{{ Fill RemoveCustomTabName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveCustomTabNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectBuiltInTab
{{ Fill SelectBuiltInTab Description }}

```yaml
Type: BuiltInTab
Parameter Sets: (All)
Aliases:
Accepted values: AvailableSoftware, Updates, Osd, InstallationStatus, Compliance, Options

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectCustomTabName
{{ Fill SelectCustomTabName Description }}

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

### -SelectedTabNewName
{{ Fill SelectedTabNewName Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: SelectedCustomTabNewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectedTabNewUrl
{{ Fill SelectedTabNewUrl Description }}

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: SelectedCustomTabNewUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectTabIndex
{{ Fill SelectTabIndex Description }}

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

### -SetInvisibleTabName
{{ Fill SetInvisibleTabName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SetInvisibleCustomTabNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SetVisibleTabName
{{ Fill SetVisibleTabName Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SetVisibleCustomTabNames

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

### System.Object
## NOTES

## RELATED LINKS
