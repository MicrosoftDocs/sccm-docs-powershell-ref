---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 46449F73-D5C2-440E-A775-5C2A01F9C1B3
online version: https://go.microsoft.com/fwlink/?linkid=833887
schema: 2.0.0
---

# Get-CMSoftwareDistributionComponent

## SYNOPSIS
Gets an object that represents a software distribution component in Configuration Manager.

## SYNTAX

```
Get-CMSoftwareDistributionComponent [-SiteCode <String>] [-SiteSystemServerName <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareDistributionComponent** cmdlet gets an object that represents a software distribution component in Microsoft System Center Configuration Manager.
A software distribution component consists of individual components such as the client software distribution component.

## EXAMPLES

### Example 1: Get a software distribution component
```
PS C:\> Get-CMSoftwareDistributionComponent -Name "CM2"
```

This command gets the software distribution component.

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
Type: String[]
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

[Set-CMSoftwareDistributionComponent](./Set-CMSoftwareDistributionComponent.md)


