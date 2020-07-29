---
external help file: AdminUI.PS.Sum.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMThirdPartyUpdateCatalog

## SYNOPSIS

Use this cmdlet to create a new third-party updates catalog.

## SYNTAX

```
New-CMThirdPartyUpdateCatalog [-DownloadUrl] <Uri> [-PublisherName] <String> [-Name] <String>
 [-Description] <String> [[-SupportUrl] <Uri>] [[-SupportContact] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1910, use this cmdlet to create a new third-party updates catalog.

## EXAMPLES

### Example 1: Create a third-party update catalog

```powershell
New-CMThirdPartyUpdateCatalog -DownloadUrl $downloadUrl -PublisherName $publisher -Name $name -Description $description -SupportUrl $supportUrl -SupportContact $supportContact
```

## PARAMETERS

### -Description

Specify a description for the third-party update catalog. The maximum length is 200 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

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

### -DownloadUrl

Specify a valid HTTPS URL for the site to download the third-party update catalog.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

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

### -Name

Specify a name for the third-party update catalog. The maximum length is 200 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CatalogName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublisherName

Specify the publisher name of the third-party update catalog. The maximum length is 200 characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportContact

Specify the support contact for the third-party update catalog.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportUrl

Specify the support URL for the third-party update catalog.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_ISVCatalogs

## NOTES

## RELATED LINKS
