---
description: Get a cloud management gateway.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/26/2021
schema: 2.0.0
title: Get-CMCloudManagementGateway
---

# Get-CMCloudManagementGateway

## SYNOPSIS

Get a cloud management gateway (CMG).

## SYNTAX

### SearchByName (Default)
```
Get-CMCloudManagementGateway [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMCloudManagementGateway -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get an object for a cloud management gateway (CMG) that's configured for the site.

For more information, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Get-CMCloudManagementGateway -Name "GraniteFalls.cloudapp.net"
```

## PARAMETERS

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

### -Id

Specify the site's ID for the Azure service. The **Id** is the integer value stored in the site database for the service. For example, run the following SQL query, and look at the **ID** column: `select * from Azure_CloudService`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the service name for the CMG in Azure.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_AzureService
## NOTES

## RELATED LINKS

[New-CMCloudManagementGateway](New-CMCloudManagementGateway.md)
[Remove-CMCloudManagementGateway](Remove-CMCloudManagementGateway.md)
[Set-CMCloudManagementGateway](Set-CMCloudManagementGateway.md)
[Start-CMCloudManagementGateway](Start-CMCloudManagementGateway.md)
[Stop-CMCloudManagementGateway](Stop-CMCloudManagementGateway.md)

[Sync-CMCloudManagementGateway](Sync-CMCloudManagementGateway.md)

[CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview)
