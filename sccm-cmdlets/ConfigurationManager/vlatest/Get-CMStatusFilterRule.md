---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833936
schema: 2.0.0
ms.assetid: 9A9F77DF-FAA9-438A-AB3F-B72A9AD98016
---

# Get-CMStatusFilterRule

## SYNOPSIS
Gets Configuration Manager filter rules for status messages.

## SYNTAX

```
Get-CMStatusFilterRule [-SiteCode <String>] [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMStatusFilterRule** cmdlet gets filter rules for Microsoft System Center Configuration Manager status messages.
You can get all the rules for a System Center Configuration Manager site or you can specify a name of a rule within a site.

Status filter rules specify how System Center Configuration Manager responds to status messages.
Each filter rule contains criteria and actions for status messages.
You configure status filter rules for each site, not across all sites.

## EXAMPLES

### Example 1: Get rules for a specified site
```
PS C:\> Get-CMStatusFilterRule -SiteCode "CM1"
```

This cmdlet gets status filter rules for the site that has the site code CM1.

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

### -Name
Specifies a name of a rule.

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

### -SiteCode
Specifies a site code for the Configuration Manager site.

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

[Disable-CMStatusFilterRule](./Disable-CMStatusFilterRule.md)

[Enable-CMStatusFilterRule](./Enable-CMStatusFilterRule.md)

[New-CMStatusFilterRule](./New-CMStatusFilterRule.md)

[Remove-CMStatusFilterRule](./Remove-CMStatusFilterRule.md)

[Set-CMStatusFilterRule](./Set-CMStatusFilterRule.md)


