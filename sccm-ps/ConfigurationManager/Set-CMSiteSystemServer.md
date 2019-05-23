---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 20AEB24C-2706-4103-B3D1-808D355C696C
online version: https://go.microsoft.com/fwlink/?linkid=834042
schema: 2.0.0
---

# Set-CMSiteSystemServer

## SYNOPSIS
Modifies a site system server.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMSiteSystemServer [-PublicFqdn <String>] [-FdmOperation <Boolean>] [-UseSiteServerAccount]
 [-AccountName <String>] [-EnableProxy <Boolean>] [-ProxyServerName <String>] [-ProxyServerPort <UInt32>]
 [-ProxyAccessAccount <IResultObject>] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMSiteSystemServer [-SiteCode <String>] [-SiteSystemServerName] <String> [-PublicFqdn <String>]
 [-FdmOperation <Boolean>] [-UseSiteServerAccount] [-AccountName <String>] [-EnableProxy <Boolean>]
 [-ProxyServerName <String>] [-ProxyServerPort <UInt32>] [-ProxyAccessAccount <IResultObject>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSiteSystemServer** cmdlet modifies a site system server in Microsoft System Center Configuration Manager.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Modify a site system server by using the pipeline operator
```
PS XYZ:\> Get-CMSiteSystemServer -Name "Server2.contoso.com" -SiteCode MP5 | Set-CMSiteSystemServer -SiteCode MP5 -PublicFqdn "Internetsrv2New.contoso.com" -FdmOperation $False -AccountName "contoso\administrator" -EnableProxy $True -ProxyServerName "ProxyServer1" -ProxyServerPort 80 -ProxyAccessAccount (Get-CMAccount "contoso\administrator") -PassThru
```

This command gets the site system server object named Server2.contoso.com with the site code MP5 and uses the pipeline operator to pass the object to **Set-CMSiteSystemServer**.
**Set-CMSiteSystemServer** adds an FQDN to the site system server to use on the Internet, and enables a proxy server named ProxyServer1 to connect to the Internet using port 80.

### Example 2: Modify a site system server
```
PS XYZ:\> Set-CMSiteSystemServer -SiteSystemServerName "Server2.contoso.com" -SiteCode "MP5" -PublicFqdn "Internetsrv2New.contoso.com" -FdmOperation $False -AccountName "contoso\administrator" -EnableProxy $True -ProxyServerName "ProxyServer1" -ProxyServerPort 80 -ProxyAccessAccount (Get-CMAccount "contoso\administrator") -PassThru
```

This command gets the site system server object named Server2.contoso.com with the site code MP5, adds an FQDN to the site system server to use on the Internet, and enables a proxy server named ProxyServer1 to connect to the Internet using port 80.

## PARAMETERS

### -AccountName
Specifies the account name for the site system.

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

### -EnableProxy
Indicates whether to enable a proxy server to use when the server synchronizes information from the Internet.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FdmOperation
Indicates whether the site system server is required to initiate connections to this site system.

```yaml
Type: Boolean
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

### -InputObject
Specifies a site system server object.
To obtain a site system server object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: SiteSystemServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -ProxyAccessAccount
Specifies the credentials to use to authenticate with the proxy server.
Do not use user principal name (UPN) format.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProxyServerName
Specifies the name of a proxy server.
Use a fully qualified domain name (FQDN), short name, or IPv4/IPv6 address.

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

### -ProxyServerPort
Specifies the proxy server port number to use when connecting to the Internet.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicFqdn
Specifies a FQDN for the site system for use on the Internet.

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
Specifies the site code of a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies a server name for the site system.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseSiteServerAccount
Indicates that the cmdlet uses the site server's computer account to install the site system.

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

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Get-CMAccount](Get-CMAccount.md)

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[New-CMSiteSystemServer](New-CMSiteSystemServer.md)

[Remove-CMSiteSystemServer](Remove-CMSiteSystemServer.md)
