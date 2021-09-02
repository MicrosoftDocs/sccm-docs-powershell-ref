---
description: Change settings for a Configuration Manager maintenance task.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Set-CMSiteMaintenanceTask
---

# Set-CMSiteMaintenanceTask

## SYNOPSIS

Change settings for a Configuration Manager maintenance task.

## SYNTAX

### SetSummaryTaskByName (Default)
```
Set-CMSiteMaintenanceTask [-FixedRun] [-RunIntervalMins <Int32>] [-RunNow] -SummaryTask <SummaryTask>
 [-PassThru] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetMaintenanceTasksByValue
```
Set-CMSiteMaintenanceTask [-BeginTime <DateTime>] [-DaysOfWeek <DaysOfWeek[]>] [-DeleteOlderThanDays <Int32>]
 [-DeviceName <String>] [-EnableAlert <Boolean>] [-Enabled <Boolean>] -InputObject <IResultObject>
 [-LatestBeginTime <DateTime>] [-SiteBackupPath <String>] [-SqlBackupPath <String>] [-PassThru]
 [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetMaintenanceTasksByTaskName
```
Set-CMSiteMaintenanceTask [-BeginTime <DateTime>] [-DaysOfWeek <DaysOfWeek[]>] [-DeleteOlderThanDays <Int32>]
 [-DeviceName <String>] [-EnableAlert <Boolean>] [-Enabled <Boolean>] [-LatestBeginTime <DateTime>]
 -Name <String> [-SiteBackupPath <String>] [-SqlBackupPath <String>] [-PassThru] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetMaintenanceTasksByName
```
Set-CMSiteMaintenanceTask [-BeginTime <DateTime>] [-DaysOfWeek <DaysOfWeek[]>] [-DeleteOlderThanDays <Int32>]
 [-DeviceName <String>] [-EnableAlert <Boolean>] [-Enabled <Boolean>] [-LatestBeginTime <DateTime>]
 -MaintenanceTask <MaintenanceTask> [-SiteBackupPath <String>] [-SqlBackupPath <String>] [-PassThru]
 [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMSiteMaintenanceTask** cmdlet changes settings for a Configuration Manager maintenance task. For more information, see [Maintenance tasks](/mem/configmgr/core/servers/manage/maintenance-tasks).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a maintenance task to run once a week

This example specifies that the maintenance task named **Backup SMS Site Server** runs on **Friday** each week on the Configuration Manager site that has the site code **CM1**.

```powershell
Set-CMSiteMaintenanceTask -SiteCode "CM1" -MaintenanceTaskName "Backup SMS Site Server" -DaysOfWeek Friday
```

### Example 2: Configure backup destinations

```powershell
Set-CMSiteMaintenanceTask -Name $TaskName -SiteBackupPath "c:\site-backup" -SqlBackupPath "c:\sql-backup" -BeginTime (Get-Date) -DaysOfWeek Sunday,Monday -EnableAlert $true -Enabled $true
```

## PARAMETERS

### -BeginTime

Specify the date and time at which a maintenance task starts.

```yaml
Type: DateTime
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysOfWeek

Specify an array of day names that determine the days of each week on which the maintenance task runs.

```yaml
Type: DaysOfWeek[]
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteOlderThanDays

For maintenance tasks that delete aged data, use this parameter to specify the number of days.

```yaml
Type: Int32
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases: DeleteOlderThan, DeleteThanOlderDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName

Specifies the name of the device on which the maintenance task runs.

```yaml
Type: String
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases:

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

### -EnableAlert

Set this parameter to `$true` to enable alerts for task failures, if the task supports it.

```yaml
Type: Boolean
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases: EnabledAlert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabled

Indicates whether the maintenance task is enabled in Configuration Manager.

```yaml
Type: Boolean
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FixedRun

Indicates that this cmdlet modifies the maintenance task as a fixed run.

```yaml
Type: SwitchParameter
Parameter Sets: SetSummaryTaskByName
Aliases: FixedRunInterval, DisableFixedRunInterval

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

Specify the maintenance task object to configure. To get this object, use the [Get-CMSiteMaintenanceTask](Get-CMSiteMaintenanceTask.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetMaintenanceTasksByValue
Aliases: MaintenanceTaskObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LatestBeginTime

Specifies a future date and time at which the maintenance task runs.

```yaml
Type: DateTime
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaintenanceTask

Specify the name of a maintenance task to configure.

```yaml
Type: MaintenanceTask
Parameter Sets: SetMaintenanceTasksByName
Aliases:
Accepted values: BackupSiteServer, CheckApplicationTitleWithInventoryInformation, ClearUndiscoveredClients, DeleteAgedApplicationRequestData, DeleteUnusedApplicationRevisions, DeleteAgedClientOperations, DeleteAgedCollectedFiles, DeleteAgedComputerAssociationData, DeleteAgedDeleteDetectionData, DeleteAgedDeviceWipeRecord, DeleteAgedDiscoveryData, DeleteAgedEnrolledDevices, DeleteAgedEndpointProtectionHealthStatusHistoryData, DeleteAgedDevicesManagedByTheExchangeServerConnector, DeleteAgedInventoryHistory, DeleteAgedLogData, DeleteAgedSoftwareMeteringData, DeleteAgedSoftwareMeteringSummaryData, DeleteAgedClientPresenceHistory, DeleteAgedNotificationTaskHistory, DeleteAgedReplicationTrackingData, DeleteAgedReplicationSummaryData, DeleteAgedStatusMessages, DeleteAgedThreatData, DeleteAgedUnknownComputers, DeleteAgedUserDeviceAffinityData, DeleteInactiveClientDiscoveryData, DeleteObsoleteAlerts, DeleteObsoleteClientDiscoveryData, DeleteObsoleteForestDiscoverySitesAndSubnets, EvaluateProvisionedAmtComputerCertificates, MonitorKeys, RebuildIndexes, SummarizeSoftwareMeteringFileUsageData, SummarizeInstalledSoftwareData, SummarizeSoftwareMeteringMonthlyUsageData, DeleteAgedDistributionPointUsageStats, DeleteAgedProxyTrafficData

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of a maintenance task object to configure.

```yaml
Type: String
Parameter Sets: SetMaintenanceTasksByTaskName
Aliases: MaintenanceTaskName, TaskName, ItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -RunIntervalMins
```yaml
Type: Int32
Parameter Sets: SetSummaryTaskByName
Aliases: RunIntervalMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunNow

Add this parameter to have Configuration Manager run the maintenance task immediately.

```yaml
Type: SwitchParameter
Parameter Sets: SetSummaryTaskByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteBackupPath

Applies to version 2010 and later. For the **Backup Site Server** task, specify the **Site backup destination**. The site server computer account needs full control to the destination folder.

```yaml
Type: String
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode

Specifies the site code of the Configuration Manager site that hosts the site system role.

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

### -SqlBackupPath

Applies to version 2010 and later. For the **Backup Site Server** task, specify the **SQL backup destination**. The site server computer account needs full control to the destination folder.

```yaml
Type: String
Parameter Sets: SetMaintenanceTasksByValue, SetMaintenanceTasksByTaskName, SetMaintenanceTasksByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SummaryTask

Specifies a summary maintenance task.

```yaml
Type: SummaryTask
Parameter Sets: SetSummaryTaskByName
Aliases:
Accepted values: UpdateApplicationCatalogTables

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_SCI_SQLTask
## NOTES

## RELATED LINKS

[Get-CMSiteMaintenanceTask](Get-CMSiteMaintenanceTask.md)
