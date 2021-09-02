---
description: Stop a cloud management gateway service in Azure.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Stop-CMCloudManagementGateway
---

# Stop-CMCloudManagementGateway

## SYNOPSIS

Stop a cloud management gateway service in Azure.

## SYNTAX

### SearchByValueMandatory (Default)
```
Stop-CMCloudManagementGateway -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Stop-CMCloudManagementGateway -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Stop-CMCloudManagementGateway -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to stop a cloud management gateway (CMG) service in Azure. If you configure the CMG to automatically stop when the total data transfer exceeds your threshold, the service stops automatically.

> [!IMPORTANT]
> Even if the service isn't running, there are still costs associated with the cloud service. Stopping the service doesn't eliminate all associated Azure costs. To remove all cost for the cloud service, delete the CMG.
>
> When you stop the CMG service, internet-based clients can't communicate with Configuration Manager.

For more information, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Get-CMCloudManagementGateway -Name "GraniteFalls.cloudapp.net" | Stop-CMCloudManagementGateway
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

### -InputObject

Specify a CMG object to stop. To get this object, use the [Get-CMCloudManagementGateway](Get-CMCloudManagementGateway.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the service name of the CMG to stop.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

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

### System.Object
## NOTES

## RELATED LINKS

[Get-CMCloudManagementGateway](Get-CMCloudManagementGateway.md)
[New-CMCloudManagementGateway](New-CMCloudManagementGateway.md)
[Remove-CMCloudManagementGateway](Remove-CMCloudManagementGateway.md)
[Set-CMCloudManagementGateway](Set-CMCloudManagementGateway.md)
[Start-CMCloudManagementGateway](Start-CMCloudManagementGateway.md)

[CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview)
