---
description: Modifies client status settings.
external help file: AdminUI.PS.ClientStatus.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientStatusSetting
---

# Set-CMClientStatusSetting

## SYNOPSIS
Modifies client status settings.

## SYNTAX

```
Set-CMClientStatusSetting [-ClientPolicyDays <Int32>] [-HeartbeatDiscoveryDays <Int32>]
 [-HardwareInventoryDays <Int32>] [-SoftwareInventoryDays <Int32>] [-StatusMessageDays <Int32>]
 [-HistoryCleanupDays <Int32>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMClientStatusSetting** cmdlet modifies client status settings.
These settings determine the data collection intervals for individual client monitoring activities in Configuration Manager.

For more information about client settings, see [About Client Settings in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682067(v=technet.10)) in the TechNet library.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Modify all client status settings
```
PS XYZ:\> Set-CMClientStatusSetting -ClientPolicyDayInterval 2 -HeartbeatDiscoveryDayInterval 3 -HardwareInventoryDayInterval 4 -SoftwareInventoryDayInterval 5 -StatusMessageDayInterval 6 -HistoryCleanupDayInterval 7
```

This command modifies all client status settings.

### Example 2: Modify the Client Policy setting
```
PS XYZ:\> Set-CMClientStatusSetting -ClientPolicyDayInterval 5
```

This command modifies the client policy day setting only.

## PARAMETERS

### -ClientPolicyDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PolicyInactiveInterval, ClientPolicyDayInterval

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

### -HardwareInventoryDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: HWInactiveInterval, HardwareInventoryDayInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HeartbeatDiscoveryDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DdrInactiveInterval, HeartbeatDiscoveryDayInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HistoryCleanupDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CleanUpInterval, HistoryCleanupDayInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -SoftwareInventoryDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SWInactiveInterval, SoftwareInventoryDayInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusMessageDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StatusInactiveInterval, StatusMessageDayInterval

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_CH_Settings

### IResultObject#SMS_CH_Settings

## NOTES

## RELATED LINKS

[About Client Settings in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682067(v=technet.10))

[Get-CMClientStatusSetting](Get-CMClientStatusSetting.md)

[Update-CMClientStatus](Update-CMClientStatus.md)

[Get-CMClientStatusUpdateSchedule](Get-CMClientStatusUpdateSchedule.md)
