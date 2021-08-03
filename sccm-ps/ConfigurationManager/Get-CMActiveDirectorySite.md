---
description: Gets Configuration Manager sites that publish data to AD DS.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Get-CMActiveDirectorySite
---

# Get-CMActiveDirectorySite

## SYNOPSIS
Gets Configuration Manager sites that publish data to AD DS.

## SYNTAX

### SearchByName (Default)
```
Get-CMActiveDirectorySite [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByForestName
```
Get-CMActiveDirectorySite -ForestFqdn <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByForestId
```
Get-CMActiveDirectorySite -ForestId <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMActiveDirectorySite -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMActiveDirectorySite** cmdlet gets one or more Configuration Manager sites that are configured to publish site information to Active Directory� Domain Services (AD DS).
You can get Configuration Manager sites that publish site data to AD DS by using an identifier or a fully qualified domain name (FQDN).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an Active Directory site
```
PS XYZ:\> Get-CMActiveDirectorySite
```

This command gets the Active Directory sites that are configured to publish site information.

## PARAMETERS

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

### -ForestFqdn
Specifies an array of fully qualified domain names that identify Active Directory forests.
The FQDN provides a path to an Active Directory forest.

```yaml
Type: String[]
Parameter Sets: SearchByForestName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForestId
Specifies an array of IDs that identify Active Directory forests.

```yaml
Type: String[]
Parameter Sets: SearchByForestId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies an array of identifiers of Active Directory forest objects that contain Active Directory sites.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: SiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of FQDNs of Active Directory forest objects that contain Active Directory sites.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ADSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_ADSite
### IResultObject#SMS_ADSite
## NOTES

## RELATED LINKS

[Get-CMActiveDirectoryForest](Get-CMActiveDirectoryForest.md)
