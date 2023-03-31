---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMClientSettingSoftwareCenter

## SYNOPSIS
Use this cmdlet to configure the client settings in the **Software Center** group.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingSoftwareCenter [-AddCustomTab <SoftwareCenterTabItem[]>] [-ClearCustomTab]
 [-ColorScheme <Color>] [-CompanyName <String>] [-CustomTabName <String>] [-CustomTabUrl <Uri>]
 [-EnableApplicationsTab <Boolean>] [-EnableComplianceTab <Boolean>] [-EnableCustomize <Boolean>]
 [-EnableOperatingSystemsTab <Boolean>] [-EnableOptionsTab <Boolean>] [-EnableStatusTab <Boolean>]
 [-EnableUpdatesTab <Boolean>] [-HideApplicationCatalogLink <Boolean>] [-HideInstalledApplication <Boolean>]
 [-HideUnapprovedApplication <Boolean>] [-LogoFilePath <String>] [-MoveSelectedTabToIndex <Int32>]
 [-RemoveCustomTabName <String[]>] [-SelectBuiltInTab <BuiltInTab>] [-SelectCustomTabName <String>]
 [-SelectedTabNewName <String>] [-SelectedTabNewUrl <Uri>] [-SelectTabIndex <Int32>]
 [-SetInvisibleTabName <String[]>] [-SetVisibleTabName <String[]>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingSoftwareCenter [-AddCustomTab <SoftwareCenterTabItem[]>] [-ClearCustomTab]
 [-ColorScheme <Color>] [-CompanyName <String>] [-CustomTabName <String>] [-CustomTabUrl <Uri>]
 [-EnableApplicationsTab <Boolean>] [-EnableComplianceTab <Boolean>] [-EnableCustomize <Boolean>]
 [-EnableOperatingSystemsTab <Boolean>] [-EnableOptionsTab <Boolean>] [-EnableStatusTab <Boolean>]
 [-EnableUpdatesTab <Boolean>] [-HideApplicationCatalogLink <Boolean>] [-HideInstalledApplication <Boolean>]
 [-HideUnapprovedApplication <Boolean>] [-LogoFilePath <String>] [-MoveSelectedTabToIndex <Int32>]
 [-RemoveCustomTabName <String[]>] [-SelectBuiltInTab <BuiltInTab>] [-SelectCustomTabName <String>]
 [-SelectedTabNewName <String>] [-SelectedTabNewUrl <Uri>] [-SelectTabIndex <Int32>]
 [-SetInvisibleTabName <String[]>] [-SetVisibleTabName <String[]>] [-DefaultSetting] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingSoftwareCenter [-AddCustomTab <SoftwareCenterTabItem[]>] [-ClearCustomTab]
 [-ColorScheme <Color>] [-CompanyName <String>] [-CustomTabName <String>] [-CustomTabUrl <Uri>]
 [-EnableApplicationsTab <Boolean>] [-EnableComplianceTab <Boolean>] [-EnableCustomize <Boolean>]
 [-EnableOperatingSystemsTab <Boolean>] [-EnableOptionsTab <Boolean>] [-EnableStatusTab <Boolean>]
 [-EnableUpdatesTab <Boolean>] [-HideApplicationCatalogLink <Boolean>] [-HideInstalledApplication <Boolean>]
 [-HideUnapprovedApplication <Boolean>] [-LogoFilePath <String>] [-MoveSelectedTabToIndex <Int32>]
 [-RemoveCustomTabName <String[]>] [-SelectBuiltInTab <BuiltInTab>] [-SelectCustomTabName <String>]
 [-SelectedTabNewName <String>] [-SelectedTabNewUrl <Uri>] [-SelectTabIndex <Int32>]
 [-SetInvisibleTabName <String[]>] [-SetVisibleTabName <String[]>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the client settings in the **Software Center** group.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive. For more information, see the [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add custom tabs

Add five custom tab instances:

```PowerShell
$itemA = New-CMSoftwareCenterTabItem -Name "1abc" -Url "http://www.a"
$itemB = New-CMSoftwareCenterTabItem -Name "2abc" -Url "https://www.b"
$itemC = New-CMSoftwareCenterTabItem -Name "3abc" -Url "http://www.c"
$itemD = New-CMSoftwareCenterTabItem -Name "4abc" -Url "https://www.d"
$itemE = New-CMSoftwareCenterTabItem -Name "5abc" -Url "http://www.e"
Set-CMClientSettingSoftwareCenter -DefaultSetting -AddCustomTab ($itemA, $itemB, $itemC, $itemD, $itemE)
```

### Example 2: Hide a tab

Set a custom tab to invisible by name:

```powershell
Set-CMClientSettingSoftwareCenter -DefaultSetting -SetInvisibleTabName ("2abc","4abc", "5abc")
```

### Example 3: Remove a tab

Remove a custom tab by name:

```powershell
Set-CMClientSettingSoftwareCenter -DefaultSetting -RemoveCustomTabName ("3abc","4abc")
```

### Example 4: Show a hidden tab

Set a custom tab to visible by name:

```powershell
Set-CMClientSettingSoftwareCenter -DefaultSetting -SetVisibleTabName ("2abc", "5abc")
```

### Example 5: Change tab order

```powershell
# Move selected custom tab to specific position by name:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectCustomTabName "1abc" -MoveSelectedTabToIndex 0

# Move selected built-in tab to specific position:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectBuiltInTab AvailableSoftware -MoveSelectedTabToIndex 0

# Move selected tab to specific position by current index of position:
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectTabIndex 0 -MoveSelectedTabToIndex 1
```

### Example 6: Change tab properties

Modify a custom tab's name and Url by name:

```powershell
Set-CMClientSettingSoftwareCenter -DefaultSetting -SelectCustomTabName "1abc" -SelectedTabNewName "new1abc" -SelectedTabNewUrl http://www.aNew
```

### Example 7: Remove custom tabs

Clean up all custom tabs from the client setting:

```powershell
Set-CMClientSettingSoftwareCenter -DefaultSetting -ClearCustomTab
```

## PARAMETERS

### -AddCustomTab
Use this parameter to add a custom tab to the Software Center client setting.

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
Use this parameter to remove a custom tab from the Software Center client setting.

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
Use this parameter to configure the Software Center client setting, **Color scheme for Software Center**.
Example color object for: Red=255, Green=74, Blue=74: **$colorObject = [system.drawing.color]::FromArgb(255,255,74,74)**

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
Use this parameter to configure the Software Center client setting, **Company name**.

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
This parameter is deprecated. To create a custom tab, use the [New-CMSoftwareCenterTabItem](New-CMSoftwareCenterTabItem.md) cmdlet.

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
This parameter is deprecated. To create a custom tab, use the [New-CMSoftwareCenterTabItem](New-CMSoftwareCenterTabItem.md) cmdlet.

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
This parameter will apply settings to the default client setting. Use parameter **-Name** for any custom client setting.

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

### -EnableApplicationsTab
Use this parameter to show or hide the default **Applications** tab in Software Center.

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
Use this parameter to show or hide the default **Device Compliance** tab in Software Center.

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
This parameter will enable custom Software Center settings. Like the color scheme or a logo.

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
Use this parameter to show or hide the default **Operating Systems** tab in Software Center.

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
Use this parameter to show or hide the default **Options** tab in Software Center.

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
Use this parameter to show or hide the default **Installation Status** tab in Software Center.

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
Use this parameter to show or hide the default **Updates** tab in Software Center.

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

### -HideApplicationCatalogLink
Use this parameter to enable or disable the following client setting in the **Software Center** group: **Hide Application Catalog link in Software Center**

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
Use this parameter to enable or disable the following client setting in the **Software Center** group: **Hide installed applications in Software Center**

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
Use this parameter to enable or disable the following client setting in the **Software Center** group: **Hide unapproved applications in Software Center**

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
Object of **Get-CMClientSetting**

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
Use this parameter to specify the file path to an image to display as the logo in Software Center.

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
Use this parameter to change the order of tabs in Software Center. Specify an integer for position, with `0` at the top. Use one of the following parameters to select the tab to move: **SelectCustomTabName**, **SelectBuiltInTab**, **SelectTabIndex**.

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
Use this parameter to specify a client setting by its name.

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

### -RemoveCustomTabName
Specify the name of a custom tab to remove from the client setting. You can set one or more names.

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
Use this parameter to select one of the built-in tabs in Software Center. Use one of the following parameters in the same command to change the tab's configuration: **MoveSelectedTabToIndex**, **SelectedTabNewName**, **SelectedTabNewUrl**.

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
Use this parameter to select by name a custom tab in Software Center. Use one of the following parameters in the same command to change the tab's configuration: **MoveSelectedTabToIndex**, **SelectedTabNewName**, **SelectedTabNewUrl**.

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
In the same command when you select a tab, use this parameter to change the name of the tab.

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
In the same command when you select a tab, use this parameter to change the URL of the tab.

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
Use this parameter to select a tab by order in Software Center. Specify an integer for position, with `0` at the top. Use one of the following parameters in the same command to change the tab's configuration: **MoveSelectedTabToIndex**, **SelectedTabNewName**, **SelectedTabNewUrl**.

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
Use this parameter to hide a custom tab based upon its name. You can specify one or more tabs.

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
Use this parameter to show a custom tab based upon its name. You can specify one or more tabs.

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

### System.Object
## NOTES

## RELATED LINKS

[About client settings - Software Center](/mem/configmgr/core/clients/deploy/about-client-settings#software-center)

[Plan for Software Center](/mem/configmgr/apps/plan-design/plan-for-software-center)
