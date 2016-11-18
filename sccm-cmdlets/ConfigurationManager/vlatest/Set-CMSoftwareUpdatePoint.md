---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 781F6A2C-9A81-48F4-92EE-171566F550CF
---

# Set-CMSoftwareUpdatePoint

## SYNOPSIS
Changes settings for a Configuration Manager software update point.

## SYNTAX

### ByValue (Default)
```
Set-CMSoftwareUpdatePoint [-HttpPort <Int32>] [-HttpsPort <Int32>] -InputObject <IResultObject>
 [-ClientConnectionType <ClientConnectionTypes>] [-EnableSsl <Boolean>] [-UseProxy <Boolean>]
 [-UseProxyForAutoDeploymentRule <Boolean>] [-AnonymousWsusAccess] [-WsusAccessAccount <String>]
 [-NlbVirtualIP <String>] [-PublicVirtualIP <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMSoftwareUpdatePoint [-HttpPort <Int32>] [-HttpsPort <Int32>] [-SiteSystemServerName] <String>
 [-SiteCode <String>] [-ClientConnectionType <ClientConnectionTypes>] [-EnableSsl <Boolean>]
 [-UseProxy <Boolean>] [-UseProxyForAutoDeploymentRule <Boolean>] [-AnonymousWsusAccess]
 [-WsusAccessAccount <String>] [-NlbVirtualIP <String>] [-PublicVirtualIP <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdatePoint** cmdlet changes settings for a software update point in Microsoft System Center Configuration Manager.

A software update point is a site server role that hosts software updates.
System Center Configuration Manager clients connect to a software update point to get available updates.
The software update point interacts with Windows Server Update Services (WSUS) to configure update settings, request synchronization to the update source, and to synchronize software updates from the WSUS database.

You can use this cmdlet to configure the settings a software update point uses when connecting with clients and with a WSUS server.
These settings include Network Load Balancing (NLB), a virtual IP address, Internet Information Services (IIS) port, and whether to use Secure Socket Locket Layer (SSL) to connect with WSUS.

## EXAMPLES

### Example 1: Modify the server name
```
PS C:\>Set-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "CMSoftwareUpdatePoint.TSQA.Contoso.com"
```

This command modifies the name for the site system server for the site code CM1.

## PARAMETERS

### -AnonymousWsusAccess


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

### -ClientConnectionType


```yaml
Type: ClientConnectionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Intranet, Internet, InternetAndIntranet

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

### -EnableSsl


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: SslWsus, WsusSsl

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

### -HttpPort


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WsusIisPort

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HttpsPort


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WsusIisSslPort

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SoftwareUpdatePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NlbVirtualIP


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

### -PassThru


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

### -PublicVirtualIP


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

### -UseProxy


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

### -UseProxyForAutoDeploymentRule


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

### -WsusAccessAccount


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

[Add-CMSoftwareUpdatePoint](./Add-CMSoftwareUpdatePoint.md)

[Get-CMSoftwareUpdatePoint](./Get-CMSoftwareUpdatePoint.md)

[Remove-CMSoftwareUpdatePoint](./Remove-CMSoftwareUpdatePoint.md)


