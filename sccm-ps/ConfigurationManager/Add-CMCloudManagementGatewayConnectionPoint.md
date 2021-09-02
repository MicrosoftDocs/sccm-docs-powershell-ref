---
description: Add a cloud management gateway connection point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Add-CMCloudManagementGatewayConnectionPoint
---

# Add-CMCloudManagementGatewayConnectionPoint

## SYNOPSIS

Add a cloud management gateway connection point.

## SYNTAX

### ByValue (Default)
```
Add-CMCloudManagementGatewayConnectionPoint -CloudManagementGatewayName <String> [-InputObject <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMCloudManagementGatewayConnectionPoint -CloudManagementGatewayName <String> [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add the site system role for a cloud management gateway (CMG) connection point.

For more information on how to use this cmdlet to create a cloud management gateway (CMG), see [2010 release notes: Cloud management gateway](/powershell/sccm/2010-release-notes#cloud-management-gateway).

For more information on CMG, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Add-CMCloudManagementGatewayConnectionPoint -CloudManagementGatewayName "GraniteFalls.cloudapp.net" -SiteSystemServerName "cmgcp.contoso.com"
```

## PARAMETERS

### -CloudManagementGatewayName

Specify the service name of the CMG in Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

Specify a site server object as the target for this role. To get the object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode

Specify the site code for this site system role.

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

Specify the FQDN of the server as the target for this role.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[Get-CMCloudManagementGatewayConnectionPoint](Get-CMCloudManagementGatewayConnectionPoint.md)

[Remove-CMCloudManagementGatewayConnectionPoint](Remove-CMCloudManagementGatewayConnectionPoint.md)

[Set-CMCloudManagementGatewayConnectionPoint](Set-CMCloudManagementGatewayConnectionPoint.md)

[Import-CMAADServerApplication](Import-CMAADServerApplication.md)

[Import-CMAADClientApplication](Import-CMAADClientApplication.md)

[New-CMCloudManagementAzureService](New-CMCloudManagementAzureService.md)

[New-CMCloudManagementGateway](New-CMCloudManagementGateway.md)

[Set-CMCloudManagementAzureService](Set-CMCloudManagementAzureService.md)

[CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview)
