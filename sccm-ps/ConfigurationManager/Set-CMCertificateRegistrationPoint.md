---
description: Sets a certificate registration point role on a site system server.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMCertificateRegistrationPoint
---

# Set-CMCertificateRegistrationPoint

## SYNOPSIS
Sets a certificate registration point role on a site system server.

## SYNTAX

### SetByValue (Default)
```
Set-CMCertificateRegistrationPoint [-AddCertificate <Hashtable>] [-ConnectionAccountUserName <String>]
 -InputObject <IResultObject> [-PassThru] [-Port <Int32>] [-RemoveCertificate <String[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCertificateRegistrationPoint [-AddCertificate <Hashtable>] [-ConnectionAccountUserName <String>]
 [-PassThru] [-Port <Int32>] [-RemoveCertificate <String[]>] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCertificateRegistrationPoint** cmdlet updates the settings of a certificate registration point role on a site system server.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a certificate registration point role by using the pipeline
```
PS XYZ:\> Get-CMCertificateRegistrationPoint -SiteSystemServerName "SiteServer01.Contoso.com" | Set-CMCertificateRegistrationPoint  -AddCertificate @{"https://ndes2.fabrikam.com/certsrv/mscep/mscep.dll" ="\\Server\ShareFolder\Cert.cer"} -ConnectionAccountUserName (Get-CMUser -Name Contoso\Administrator).UserName -RemoveCertificate @{"https://ndes1.fabrikam.com/certsrv/mscep/mscep.dll"="\\Server\ShareFolder\RootCA.cer"}.Keys[0]
```

This command gets the certificate registration point object for the site system server named SiteServer01.Contoso.com and uses the pipeline operator to pass the object to **Set-CMCertificateRegistrationPoint**.
**Set-CMCertificateRegistrationPoint** adds the certificate named Cert.cer and removes the certificate named RootCA.cer by using the user account named Contoso\Administrator to connect to the Configuration Manager database.

### Example 2: Set a certificate registration point role by name
```
PS XYZ:\> Set-CMCertificateRegistrationPoint -SiteSystemServerName "SiteServer02.Contoso.com" -AddCertificate @{"https://ndes2.fabrikam.com/certsrv/mscep/mscep.dll"="\\Server\ShareFolder\RootCA.cer"} -ConnectionAccountUserName (Get-CMUser -Name Contoso\Admin1).UserName -RemoveCertificate @{"https://ndes1.fabrikam.com/certsrv/mscep/mscep.dll" ="\\Server\ShareFolder\Cert.cer"}.Keys[0]
```

This command adds the certificate named RootCA.cer to the site system server named SiteServer02.Contoso.com, and removes the certificate named Cert.cer, by using the user account named Contoso\Admin1 to connect to the Configuration Manager database.

## PARAMETERS

### -AddCertificate
Specifies, as a hash table, the URL for the Network Device Enrollment Service and the root CA certificate.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: AddCertificates

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionAccountUserName
Specifies the account that connects the certification registration point to the Configuration Manger database.

```yaml
Type: String
Parameter Sets: (All)
Aliases: UserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject
Specifies a certification registration point object.
To obtain a certificate registration point object, use the Get-CMCertificateRegistrationPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: CertificateRegistrationPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Port
Specifies the HTTPS port number used by the certificate registration point to communicate with the Network Device Enrollment Service.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCertificate
Specifies an array of URLs that match corresponding certificates in the original object.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveCertificates, RemoveCertificateUrl, RemoveCertificateUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site server.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of the Configuration Manager site system server.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMCertificateRegistrationPoint](Add-CMCertificateRegistrationPoint.md)

[Get-CMCertificateRegistrationPoint](Get-CMCertificateRegistrationPoint.md)

[Remove-CMCertificateRegistrationPoint](Remove-CMCertificateRegistrationPoint.md)
