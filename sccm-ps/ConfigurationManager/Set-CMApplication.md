---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: 0FF11819-7D5A-499F-9E7C-E332117BE0E6
online version: https://go.microsoft.com/fwlink/?linkid=833628
schema: 2.0.0
---

# Set-CMApplication

## SYNOPSIS
Sets the properties of an application.

## SYNTAX

### SetByValue (Default)
```
Set-CMApplication [-InputObject] <IResultObject> [-Description <String>] [-Publisher <String>]
 [-SoftwareVersion <String>] [-NewName <String>] [-OptionalReference <String>] [-ReleaseDate <DateTime>]
 [-AutoInstall <Boolean>] [-Owner <String>] [-AddOwner <String[]>] [-RemoveOwner <String[]>] [-ClearOwner]
 [-SupportContact <String>] [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>]
 [-ClearSupportContact] [-LocalizedApplicationName <String>] [-UserDocumentation <String>] [-LinkText <String>]
 [-LocalizedDescription <String>] [-Keyword <String>] [-DistributionPriority <DistributionPriorityType>]
 [-SendToProtectedDistributionPoint <Boolean>] [-DistributionPointSetting <DistributionPointSettingType>]
 [-UserCategory <String[]>] [-AppCategory <String[]>] [-AddAppCategory <IResultObject>] 
 [-AddUserCategory <IResultObject>] [-CleanAppCategory] [-CleanUserCategory] [-PrivacyUrl <String>] 
 [-IsFeatured <Boolean>] [-IconLocationFile <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>] 
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMApplication [-Id] <Int32> [-Description <String>] [-Publisher <String>] [-SoftwareVersion <String>]
 [-NewName <String>] [-OptionalReference <String>] [-ReleaseDate <DateTime>] [-AutoInstall <Boolean>]
 [-Owner <String>] [-AddOwner <String[]>] [-RemoveOwner <String[]>] [-ClearOwner] [-SupportContact <String>]
 [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>] [-ClearSupportContact]
 [-LocalizedApplicationName <String>] [-UserDocumentation <String>] [-LinkText <String>]
 [-LocalizedDescription <String>] [-Keyword <String>] [-DistributionPriority <DistributionPriorityType>]
 [-SendToProtectedDistributionPoint <Boolean>] [-DistributionPointSetting <DistributionPointSettingType>]
 [-UserCategory <String[]>] [-AppCategory <String[]>] [-AddAppCategory <IResultObject>] 
 [-AddUserCategory <IResultObject>] [-CleanAppCategory] [-CleanUserCategory] [-PrivacyUrl <String>] 
 [-IsFeatured <Boolean>] [-IconLocationFile <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>] 
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMApplication [-Name] <String> [-Description <String>] [-Publisher <String>] [-SoftwareVersion <String>]
 [-NewName <String>] [-OptionalReference <String>] [-ReleaseDate <DateTime>] [-AutoInstall <Boolean>]
 [-Owner <String>] [-AddOwner <String[]>] [-RemoveOwner <String[]>] [-ClearOwner] [-SupportContact <String>]
 [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>] [-ClearSupportContact]
 [-LocalizedApplicationName <String>] [-UserDocumentation <String>] [-LinkText <String>]
 [-LocalizedDescription <String>] [-Keyword <String>] [-DistributionPriority <DistributionPriorityType>]
 [-SendToProtectedDistributionPoint <Boolean>] [-DistributionPointSetting <DistributionPointSettingType>]
 [-UserCategory <String[]>] [-AppCategory <String[]>] [-AddAppCategory <IResultObject>] 
 [-AddUserCategory <IResultObject>] [-CleanAppCategory] [-CleanUserCategory] [-PrivacyUrl <String>] 
 [-IsFeatured <Boolean>] [-IconLocationFile <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>] 
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByModelName
```
Set-CMApplication -ModelName <String> [-Description <String>] [-Publisher <String>] [-SoftwareVersion <String>]
 [-NewName <String>] [-OptionalReference <String>] [-ReleaseDate <DateTime>] [-AutoInstall <Boolean>]
 [-Owner <String>] [-AddOwner <String[]>] [-RemoveOwner <String[]>] [-ClearOwner] [-SupportContact <String>]
 [-AddSupportContact <String[]>] [-RemoveSupportContact <String[]>] [-ClearSupportContact]
 [-LocalizedApplicationName <String>] [-UserDocumentation <String>] [-LinkText <String>]
 [-LocalizedDescription <String>] [-Keyword <String>] [-DistributionPriority <DistributionPriorityType>]
 [-SendToProtectedDistributionPoint <Boolean>] [-DistributionPointSetting <DistributionPointSettingType>]
 [-UserCategory <String[]>] [-AppCategory <String[]>] [-AddAppCategory <IResultObject>] [-AddUserCategory <IResultObject>]
 [-CleanAppCategory] [-CleanUserCategory] [-PrivacyUrl <String>] [-IsFeatured <Boolean>] [-IconLocationFile <String>] 
 [-DisplaySupersedenceInApplicationCatalog <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] 
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMApplication** cmdlet changes the settings of an application.

## EXAMPLES

### Example 1: Set the properties of an application by using the pipeline
```
PS C:\> Get-CMApplication -Name "Application01" | Set-CMApplication -NewName "Application01_New" -Description "Application updated" -Publisher "Test group" -SoftwareVersion 1.0.0.1 -OptionalReference "Reference" -ReleaseDate 2/24/2016 -AutoInstall $True -Owner "Administrator1" -SupportContact "Administrator" -LocalizedApplicationName "Localized Application01" -UserDocumentation "https://contoso.com/content" -LinkText "Linktext" -LocalizedDescription "Localized Application New" -Keyword "Application" -PrivacyUrl "https://contoso.com/privacy" -IsFeatured $True -IconLocationFile "C:\Users\art\icon.png" -DisplaySupersedenceInApplicationCatalog $True -DistributionPriority Medium -SendToProtectedDistributionPoint $True -DistributionPointSetting NoDownload -UserCategory "userCategory1","userCategory2" -AppCategory "adminCategory1","adminCategory2"
```

The first command gets the application object named Application01 and uses the pipeline operator to pass the object to **Set-CMApplication**.
**Set-CMApplication** sets the specified properties on Applicaton01.

### Example 2: Get an application, rename it, and update its settings
```
PS C:\> Set-CMApplication -Name "Application01" -NewName "Application01_New" -Description "Application updated" -Publisher "Test group" -SoftwareVersion 1.0.0.1 -OptionalReference "Reference" -ReleaseDate 2/24/2016 -AutoInstall $True -Owner "Administrator1" -SupportContact "Administrator" -LocalizedApplicationName Localized "Application01" -UserDocumentation "https://contoso.com/content" -LinkText "LinkText" -LocalizedDescription "Localized Application New" -Keyword "Application" -PrivacyUrl "https://contoso.com/privacy" -IsFeatured $True -IconLocationFile "C:\Users\art\icon.png" -DisplaySupersedenceInApplicationCatalog $True -DistributionPriority Medium -SendToProtectedDistributionPoint $True -DistributionPointSetting NoDownload -UserCategory "userCategory1","userCategory2" -AppCategory "adminCategory1","adminCategory2"
```

This command gets the application named Application01, renames it to Application01_New, and sets the specified properties on the application.

## PARAMETERS

### -AddOwner
 

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

### -AppCategory
This cmdlet is deprecated in 1802. See -AddAppCategory for more information.
Specifies an array of administrative categories assigned to the application.
Provide the categories by their name.
Only categories of the type AppCategories are supported.

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

### -AddAppCategory
Specifies an administrative category assigned to the application.
Provide the category by its name.
Only categories of the type AppCategories are supported.

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

### -AddUserCategory
Specifies a user category assigned to the application for Software Center filtering use.
Provide the category by its name.
Only categories of the type CatalogCategories are supported.

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

### -AutoInstall
Indicates whether a task sequence action can install the application.

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

### -CleanUserCategory


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

### -ClearOwner
 

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

### -Description
Specifies a description for the application.
The description appears in the Configuration Manager console

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

### -DisplaySupersedenceInApplicationCatalog
Indicates whether the application displays supersedence in the Application Catalog.

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
Specifies the prestaged distribution point settings.
Valid values are: 

- AutoDownload.
Automatically download content when packages are assigned to distribution points.
 
- DeltaCopy.
Download only content changes to distribution points.
 
- NoDownload.
Manually copy the content in this package to distribution points.

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
Specifies the order in which packages are sent to other sites.
Valid values are:

- High
- Medium
- Low

High priority packages are sent before packages with medium or low priority.
Packages with equal priority are sent in the order in which they are created.

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

### -IconLocationFile
Specifies the location of the icon file.
This is set to the single default language.

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
Specifies the CI_ID and ModelID properties (the same value) of an application.

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
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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
Indicates whether the application displays as a featured app and is highlighted in the company portal.

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
Specifies a keyword for the application.
Provide the keyword in the default language.
To add multiple keywords, use CultureInfo.CurrentCulture.TextInfo.ListSeparator as the delimiter.

This keyword will help users of Software Center search for the application.

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

### -LinkText
Specifies a description that appears in the Application Catalog with a hyperlink to additional information or documentation for the application.
This is set to the single default language.

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
Specifies a localized name string that appears in the client software center or catalog web site.

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
Specifies a localized description string that appears in the client software center or catalog web site.
This is set to the single default language.

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
Specifies the model name of the application.

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
Specifies the name of the application.

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
Specifies a new name for the application.

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
Specifies optional reference information for this application.

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
Specifies an owner for the application.

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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
Specifies a hyperlink, in URI format, to privacy information about the application.
This is set to the single default language.

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
Specifies the name of a software publisher.

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
Specifies a release date for the application.

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

### -RemoveOwner
 

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
Specifies a software version for an application.

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
Specifies one or more administrative users who are support contacts for the application.

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
This cmdlet is deprecated in 1802. See -AddUserCategory for more information. 
Specifies an array of user categories assigned to the application.
You can use this parameter to identify a group or category of software, such as "office productivity" or "graphics."

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
Specifies a hyperlink, in URI format, to additional information about the application.
This is set to the single default language.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

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


