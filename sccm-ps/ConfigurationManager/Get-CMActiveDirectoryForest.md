---
description: Gets one or more Active Directory forest objects.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/01/2019
schema: 2.0.0
title: Get-CMActiveDirectoryForest
---

# Get-CMActiveDirectoryForest

## SYNOPSIS
Gets one or more Active Directory forest objects.

## SYNTAX

### SearchByFQDN (Default)
```
Get-CMActiveDirectoryForest [-ForestFqdn <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMActiveDirectoryForest -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMActiveDirectoryForest** cmdlet gets one or more Active Directory forest objects in Microsoft System Center Configuration Manager.
You can get an Active Directory forest object by ID or fully qualified domain name (FQDN).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get all Active Directory forest objects
```
PS XYZ:\> Get-CMActiveDirectoryForest
```

This command gets all Active Directory forest objects.

### Example 2: Get an Active Directory Forest object by ID
```
PS XYZ:\> Get-CMActiveDirectoryForest -Id "16777217"
```

This command gets an Active Directory forest object that has the ID 16777217.

### Example 3: Get Active Directory Forest by domain name
```
PS XYZ:\> Get-CMActiveDirectoryForest -ForestFqdn "tsqa.contoso.com"
```

This command gets an Active Directory forest object that has the FQDN tsqa.contoso.com.

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

### -ForestFqdn
Specifies the FQDN of a Configuration Manager object.

```yaml
Type: String
Parameter Sets: SearchByFQDN
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies an array of IDs of Configuration Manager objects.
You can find the identifier value in the **ForestID** property of an Active Directory forest.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: ForestId

Required: True
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

### IResultObject[]#SMS_ADForest

### IResultObject#SMS_ADForest

## NOTES

## RELATED LINKS

[New-CMActiveDirectoryForest](New-CMActiveDirectoryForest.md)

[Set-CMActiveDirectoryForest](Set-CMActiveDirectoryForest.md)

[Remove-CMActiveDirectoryForest](Remove-CMActiveDirectoryForest.md)


