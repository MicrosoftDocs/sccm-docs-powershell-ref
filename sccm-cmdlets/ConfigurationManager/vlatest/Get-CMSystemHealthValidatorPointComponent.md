---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 28507B76-6E7C-4438-97E4-42BCB4E0E221
---

# Get-CMSystemHealthValidatorPointComponent

## SYNOPSIS
Retrieves an object that represents a system health validator point in Configuration Manager.

## SYNTAX

```
Get-CMSystemHealthValidatorPointComponent [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSystemHealthValidatorPointComponent** cmdlet retrieves an object that represents a system health validator point.
A system health validator point is a site system role that evaluates system health information reported by Windows clients for security related compliance.

## EXAMPLES

### Example 1: Retrieve a system health validator point by site system server name
```
PS C:\>Get-CMSystemHealthValidatorPointComponent -SiteSystemServerName "Shvp-01.TSQA.Corp.Contoso.com"
```

This command retrieves a system health validator point component by using a site system server name.

### Example 2: Retrieve a system health validator point by site code
```
PS C:\>Get-CMSystemHealthValidatorPointComponent -SiteCode "CM4"
```

This command retrieves a system health validator point component by using a site code.

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

### -SiteCode


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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMSystemHealthValidatorPointComponent](./Set-CMSystemHealthValidatorPointComponent.md)


