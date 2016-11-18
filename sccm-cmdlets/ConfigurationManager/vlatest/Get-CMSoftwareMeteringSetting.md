---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 9DD38462-DD7F-42F1-956D-43142B02AA7D
---

# Get-CMSoftwareMeteringSetting

## SYNOPSIS
Gets Configuration Manager software metering settings.

## SYNTAX

```
Get-CMSoftwareMeteringSetting [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareMeteringSetting** cmdlet gets a software metering settings object in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get software metering setting object
```
PS C:\>Get-CMSoftwareMeteringSetting

ClientComponentName : Software Metering Agent
FileType            : 2
Flags               : 1
ItemName            : Software Metering Agent
ItemType            : Client Component
PropLists           : 
Props               : 
RegMultiStringLists : 
SiteCode            : CM1
```

This command gets a software metering setting object.

## PARAMETERS

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSoftwareMeteringSetting](./Set-CMSoftwareMeteringSetting.md)


