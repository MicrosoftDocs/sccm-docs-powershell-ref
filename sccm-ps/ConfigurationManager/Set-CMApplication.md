---
description: Configure the properties of an application.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
schema: 2.0.0
title: Set-CMApplication
---

# Set-CMApplication

## SYNOPSIS

Configure the properties of an application.

## SYNTAX

### SetByValue (Default)
```
Set-CMApplication [-AddAppCatalog <AppDisplayInfo[]>] [-AddAppCategory <IResultObject[]>]
 [-AddOwner <String[]>] [-AddSupportContact <String[]>] [-AddUserCategory <IResultObject[]>]
 [-AppCategory <String[]>] [-ApplyToLanguageById <Int32>] [-AutoInstall <Boolean>] [-CleanAppCategory]
 [-CleanUserCategory] [-ClearAppCatalog] [-ClearOwner] [-ClearSupportContact] [-DefaultLanguageId <Int32>]
 [-Description <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>]
 [-DistributionPointSetting <DistributionPointSettingType>] [-DistributionPriority <DistributionPriorityType>]
 [-IconLocationFile <String>] [-InputObject] <IResultObject> [-IsFeatured <Boolean>] [-Keyword <String[]>]
 [-LinkText <String>] [-LocalizedApplicationName <String>] [-LocalizedDescription <String>] [-NewName <String>]
 [-OptionalReference <String>] [-Owner <String>] [-PassThru] [-PrivacyUrl <String>] [-Publisher <String>]
 [-ReleaseDate <DateTime>] [-RemoveAppCatalog <Int32[]>] [-RemoveAppCategoryName <String[]>]
 [-RemoveOwner <String[]>] [-RemoveSupportContact <String[]>] [-RemoveUserCategoryName <String[]>]
 [-SendToProtectedDistributionPoint <Boolean>] [-SoftwareVersion <String>] [-SupportContact <String>]
 [-UserCategory <String[]>] [-UserDocumentation <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMApplication [-AddAppCatalog <AppDisplayInfo[]>] [-AddAppCategory <IResultObject[]>]
 [-AddOwner <String[]>] [-AddSupportContact <String[]>] [-AddUserCategory <IResultObject[]>]
 [-AppCategory <String[]>] [-ApplyToLanguageById <Int32>] [-AutoInstall <Boolean>] [-CleanAppCategory]
 [-CleanUserCategory] [-ClearAppCatalog] [-ClearOwner] [-ClearSupportContact] [-DefaultLanguageId <Int32>]
 [-Description <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>]
 [-DistributionPointSetting <DistributionPointSettingType>] [-DistributionPriority <DistributionPriorityType>]
 [-IconLocationFile <String>] [-Id] <Int32> [-IsFeatured <Boolean>] [-Keyword <String[]>] [-LinkText <String>]
 [-LocalizedApplicationName <String>] [-LocalizedDescription <String>] [-NewName <String>]
 [-OptionalReference <String>] [-Owner <String>] [-PassThru] [-PrivacyUrl <String>] [-Publisher <String>]
 [-ReleaseDate <DateTime>] [-RemoveAppCatalog <Int32[]>] [-RemoveAppCategoryName <String[]>]
 [-RemoveOwner <String[]>] [-RemoveSupportContact <String[]>] [-RemoveUserCategoryName <String[]>]
 [-SendToProtectedDistributionPoint <Boolean>] [-SoftwareVersion <String>] [-SupportContact <String>]
 [-UserCategory <String[]>] [-UserDocumentation <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByModelName
```
Set-CMApplication [-AddAppCatalog <AppDisplayInfo[]>] [-AddAppCategory <IResultObject[]>]
 [-AddOwner <String[]>] [-AddSupportContact <String[]>] [-AddUserCategory <IResultObject[]>]
 [-AppCategory <String[]>] [-ApplyToLanguageById <Int32>] [-AutoInstall <Boolean>] [-CleanAppCategory]
 [-CleanUserCategory] [-ClearAppCatalog] [-ClearOwner] [-ClearSupportContact] [-DefaultLanguageId <Int32>]
 [-Description <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>]
 [-DistributionPointSetting <DistributionPointSettingType>] [-DistributionPriority <DistributionPriorityType>]
 [-IconLocationFile <String>] [-IsFeatured <Boolean>] [-Keyword <String[]>] [-LinkText <String>]
 [-LocalizedApplicationName <String>] [-LocalizedDescription <String>] -ModelName <String> [-NewName <String>]
 [-OptionalReference <String>] [-Owner <String>] [-PassThru] [-PrivacyUrl <String>] [-Publisher <String>]
 [-ReleaseDate <DateTime>] [-RemoveAppCatalog <Int32[]>] [-RemoveAppCategoryName <String[]>]
 [-RemoveOwner <String[]>] [-RemoveSupportContact <String[]>] [-RemoveUserCategoryName <String[]>]
 [-SendToProtectedDistributionPoint <Boolean>] [-SoftwareVersion <String>] [-SupportContact <String>]
 [-UserCategory <String[]>] [-UserDocumentation <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMApplication [-AddAppCatalog <AppDisplayInfo[]>] [-AddAppCategory <IResultObject[]>]
 [-AddOwner <String[]>] [-AddSupportContact <String[]>] [-AddUserCategory <IResultObject[]>]
 [-AppCategory <String[]>] [-ApplyToLanguageById <Int32>] [-AutoInstall <Boolean>] [-CleanAppCategory]
 [-CleanUserCategory] [-ClearAppCatalog] [-ClearOwner] [-ClearSupportContact] [-DefaultLanguageId <Int32>]
 [-Description <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>]
 [-DistributionPointSetting <DistributionPointSettingType>] [-DistributionPriority <DistributionPriorityType>]
 [-IconLocationFile <String>] [-IsFeatured <Boolean>] [-Keyword <String[]>] [-LinkText <String>]
 [-LocalizedApplicationName <String>] [-LocalizedDescription <String>] [-Name] <String> [-NewName <String>]
 [-OptionalReference <String>] [-Owner <String>] [-PassThru] [-PrivacyUrl <String>] [-Publisher <String>]
 [-ReleaseDate <DateTime>] [-RemoveAppCatalog <Int32[]>] [-RemoveAppCategoryName <String[]>]
 [-RemoveOwner <String[]>] [-RemoveSupportContact <String[]>] [-RemoveUserCategoryName <String[]>]
 [-SendToProtectedDistributionPoint <Boolean>] [-SoftwareVersion <String>] [-SupportContact <String>]
 [-UserCategory <String[]>] [-UserDocumentation <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the **Set-CMApplication** cmdlet to configure the settings of an application.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Reconfigure the properties of an application

The first command gets the application object named **Application01**. The next two commands use the **Get-CMCategory** cmdlet to get objects for a user and administrator category. The **Set-CMApplication** cmdlet then sets the specified properties on **Applicaton01**.

```powershell
$app = Get-CMApplication -Name "Application01"
$userCat = Get-CMCategory -Name "Test Applications" -CategoryType CatalogCategories
$adminCat = Get-CMCategory -Name "Testing" -CategoryType AppCategories

Set-CMApplication -InputObject $app -NewName "Application01_New" -Description "Application updated" -Publisher "Test group" -SoftwareVersion "1.0.0.1" -OptionalReference "Reference" -ReleaseDate 2/24/2016 -AutoInstall $True -Owner "jqpublic" -SupportContact "jqpublic" -LocalizedApplicationName "Localized Application01" -UserDocumentation "https://contoso.com/content" -LinkText "For more info" -LocalizedDescription "Localized Application New" -Keyword "Application" -PrivacyUrl "https://contoso.com/privacy" -IsFeatured $True -IconLocationFile "C:\Users\art\icon.png" -DistributionPriority Medium -SendToProtectedDistributionPoint $True -DistributionPointSetting NoDownload -AddUserCategory $userCat -AddAppCategory $adminCat
```

## PARAMETERS

### -AddAppCatalog

Use this parameter to specify a Software Center entry for a specific language. This entry can include all of the localized information about the app:

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

Specify one or more administrative category objects to help you filter and find the app in the console. To get these objects, use the [Get-CMCategory](Get-CMCategory.md) cmdlet. These categories are of type **AppCategories**.

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

### -AddOwner

Specify one or more administrative users who are responsible for this app.

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

### -AppCategory

This parameter is deprecated, use **-AddAppCategory**.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AppCategories

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

### -AutoInstall

Set this parameter to **$true** to allow the app to be installed from the Install Application task sequence step without being deployed.

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

Specify an optional administrator comment for the app. The maximum length is 2048 characters.

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

### -DisplaySupersedenceInApplicationCatalog

While the application catalog is no longer supported, you can still use this parameter to allow users to see in Software Center deployments for this application and all applications that it supersedes.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DisplaySupersedencesInApplicationCatalog

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointSetting

Specify the prestaged distribution point settings:

- `AutoDownload`: Automatically download content when packages are assigned to distribution points.

- `DeltaCopy`: Download only content changes to distribution points.

- `NoDownload`: Manually copy the content in this package to distribution points.

```yaml
Type: DistributionPointSettingType
Parameter Sets: (All)
Aliases:
Accepted values: AutoDownload, DeltaCopy, NoDownload

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPriority

Specify the order in which the site sends the content to other sites and the distribution points in this site.

The site sends high priority content before content with medium or low priority. Content with equal priority are sent in the order in which they're created.

```yaml
Type: DistributionPriorityType
Parameter Sets: (All)
Aliases:
Accepted values: High, Medium, Low

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

Specify the path to the file that contains the icon for this app. Icons can have pixel dimensions of up to 512x512. The file can be of the following image and icon file types:

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

Specify the ID of the app to configure. This value is the same as the **CI_ID**, for example `1025866`.

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

Specify an app object to configure. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: Application

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsFeatured

Set this parameter to **$true** to display this application as a featured app and highlight it in the Company Portal.

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

### -LocalizedApplicationName

Specify the app name in the selected language. This name appears in Software Center.

A name is required for each language that you add.

The maximum length is 256 characters.

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

Specify a description for this app in the selected language. The maximum length is 2048 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedApplicationDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ModelName

Specify the application model identifier of the app to configure. This value is also known as the **CI Unique ID**. For example, `ScopeId_0D7D8B60-F2F9-484A-B9F3-4A8B68D14D59/ApplicationGroup_047fbf05-55f4-42ab-9581-e63fd0337fed`.

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

Specify the name of the app to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName, ApplicationName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename the app. The maximum length is 256 characters.

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

Specify an optional string to help you find the app in the console. The maximum length is 256 characters.

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

### -Owner

Specify an administrative user who's responsible for this app.

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

Specify a website address to the privacy statement for the app. The format needs to be a valid URL, for example `https://contoso.com/privacy`. The maximum length of the entire string is 128 characters.

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

Specify optional vendor information for this app. The maximum length is 256 characters.

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

Specify a date object for when this app was released. To get this object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) built-in cmdlet.

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

### -SendToProtectedDistributionPoint
Indicates whether to copy this application to protected distribution points.

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

### -SoftwareVersion

Specify an optional version string for the app. The maximum length is 64 characters.

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

### -SupportContact

Specify an administrative user that end users can contact for help with this application.

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

### -UserCategory

This parameter is deprecated, use **-AddUserCategory**.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: UserCategories

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDocumentation

Specify the location of a file from which Software Center users can get more information about this app. This location is a website address, or a network path and file name. Make sure that users have access to this location.

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

### IResultObject#SMS_Application
## NOTES

For more information on this return object and its properties, see [SMS_Application server WMI class](/mem/configmgr/develop/reference/apps/sms_application-server-wmi-class).

## RELATED LINKS

[Convert-CMApplication](Convert-CMApplication.md)

[ConvertFrom-CMApplication](ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](ConvertTo-CMApplication.md)

[Export-CMApplication](Export-CMApplication.md)

[Get-CMApplication](Get-CMApplication.md)

[Import-CMApplication](Import-CMApplication.md)

[New-CMApplication](New-CMApplication.md)

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)

[New-CMApplicationDisplayInfo](New-CMApplicationDisplayInfo.md)

[Create applications in Configuration Manager](/mem/configmgr/apps/deploy-use/create-applications)
