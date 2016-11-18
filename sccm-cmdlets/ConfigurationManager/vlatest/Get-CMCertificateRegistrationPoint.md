---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 89EBC6C7-BDB2-4AB6-B54D-62361D0B6620
---

# Get-CMCertificateRegistrationPoint

## SYNOPSIS
Gets a certificate registration point.

## SYNTAX

### SearchByName
```
Get-CMCertificateRegistrationPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMCertificateRegistrationPoint -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCertificateRegistrationPoint** cmdlet gets a certificate registration point.

## EXAMPLES

### Example 1: Get a certificate registration point by name
```
PS C:\> Get-CMCertificateRegistrationPoint -SiteCode SC3
```

This command gets the certificate registration point for site code SC3.

### Example 2: Get a certificate registration point by using the pipeline
```
PS C:\> Get-CMSitesystemserver -SiteSystemServerName "SiteServer01.Contoso.com" | Get-CMCertificateRegistrationPoint
```

This command gets the site system server object named SiteServer01.Contoso.com and uses the pipeline operator to pass the object to **Get-CMCertificateRegistrationPoint**, which gets the certificate registration point for the site system server object.

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
Specifies a Configuration Manager site system server object.
To obtain a site system server object, use the Get-CMSiteSystemServer cmdlet.

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
Specifies the site code of a Configuration Manager site system server.

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
Specifies the name of a Configuration Manager site system server.

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

[Add-CMCertificateRegistrationPoint](./Add-CMCertificateRegistrationPoint.md)

[Remove-CMCertificateRegistrationPoint](./Remove-CMCertificateRegistrationPoint.md)

[Set-CMCertificateRegistrationPoint](./Set-CMCertificateRegistrationPoint.md)


