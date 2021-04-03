---
description: Remove a cloud management gateway connection point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Remove-CMCloudManagementGatewayConnectionPoint
---

# Remove-CMCloudManagementGatewayConnectionPoint

## SYNOPSIS

Remove a cloud management gateway connection point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMCloudManagementGatewayConnectionPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMCloudManagementGatewayConnectionPoint [-Force] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a cloud management gateway (CMG) connection point role from a site system server.

For more information on CMG, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Get-CMCloudManagementGatewayConnectionPoint -SiteSystemServerName "cmgcp.contoso.com" | Remove-CMCloudManagementGatewayConnectionPoint
```

## PARAMETERS

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

### -Force

Run the command without asking for confirmation.

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

Specify a CMG connection point object as the target for this cmdlet. To get the object, use the [Get-CMCloudManagementGatewayConnectionPoint](Get-CMCloudManagementGatewayConnectionPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: GatewayConnectionPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode

Specify the site code for this site system role.

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

Specify the FQDN of the server with this role.

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

###  

## NOTES

## RELATED LINKS

[Add-CMCloudManagementGatewayConnectionPoint](Add-CMCloudManagementGatewayConnectionPoint.md)

[Get-CMCloudManagementGatewayConnectionPoint](Get-CMCloudManagementGatewayConnectionPoint.md)

[Set-CMCloudManagementGatewayConnectionPoint](Set-CMCloudManagementGatewayConnectionPoint.md)
