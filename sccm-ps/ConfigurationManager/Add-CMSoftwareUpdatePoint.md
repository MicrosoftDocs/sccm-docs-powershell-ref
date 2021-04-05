---
description: Adds a software update point for Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMSoftwareUpdatePoint
---

# Add-CMSoftwareUpdatePoint

## SYNOPSIS
Adds a software update point for Configuration Manager.

## SYNTAX

### SumPByValueWithWsus (Default)
```
Add-CMSoftwareUpdatePoint [-AnonymousWsusAccess] [-ClientConnectionType <ClientConnectionTypes>]
 [-ConnectionAccountUserName <String>] [-EnableCloudGateway] -InputObject <IResultObject> [-UseProxy <Boolean>]
 [-UseProxyForAutoDeploymentRule <Boolean>] [-WsusIisPort <Int32>] [-WsusIisSslPort <Int32>]
 [-WsusSsl <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SumPWithWsus
```
Add-CMSoftwareUpdatePoint [-AnonymousWsusAccess] [-ClientConnectionType <ClientConnectionTypes>]
 [-ConnectionAccountUserName <String>] [-EnableCloudGateway] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-UseProxy <Boolean>] [-UseProxyForAutoDeploymentRule <Boolean>]
 [-WsusIisPort <Int32>] [-WsusIisSslPort <Int32>] [-WsusSsl <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSoftwareUpdatePoint** cmdlet adds a software update point that hosts the Windows Software Update Services (WSUS) processes.
A software update point in Configuration Manager manages the transfer of information from WSUS.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a software update point
```
PS XYZ:\>Add-CMSoftwareUpdatePoint -SiteCode "CM1" -SiteSystemServerName "CMSoftwareUpdatePoint.TSQA.Contoso.com"
```

This command adds a software update point on the computer named CMSoftwareUpdatePoint.TSQA.Contoso.com for the Configuration Manager site that has the site code CM1.

## PARAMETERS

### -AnonymousWsusAccess
Indicates that the software update point allows anonymous WSUS access.

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
Specifies the type of the client connection.
The acceptable values for this parameter are:

- Internet
- InternetAndIntranet
- Intranet

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

### -ConnectionAccountUserName
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

### -EnableCloudGateway
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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SumPByValueWithWsus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for the Configuration Manager site that manages the system role for the software update point.

```yaml
Type: String
Parameter Sets: SumPWithWsus
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a computer that hosts the software update point site system role.

```yaml
Type: String
Parameter Sets: SumPWithWsus
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseProxy
Indicates whether a software update point can use a proxy.

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
Indicates whether an auto deployment rule can use a proxy.

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

### -WsusIisPort
Specifies a port to use for unsecured access to the WSUS server.

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

### -WsusIisSslPort
Specifies a port to user for secured access to the WSUS server.

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

### -WsusSsl
Specifies whether the software update point uses SSL to connect to the WSUS server.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: SslWsus

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Get-CMSoftwareUpdatePoint](Get-CMSoftwareUpdatePoint.md)

[Remove-CMSoftwareUpdatePoint](Remove-CMSoftwareUpdatePoint.md)

[Set-CMSoftwareUpdatePoint](Set-CMSoftwareUpdatePoint.md)

[Get-CMSoftwareUpdatePointComponent](Get-CMSoftwareUpdatePointComponent.md)


