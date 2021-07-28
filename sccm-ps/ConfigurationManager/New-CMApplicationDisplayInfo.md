---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
online version:
schema: 2.0.0
---

# New-CMApplicationDisplayInfo

## SYNOPSIS

Create a Software Center entry for an application or application group.

## SYNTAX

```
New-CMApplicationDisplayInfo [-Description <String>] [-IconLocationFile <String>] [-Keyword <String[]>]
 -LanguageId <Int32> [-LinkText <String>] [-PrivacyUrl <String>] -Title <String> [-UserDocumentation <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a Software Center entry for an application or application group. Specify information about how you want to display this app or app group to users when they browse the Software Center. To provide information in a specific language, specify the language ID.

This cmdlet creates an object that you can pass to the **New-CMApplication**, **New-CMApplicationGroup**, **Set-CMApplication**, and **Set-CMApplicationGroup** cmdlets.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example collects all of the settings for an app group entry in the **Irish** language, and then adds it to the app group.

```powershell
$welcomeAppInfoIrish = New-CMApplicationDisplayInfo -Description "Fáilte a Contoso! Go raibh maith agat faoi theacht chugainn." -IconLocationFile "\\central\icons\welcome.ico" -Keyword "fostaí","nua" -LanguageId 60 -LinkText "Mar eolas duit" -PrivacyUrl "https://contoso.com/privacy" -Title "Fáilte romhat" -UserDocumentation "https://my.contoso.com/welcome"

Set-CMApplicationGroup -Name "Contoso Welcome app" -AddAppCatalog $welcomeAppInfoIrish
```

## PARAMETERS

### -Description

Specify a description for this app in the specified language. The maximum length is 2048 characters.

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

### -IconLocationFile

Specify the path to the file that contains the icon for the app. Icons can have pixel dimensions of up to 512x512. The file can be of the following image and icon file types:

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

### -Keyword

Specify a list of keywords in the specified language. These keywords help Software Center users search for the app.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LanguageId

Use this parameter to specify the language ID for the settings.

This ID is the decimal equivalent of the Windows language ID. For example, `1033` is `0x0409` for **English (United States)**, and `2108` is `0x083C` for **Irish (Ireland)**. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
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

### -Title

Specify the app name in the specified language. This name appears in Software Center. The maximum length is 256 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedName

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### AppDisplayInfo
## NOTES

## RELATED LINKS

[New-CMApplication](New-CMApplication.md)
[Set-CMApplication](Set-CMApplication.md)
[New-CMApplicationGroup](New-CMApplicationGroup.md)
[Set-CMApplicationGroup](Set-CMApplicationGroup.md)
