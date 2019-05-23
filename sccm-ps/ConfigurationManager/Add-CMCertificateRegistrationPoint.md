---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: F07B1E32-8C9F-4625-ABE9-A6A75E688700
online version: https://go.microsoft.com/fwlink/?linkid=833606
schema: 2.0.0
---

# Add-CMCertificateRegistrationPoint

## SYNOPSIS
Adds a certificate registration point role to a site system server.

## SYNTAX

### ByValue (Default)
```
Add-CMCertificateRegistrationPoint -Certificate <Hashtable> [-ConnectionAccountUserName <String>]
 -InputObject <IResultObject> [-IisWebsite <String>] [-WebApplicationName <String>] [-Port <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMCertificateRegistrationPoint -Certificate <Hashtable> [-ConnectionAccountUserName <String>]
 [-IisWebsite <String>] [-WebApplicationName <String>] [-Port <Int32>] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMCertificateRegistrationPoint** cmdlet adds a certificate registration point role to a site system server.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Add a certificate registration point role by using the pipeline
```
PS XYZ:\> Get-CMSitesystemserver -SiteSystemServerName "SiteSystemServer01.Contoso.com" | Add-CMCertificateRegistrationPoint -Certificate @{"https://www.ndes1.fabrikam.com/certsrv/mscep/mscep.dll"="\\Server\Sharefolder\RootCA.cer"}
```

This command gets the site system server object named SiteSystemServer01.Contoso.com and uses the pipeline operator to pass the object to **Add-CMCertificateRegistrationPoint**, which adds a certificate registration point role to the site system server.

### Example 2: Add a certificate registration point role by name
```
PS XYZ:\> Add-CMCertificateRegistrationPoint -SiteSystemServerName "SiteSystemServer02.Contoso.com" -Certificate @{"https://www.ndes1.fabrikam.com/certsrv/mscep/mscep.dll"="\\Server\Sharefolder\RootCA.cer"} -ConnectionAccountUserName (Get-CMUser -Name Contoso\User01).UserName -IisWebsite "TestWebsite01" -WebApplicationName "TestWebApp01" -Port 443 -Sitecode SC3
```

This command adds a site system server role to the site system server named SiteSystemServer02.Contoso.com, specifying a user account to use when connecting the certification registration point to the Configuration Manager database.

## PARAMETERS

### -Certificate
Specifies, as a hash table, the URL for the Network Device Enrollment Service and the root CA certificate.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Certificates

Required: True
Position: Named
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

### -IisWebsite
Specifies the website name used by the certificate registration point.

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

### -InputObject
Specifies a Configuration Manager site system server object.
To obtain a site system server object, use the Get-CMSiteSystemServer cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -SiteCode
Specifies the site code of the Configuration Manager site server.

```yaml
Type: String
Parameter Sets: ByName
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
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplicationName
Specifies the web application name used by the certificate registration point.

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCertificateRegistrationPoint](Get-CMCertificateRegistrationPoint.md)

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[Get-CMUser](Get-CMUser.md)

[Remove-CMCertificateRegistrationPoint](Remove-CMCertificateRegistrationPoint.md)

[Set-CMCertificateRegistrationPoint](Set-CMCertificateRegistrationPoint.md)
