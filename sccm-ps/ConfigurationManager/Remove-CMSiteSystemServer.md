---
description: Remove the site system server role.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: Remove-CMSiteSystemServer
---

# Remove-CMSiteSystemServer

## SYNOPSIS

Remove the site system server role.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMSiteSystemServer [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Remove-CMSiteSystemServer [-Force] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove the site system server role. A server with the **Site system** role hosts one or more other roles for a Configuration Manager site.

If the server has other site system roles besides the site system role, this cmdlet fails.

To remove other roles, use one of the following cmdlets:

- [Remove-CMAssetIntelligenceSynchronizationPoint](Remove-CMAssetIntelligenceSynchronizationPoint.md)
- [Remove-CMCertificateRegistrationPoint](Remove-CMCertificateRegistrationPoint.md)
- [Remove-CMCloudManagementGatewayConnectionPoint](Remove-CMCloudManagementGatewayConnectionPoint.md)
- [Remove-CMDataWarehouseServicePoint](Remove-CMDataWarehouseServicePoint.md)
- [Remove-CMDistributionPoint](Remove-CMDistributionPoint.md)
- [Remove-CMEndpointProtectionPoint](Remove-CMEndpointProtectionPoint.md)
- [Remove-CMFallbackStatusPoint](Remove-CMFallbackStatusPoint.md)
- [Remove-CMManagementPoint](Remove-CMManagementPoint.md)
- [Remove-CMMulticastServicePoint](Remove-CMMulticastServicePoint.md)
- [Remove-CMReportingServicePoint](Remove-CMReportingServicePoint.md)
- [Remove-CMServiceConnectionPoint](Remove-CMServiceConnectionPoint.md)
- [Remove-CMSoftwareUpdatePoint](Remove-CMSoftwareUpdatePoint.md)
- [Remove-CMStateMigrationPoint](Remove-CMStateMigrationPoint.md)

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a site system server

This command first uses the **Get-CMSiteSystemServer** cmdlet to get the site system server object for **Server2.contoso.com** in the site **MP5**. It then uses the pipeline operator to pass the object to **Remove-CMSiteSystemServer**, which removes the site system server role.

```powershell
Get-CMSiteSystemServer -SiteSystemServerName "Server2.contoso.com" -SiteCode "MP5" | Remove-CMSiteSystemServer -Force
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
Default value: False
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

Specify a site system server object to remove. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: SiteSystem, SiteSystemServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode

Specify the Configuration Manager site code.

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

Specify the name of the server with the site system role to remove.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName

Required: True
Position: 0
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

###  

## NOTES

## RELATED LINKS

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[New-CMSiteSystemServer](New-CMSiteSystemServer.md)

[Set-CMSiteSystemServer](Set-CMSiteSystemServer.md)
