---
description: Create an application.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
schema: 2.0.0
title: New-CMApplication
---

# New-CMApplication

## SYNOPSIS

Create an application.

## SYNTAX

```
New-CMApplication [-AddOwner <String[]>] [-AddSupportContact <String[]>] [-AppCatalog <AppDisplayInfo[]>]
 [-AutoInstall <Boolean>] [-DefaultLanguageId <Int32>] [-Description <String>]
 [-DisplaySupersedenceInApplicationCatalog <Boolean>] [-IconLocationFile <String>] [-IsFeatured <Boolean>]
 [-Keyword <String[]>] [-LinkText <String>] [-LocalizedDescription <String>] [-LocalizedName <String>]
 [-Name] <String> [-OptionalReference <String>] [-Owner <String>] [-PrivacyUrl <String>] [-Publisher <String>]
 [-ReleaseDate <DateTime>] [-SoftwareVersion <String>] [-SupportContact <String>] [-UserDocumentation <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an application. A Configuration Manager application defines the metadata about application. For more information, see [Create applications in Configuration Manager](/mem/configmgr/apps/deploy-use/create-applications).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create an application

This command creates an application named Application01.

```powershell
New-CMApplication -Name "Application01" -Description "New Application" -Publisher "Contoso" -SoftwareVersion "1.0.0.1" -OptionalReference "Reference" -ReleaseDate 2/24/2016 -AutoInstall $True -Owner "Administrator" -SupportContact "Administrator" -LocalizedName "Application01" -UserDocumentation "https://contoso.com/content" -LinkText "For more information" -LocalizedDescription "New Localized Application" -Keyword "application" -PrivacyUrl "https://contoso.com/library/privacy" -IsFeatured $True -IconLocationFile "\\central\icons\icon.png"
```

## PARAMETERS

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

### -AppCatalog

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

Don't use this parameter. The application catalog is no longer supported.

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

Specify a list of keywords in the selected language. These keywords help Software Center users search for the app.

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

### -LocalizedName

Specify the app name in the selected language. This name appears in Software Center.

A name is required for each language that you add.

The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedApplicationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a name for the app. The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: 0
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

### None
## OUTPUTS

### IResultObject#SMS_ApplicationLatest
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

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Set-CMApplication](Set-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)

[New-CMApplicationDisplayInfo](New-CMApplicationDisplayInfo.md)

[Create applications in Configuration Manager](/mem/configmgr/apps/deploy-use/create-applications)
