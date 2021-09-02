---
description: Changes settings for a file replication route in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMFileReplicationRoute
---

# Set-CMFileReplicationRoute

## SYNOPSIS
Changes settings for a file replication route in Configuration Manager.

## SYNTAX

### SetFileReplicationAccount (Default)
```
Set-CMFileReplicationRoute -DestinationSiteCode <String> [-FileReplicationAccountName <String>]
 -SourceSiteCode <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetFileReplicationRouteBySchedule
```
Set-CMFileReplicationRoute [-AvailabilityLevel <AvailabilityLevel>] [-BeginHr <Int32>]
 [-ControlNetworkLoadSchedule] [-DaysOfWeek <DaysOfWeek[]>] -DestinationSiteCode <String> [-EndHr <Int32>]
 -SourceSiteCode <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetFileReplicationRouteByPulseMode
```
Set-CMFileReplicationRoute [-DataBlockSizeKB <Int32>] [-DelayBetweenDataBlockSec <Int32>]
 -DestinationSiteCode <String> [-FileReplicationAccountName <String>] [-PulseMode] -SourceSiteCode <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetFileReplicationRouteByUnlimited
```
Set-CMFileReplicationRoute -DestinationSiteCode <String> [-FileReplicationAccountName <String>]
 -SourceSiteCode <String> [-Unlimited] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetFileReplicationRouteByLimited
```
Set-CMFileReplicationRoute -DestinationSiteCode <String> [-FileReplicationAccountName <String>]
 [-LimitAvailableBandwidthPercent <Int32>] [-Limited] [-LimitedBeginHr <Int32>] [-LimitedEndHr <Int32>]
 -SourceSiteCode <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMFileReplicationRoute** cmdlet changes settings for a file replication route from Configuration Manager.
Configuration Manager uses file replication routes to transfer file-based data between sites in a hierarchy.
Each file replication route identifies a destination site to which file-based data can transfer.

File replication routes were known as addresses in versions of Configuration Manager before Configuration Manager.
The functionality of file replication routes is the same as that of addresses in earlier versions.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Specify a file replication route by using a replication account name
```
PS XYZ:\> Set-CMFileReplicationRoute -SourceSiteCode "CM2" -DestinationSiteCode "SS2" -FileReplicationAccountName "11\12" -Unlimited
```

This command specifies a file replication route between the source site named CM2 and the destination site named SS2.
It uses the user account name 11\12 for file replication.

### Example 2: Specify a file replication route by using a source and destination site names
```
PS XYZ:\> Set-CMFileReplicationRoute -SourceSiteCode "CM2" -DestinationSiteCode "SS2" -ControlNetworkLoadSchedule -DaysOfWeek Friday, Sunday -AvailabilityLevel All
```

This command specifies a file replication route between the source site named CM2 and the destination site named SS2.
It schedules file replication for Fridays and Sundays.

## PARAMETERS

### -AvailabilityLevel
Specifies a value that indicates the priorities for which the scheduled restriction allows.
The system allows all priorities, no priorities, high priority only or high and medium priority.
The acceptable values for this parameter are:

- All
- Closed
- High
- MediumHigh

```yaml
Type: AvailabilityLevel
Parameter Sets: SetFileReplicationRouteBySchedule
Aliases:
Accepted values: All, MediumHigh, High, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BeginHr
```yaml
Type: Int32
Parameter Sets: SetFileReplicationRouteBySchedule
Aliases: TimePeriodStart, BeginHour

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ControlNetworkLoadSchedule
Indicates that scheduled replication controls network load.

```yaml
Type: SwitchParameter
Parameter Sets: SetFileReplicationRouteBySchedule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataBlockSizeKB
Specifies a data block size, in kilobytes.

```yaml
Type: Int32
Parameter Sets: SetFileReplicationRouteByPulseMode
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek
Specifies an array of values that indicate when the file replication runs for this route.
The acceptable values for this parameter are:

- Friday
- Saturday
- Sunday
- Monday
- Tuesday
- Wednesday
- Thursday

```yaml
Type: DaysOfWeek[]
Parameter Sets: SetFileReplicationRouteBySchedule
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DelayBetweenDataBlockSec
```yaml
Type: Int32
Parameter Sets: SetFileReplicationRouteByPulseMode
Aliases: DelayBetweenDataBlocksSeconds, DelayBetweenDataBlocksSec

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationSiteCode
Specifies the destination site in the file replication route that you change by using a site code.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DesSiteCode, DestSiteCode, ServerFqdn

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

### -EndHr
```yaml
Type: Int32
Parameter Sets: SetFileReplicationRouteBySchedule
Aliases: TimePeriodEnd, EndHour

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileReplicationAccountName
Specifies the account that Configuration Manager uses to install a site on the specified server and maintain communications between the site and other sites.
This account must have local administrative credentials.

```yaml
Type: String
Parameter Sets: SetFileReplicationAccount, SetFileReplicationRouteByPulseMode, SetFileReplicationRouteByUnlimited, SetFileReplicationRouteByLimited
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

### -LimitAvailableBandwidthPercent
```yaml
Type: Int32
Parameter Sets: SetFileReplicationRouteByLimited
Aliases: LimitAvailableBandwidthPercentage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Limited
Indicates that bandwidth for a file replication route is limited.

```yaml
Type: SwitchParameter
Parameter Sets: SetFileReplicationRouteByLimited
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitedBeginHr
```yaml
Type: Int32
Parameter Sets: SetFileReplicationRouteByLimited
Aliases: LimitedTimePeriodStart, LimitedBeginHour

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitedEndHr
```yaml
Type: Int32
Parameter Sets: SetFileReplicationRouteByLimited
Aliases: LimitedTimePeriodEnd, LimitedEndHour

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PulseMode
Indicates that file replication uses data block size and delays between transmissions.
Use this parameter when you have low network bandwidth between sites.

```yaml
Type: SwitchParameter
Parameter Sets: SetFileReplicationRouteByPulseMode
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceSiteCode
Specifies the source site in the file replication route that you change by using a site code.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SiteCode

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Unlimited
Indicates that bandwidth for a file replication route is unlimited.

```yaml
Type: SwitchParameter
Parameter Sets: SetFileReplicationRouteByUnlimited
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
Default value: False
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

### None
## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMFileReplicationRoute](Get-CMFileReplicationRoute.md)

[New-CMFileReplicationRoute](New-CMFileReplicationRoute.md)

[Remove-CMFileReplicationRoute](Remove-CMFileReplicationRoute.md)


