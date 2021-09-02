---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
online version:
schema: 2.0.0
---

# Set-CMApplicationGroup

## SYNOPSIS

Configure an existing application group.

## SYNTAX

### SetByValue (Default)
```
Set-CMApplicationGroup [-InputObject] <IResultObject> [-NewName <String>] [-Description <String>]
 [-Publisher <String>] [-SoftwareVersion <String>] [-OptionalReference <String>]
 [-AddAppCategory <IResultObject[]>] [-RemoveAppCategoryName <String[]>] [-CleanAppCategory]
 [-ReleaseDate <DateTime>] [-AddOwner <String[]>] [-RemoveOwner <String[]>] [-ClearOwner]
 [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>] [-ClearSupportContact]
 [-AddAppCatalog <AppDisplayInfo[]>] [-RemoveAppCatalog <Int32[]>] [-ClearAppCatalog]
 [-DefaultLanguageId <Int32>] [-ApplyToLanguageById <Int32>] [-LocalizedName <String>]
 [-AddUserCategory <IResultObject[]>] [-RemoveUserCategoryName <String[]>] [-CleanUserCategory]
 [-UserDocumentation <String>] [-LinkText <String>] [-PrivacyUrl <String>] [-LocalizedDescription <String>]
 [-Keyword <String[]>] [-IconLocationFile <String>] [-AddApplication <String[]>]
 [-RemoveApplication <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMApplicationGroup [-Id] <Int32> [-NewName <String>] [-Description <String>] [-Publisher <String>]
 [-SoftwareVersion <String>] [-OptionalReference <String>] [-AddAppCategory <IResultObject[]>]
 [-RemoveAppCategoryName <String[]>] [-CleanAppCategory] [-ReleaseDate <DateTime>] [-AddOwner <String[]>]
 [-RemoveOwner <String[]>] [-ClearOwner] [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>]
 [-ClearSupportContact] [-AddAppCatalog <AppDisplayInfo[]>] [-RemoveAppCatalog <Int32[]>] [-ClearAppCatalog]
 [-DefaultLanguageId <Int32>] [-ApplyToLanguageById <Int32>] [-LocalizedName <String>]
 [-AddUserCategory <IResultObject[]>] [-RemoveUserCategoryName <String[]>] [-CleanUserCategory]
 [-UserDocumentation <String>] [-LinkText <String>] [-PrivacyUrl <String>] [-LocalizedDescription <String>]
 [-Keyword <String[]>] [-IconLocationFile <String>] [-AddApplication <String[]>]
 [-RemoveApplication <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByModelName
```
Set-CMApplicationGroup -ModelName <String> [-NewName <String>] [-Description <String>] [-Publisher <String>]
 [-SoftwareVersion <String>] [-OptionalReference <String>] [-AddAppCategory <IResultObject[]>]
 [-RemoveAppCategoryName <String[]>] [-CleanAppCategory] [-ReleaseDate <DateTime>] [-AddOwner <String[]>]
 [-RemoveOwner <String[]>] [-ClearOwner] [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>]
 [-ClearSupportContact] [-AddAppCatalog <AppDisplayInfo[]>] [-RemoveAppCatalog <Int32[]>] [-ClearAppCatalog]
 [-DefaultLanguageId <Int32>] [-ApplyToLanguageById <Int32>] [-LocalizedName <String>]
 [-AddUserCategory <IResultObject[]>] [-RemoveUserCategoryName <String[]>] [-CleanUserCategory]
 [-UserDocumentation <String>] [-LinkText <String>] [-PrivacyUrl <String>] [-LocalizedDescription <String>]
 [-Keyword <String[]>] [-IconLocationFile <String>] [-AddApplication <String[]>]
 [-RemoveApplication <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMApplicationGroup [-Name] <String> [-NewName <String>] [-Description <String>] [-Publisher <String>]
 [-SoftwareVersion <String>] [-OptionalReference <String>] [-AddAppCategory <IResultObject[]>]
 [-RemoveAppCategoryName <String[]>] [-CleanAppCategory] [-ReleaseDate <DateTime>] [-AddOwner <String[]>]
 [-RemoveOwner <String[]>] [-ClearOwner] [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>]
 [-ClearSupportContact] [-AddAppCatalog <AppDisplayInfo[]>] [-RemoveAppCatalog <Int32[]>] [-ClearAppCatalog]
 [-DefaultLanguageId <Int32>] [-ApplyToLanguageById <Int32>] [-LocalizedName <String>]
 [-AddUserCategory <IResultObject[]>] [-RemoveUserCategoryName <String[]>] [-CleanUserCategory]
 [-UserDocumentation <String>] [-LinkText <String>] [-PrivacyUrl <String>] [-LocalizedDescription <String>]
 [-Keyword <String[]>] [-IconLocationFile <String>] [-AddApplication <String[]>]
 [-RemoveApplication <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the settings of an existing application group. Use an app group to deploy multiple applications to a collection as a single deployment. The metadata you specify about the app group is seen in Software Center as a single entity. You can order the apps in the group so that the client installs them in a specific order. For more information, see [Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename an app group

This example gets an object for the app group, and passes it to this cmdlet to rename it.

```powershell
$appgroup = Get-CMApplicationGroup -Name "Central app"
Set-CMApplicationGroup -InputObject $appgroup -NewName "Contoso Central App"
```

### Example 2: Add a localized name

This example configures the app group with a localized app name for the **Irish** language.

```powershell
Set-CMApplicationGroup -Name "Contoso Welcome app" -ApplyToLanguageById 60 -LocalizedName "Fáilte romhat"
```

## PARAMETERS

### -AddAppCatalog

Use this parameter to specify a Software Center entry for a specific language. This entry can include all of the localized information about the app group:

- Description
- IconLocationFile
- Keyword
- LinkText
- PrivacyUrl
- Title
- UserDocumentation

To get this object, use the [New-CMApplicationDisplayInfo](New-CMApplicationDisplayInfo.md) cmdlet.

```yaml
Type: AppDisplayInfo[]
Parameter Sets: (All)
Aliases: AppCatalogs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddAppCategory

Specify one or more administrative category objects to help you filter and find the app group in the console. To get these objects, use the [Get-CMCategory](Get-CMCategory.md) cmdlet. These categories are of type **AppCategories**.

To add categories to help users filter and find applications in Software Center, use the **AddUserCategory** parameter.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddAppCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddApplication

Specify a string array of app names to add to the group. If you already have an app object from another cmdlet like [Get-CMApplication](Get-CMApplication.md), this value is the **LocalizedDisplayName** property. For example: `$appList = @($app1.LocalizedDisplayName,$app2.LocalizedDisplayName)`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddApplications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOwner

Specify one or more administrative users who are responsible for this app group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSupportContact

Specify one or more administrative users that end users can contact for help with this application.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddSupportContacts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddUserCategory

Specify one or more user category objects to help you filter and find the app group in the console. To get these objects, use the [Get-CMCategory](Get-CMCategory.md) cmdlet. These categories are of type **CatalogCategories**.

To add categories to help users filter and find applications in Software Center, use the **AddAppCategory** parameter.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddUserCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyToLanguageById

For settings that display in Software Center, use this parameter to specify the language ID for the settings.

This ID is the decimal equivalent of the Windows language ID. For example, `1033` is `0x0409` for **English (United States)**, and `2108` is `0x083C` for **Irish (Ireland)**. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

For example, to add a localized app name for **Irish (Ireland)**:

`-ApplyToLanguageById 2108 -LocalizedName "Fáilte romhat"`

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ApplySettingToSpecificLanguage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanAppCategory

Add this parameter to remove all administrative categories. To remove a single category, use the **RemoveAppCategory** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanAppCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanUserCategory

Add this parameter to remove all user categories. To remove a single category, use the **RemoveUserCategory** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanUserCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearAppCatalog

Add this parameter to remove all localized Software Center entries. To remove a single entry, use the **RemoveAppCatalog** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearAppCatalogs, CleanAppCatalog, CleanAppCatalogs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearOwner

Add this parameter to remove all owners. To remove a single owner, use the **RemoveOwner** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearSupportContact

Add this parameter to remove all support contacts. To remove a single contact, use the **RemoveSupportContact** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanSupportContacts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultLanguageId

Specify the language ID for the default Software Center language.

This ID is the decimal equivalent of the Windows language ID. For example, `1033` is `0x0409` for **English (United States)**, and `2108` is `0x083C` for **Irish (Ireland)**. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

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

### -Description

Specify an optional administrator comment for the app group. The maximum length is 2048 characters.

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

### -IconLocationFile

Specify the path to the file that contains the icon for this app group. Icons can have pixel dimensions of up to 512x512. The file can be of the following image and icon file types:

- DLL
- EXE
- JPG
- ICO
- PNG

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

### -Id

Specify the ID of the app group to configure. This value is the same as the **CI_ID**, for example `1025866`.

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

Specify an app group object to configure. To get this object, use the [Get-CMApplicationGroup](Get-CMApplicationGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: ApplicationGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Keyword

Specify a list of keywords in the selected language. These keywords help Software Center users search for the app group.

> [!TIP]
> To add multiple keywords, use **CultureInfo.CurrentCulture.TextInfo.ListSeparator** as the delimiter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Keywords

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinkText

When you use the **UserDocumentation** parameter, use this parameter to show a string in place of "Additional information" in Software Center. The maximum length is 128 characters.

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

### -LocalizedDescription

Specify a description for this app group in the selected language. The maximum length is 2048 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedAppGroupDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalizedName

Specify the app group name in the selected language. This name appears in Software Center.

A name is required for each language that you add.

The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedAppGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ModelName

Specify the application model identifier of the app group to configure. This value is also known as the **CI Unique ID**. For example, `ScopeId_0D7D8B60-F2F9-484A-B9F3-4A8B68D14D59/ApplicationGroup_047fbf05-55f4-42ab-9581-e63fd0337fed`.

```yaml
Type: String
Parameter Sets: SetByModelName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the app group to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName, ApplicationGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename the app group. The maximum length is 256 characters.

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

### -OptionalReference

Specify an optional string to help you find the app group in the console. The maximum length is 256 characters.

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

### -PrivacyUrl

Specify a website address to the privacy statement for the app group. The format needs to be a valid URL, for example `https://contoso.com/privacy`. The maximum length of the entire string is 128 characters.

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

### -Publisher

Specify optional vendor information for this app group. The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Manufacturer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReleaseDate

Specify a date object for when this app group was released. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveAppCatalog

Specify an array of language IDs to remove the associated Software Center entries. To remove all entries, use the **ClearAppCatalog** parameter.

This ID is the decimal equivalent of the Windows language ID. For example, `1033` is `0x0409` for **English (United States)**, and `2108` is `0x083C` for **Irish (Ireland)**. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

For example, to remove the localized Software Center entry for **Irish (Ireland)**:

`-RemoveAppCatalog 2108`

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: RemoveAppCatalogsByLanguageId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveAppCategoryName

Specify an array of administrative category names to remove. To remove all administrative categories, use the **CleanAppCategory** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveAppCategoryNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveApplication

Specify an array of application names to remove from this group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveApplications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOwner

Specify an array of owners to remove. To remove all owners, use the **ClearOwner** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveOwners

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSupportContact

Specify an array of support contacts to remove. To remove all support contacts, use the **ClearSupportContact** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveSupportContacts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveUserCategoryName

Specify an array of user category names to remove. To remove all user categories, use the **CleanUserCategory** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveUserCategoryNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareVersion

Specify an optional version string for the app group. The maximum length is 64 characters.

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

### -UserDocumentation

Specify the location of a file from which Software Center users can get more information about this app group. This location is a website address, or a network path and file name. Make sure that users have access to this location.

The maximum length of the entire string is 256 characters.

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

### IResultObject#SMS_ApplicationGroup
This cmdlet returns the SMS_ApplicationGroup WMI class object.

## NOTES

## RELATED LINKS

[Get-CMApplicationGroup](Get-CMApplicationGroup.md)
[New-CMApplicationGroup](New-CMApplicationGroup.md)
[Remove-CMApplicationGroup](Remove-CMApplicationGroup.md)

[New-CMApplicationDisplayInfo](New-CMApplicationDisplayInfo.md)

[Get-CMApplicationGroupDeployment](Get-CMApplicationGroupDeployment.md)
[New-CMApplicationGroupDeployment](New-CMApplicationGroupDeployment.md)
[Remove-CMApplicationGroupDeployment](Remove-CMApplicationGroupDeployment.md)
[Set-CMApplicationGroupDeployment](Set-CMApplicationGroupDeployment.md)

[Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups)
