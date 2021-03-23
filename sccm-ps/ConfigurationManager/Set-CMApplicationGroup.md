---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMApplicationGroup

## SYNOPSIS
{{ Fill in the Synopsis }}

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
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AddAppCatalog
{{ Fill AddAppCatalog Description }}

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
{{ Fill AddAppCategory Description }}

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
{{ Fill AddApplication Description }}

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
{{ Fill AddOwner Description }}

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
{{ Fill AddSupportContact Description }}

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
{{ Fill AddUserCategory Description }}

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
{{ Fill ApplyToLanguageById Description }}

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
{{ Fill CleanAppCategory Description }}

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
{{ Fill CleanUserCategory Description }}

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
{{ Fill ClearAppCatalog Description }}

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
{{ Fill ClearOwner Description }}

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
{{ Fill ClearSupportContact Description }}

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
{{ Fill DefaultLanguageId Description }}

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
{{ Fill Description Description }}

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

### -IconLocationFile
{{ Fill IconLocationFile Description }}

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
{{ Fill Id Description }}

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
{{ Fill InputObject Description }}

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
{{ Fill Keyword Description }}

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
{{ Fill LinkText Description }}

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
{{ Fill LocalizedDescription Description }}

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
{{ Fill LocalizedName Description }}

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
{{ Fill ModelName Description }}

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
{{ Fill Name Description }}

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

### -OptionalReference
{{ Fill OptionalReference Description }}

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

### -PrivacyUrl
{{ Fill PrivacyUrl Description }}

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
{{ Fill Publisher Description }}

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
{{ Fill ReleaseDate Description }}

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
{{ Fill RemoveAppCatalog Description }}

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
{{ Fill RemoveAppCategoryName Description }}

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
{{ Fill RemoveApplication Description }}

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
{{ Fill RemoveOwner Description }}

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
{{ Fill RemoveSupportContact Description }}

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
{{ Fill RemoveUserCategoryName Description }}

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
{{ Fill SoftwareVersion Description }}

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
{{ Fill UserDocumentation Description }}

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

### IResultObject#SMS_ApplicationGroup

## NOTES

## RELATED LINKS
