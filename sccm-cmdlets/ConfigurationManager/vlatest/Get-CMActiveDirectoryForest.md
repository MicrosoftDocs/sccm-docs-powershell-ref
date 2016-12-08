---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834061
schema: 2.0.0
ms.assetid: 2626D1D7-FB5C-4563-8694-CD8E19DA371B
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

## EXAMPLES

### Example 1: Get all Active Directory forest objects
```
PS C:\> Get-CMActiveDirectoryForest
```

This command gets all Active Directory forest objects.

### Example 2: Get an Active Directory Forest object by ID
```
PS C:\> Get-CMActiveDirectoryForest -Id "16777217"
```

This command gets an Active Directory forest object that has the ID 16777217.

### Example 3: Get Active Directory Forest by domain name
```
PS C:\> Get-CMActiveDirectoryForest -ForestFqdn "tsqa.contoso.com"
```

This command gets an Active Directory forest object that has the FQDN tsqa.contoso.com.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMActiveDirectoryForest](./New-CMActiveDirectoryForest.md)

[Set-CMActiveDirectoryForest](./Set-CMActiveDirectoryForest.md)

[Remove-CMActiveDirectoryForest](./Remove-CMActiveDirectoryForest.md)


