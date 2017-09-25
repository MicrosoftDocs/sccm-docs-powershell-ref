---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: D8EA1510-9DA9-4DE1-BCBB-D5AA2D737E58
online version: https://go.microsoft.com/fwlink/?linkid=833944
schema: 2.0.0
---

# Get-CMStatusReportingComponent

## SYNOPSIS
Gets an object representing a status reporting component.

## SYNTAX

```
Get-CMStatusReportingComponent [-SiteSystemServerName <String>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMStatusReportingComponent** cmdlet gets an object that represents the status reporting component.
This object provides information about the client configuration and server configuration components.

## EXAMPLES

### Example 1: Get status reporting components
```
PS C:\> Get-CMStatusReportingComponent -SiteCode "CM1"
```

This command gets the status reporting components that Set-CMStatusReportingComponent configures for the site.

## PARAMETERS

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

### -SiteCode
Specifies a site code of a Configuration Manager site.

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

### -SiteSystemServerName
Specifies an array of site system server names.

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

[Set-CMStatusReportingComponent](Set-CMStatusReportingComponent.md)


