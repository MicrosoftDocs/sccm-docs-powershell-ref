---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833689
schema: 2.0.0
ms.assetid: A635E162-B777-4289-B6EE-B8BF2F9EC302
---

# Get-CMEnrollmentPoint

## SYNOPSIS
Gets an enrollment point.

## SYNTAX

### SearchByName
```
Get-CMEnrollmentPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMEnrollmentPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMEnrollmentPoint** cmdlet gets an enrollment point in Microsoft System Center Configuration Manager.
An enrollment point is a site system role that uses public key infrastructure (PKI) certificates to complete mobile device enrollment and to provision Intel AMT-based computers.

## EXAMPLES

### Example 1: Get an enrollment point
```
PS C:\>Get-CMEnrollmentPoint -SiteSystemServerName "SiteServer01.Contoso.com" -SiteCode "CM1"
```

This command gets an enrollment point.

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

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: False
Position: 0
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

[Add-CMEnrollmentPoint](./Add-CMEnrollmentPoint.md)

[Remove-CMEnrollmentPoint](./Remove-CMEnrollmentPoint.md)

[Set-CMEnrollmentPoint](./Set-CMEnrollmentPoint.md)


