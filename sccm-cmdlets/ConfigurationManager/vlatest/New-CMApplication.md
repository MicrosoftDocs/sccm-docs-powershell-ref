---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834248
schema: 2.0.0
ms.assetid: 523AADB5-3AAE-410A-AFCA-5B3C56138653
---

# New-CMApplication

## SYNOPSIS
Creates an application.

## SYNTAX

```
New-CMApplication [-Name] <String> [-Description <String>] [-Publisher <String>] [-SoftwareVersion <String>]
 [-OptionalReference <String>] [-ReleaseDate <DateTime>] [-AutoInstall <Boolean>] [-Owner <String>]
 [-SupportContact <String>] [-LocalizedName <String>] [-UserDocumentation <String>] [-LinkText <String>]
 [-LocalizedDescription <String>] [-Keyword <String>] [-PrivacyUrl <String>] [-IsFeatured <Boolean>]
 [-IconLocationFile <String>] [-DisplaySupersedenceInApplicationCatalog <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMApplication** cmdlet creates an application in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Create an application
```
PS C:\> New-CMApplication -Name "Application01" -Description "New Application" -Publisher "Contoso" -SoftwareVersion 1.0.0.1 -OptionalReference "Reference" -ReleaseDate 2/24/2016 -AutoInstall $True -Owner "Administrator" -SupportContact "Administrator" -LocalizedName "Application01" -UserDocumentation "https://contoso.com/content" -LinkText "For more information, see https://contoso.com/content" -LocalizedDescription "New Localized Application" -Keyword "application" -PrivacyUrl "https://contoso.com/library/privacy" -IsFeatured $True -IconLocationFile "C:\Users\administrator\Desktop\icon.png" -DisplaySupersedenceInApplicationCatalog $True
```

This command creates an application named Application01.

## PARAMETERS

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
The description appears in the Configuration Manager console.

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
Indicates that wildcard handling is disabled.

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

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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

### -LocalizedName
Specifies a localized name string that appears in the client software center or catalog web site.
This is set to the single default language.

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
Specifies a name for the application.

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
Specifies optional reference information for the application.

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
Specifies the name of the software publisher.

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

### -SoftwareVersion
Specifies a software version for the application.

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

[Convert-CMApplication](./Convert-CMApplication.md)

[ConvertFrom-CMApplication](./ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](./ConvertTo-CMApplication.md)

[Export-CMApplication](./Export-CMApplication.md)

[Get-CMApplication](./Get-CMApplication.md)

[Import-CMApplication](./Import-CMApplication.md)

[Remove-CMApplication](./Remove-CMApplication.md)

[Resume-CMApplication](./Resume-CMApplication.md)

[Set-CMApplication](./Set-CMApplication.md)

[Suspend-CMApplication](./Suspend-CMApplication.md)


