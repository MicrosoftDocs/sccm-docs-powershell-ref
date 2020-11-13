---
description: Changes settings for a Configuration Manager maintenance task.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSiteMaintenanceTask
---

# Set-CMSiteMaintenanceTask

## SYNOPSIS
Changes settings for a Configuration Manager maintenance task.

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
The **Set-CMSiteMaintenanceTask** cmdlet changes settings for a Configuration Manager maintenance task.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Set a maintenance task to run once a week

This example specifies that the maintenance task named **Backup SMS Site Server** runs on **Friday** each week on the Configuration Manager site that has the site code **CM1**.

```powershell
Set-CMSiteMaintenanceTask -SiteCode "CM1" -MaintenanceTaskName "Backup SMS Site Server" -DaysOfWeek Friday
```

## PARAMETERS

### -BeginTime
Specifies the date and time at which a maintenance task starts.

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
Specifies an array of day names that determine the days of each week on which the maintenance task runs.
The acceptable values for this parameter are:

- Monday
- Tuesday
- Wednesday
- Thursday
- Friday
- Saturday
- Sunday

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

### -EnableAlert
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

### -InputObject
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
Specifies the name of a maintenance task.
The acceptable values for this parameter are:

- BackupConfigMgrSecondarySiteServer
- BackupSiteServer
- CheckApplicationTitleWithInventoryInformation
- ClearUndiscoveredClients
- DeleteAgedApplicationRequestData
- DeleteAgedClientAccessLicenseData
- DeleteAgedClientOperations
- DeleteAgedClientPresenceHistory
- DeleteAgedCollectedFiles
- DeleteAgedComputerAssociationData
- DeleteAgedConfigurationManagementData
- DeleteAgedDeleteDetectionData
- DeleteAgedDevicesManagedByTheExchangeServerConnector
- DeleteAgedDeviceWipeRecord
- DeleteAgedDiscoveryData
- DeleteAgedEndpointProtectionHealthStatusHistoryData
- DeleteAgedEnrolledDevices
- DeleteAgedInventoryHistory
- DeleteAgedLogData
- DeleteAgedNotificationTaskHistory
- DeleteAgedReplicationSummaryData
- DeleteAgedReplicationTrackingData
- DeleteAgedSoftwareMeteringData
- DeleteAgedStatusMessages
- DeleteAgedThreatData
- DeleteAgedUnknownComputers
- DeleteAgedUserDeviceAffinityData
- DeletedAgedClientPresenceHistory
- DeleteExpiredActivities
- DeleteExpiredActivityFacts
- DeleteExpiredBookmarks
- DeleteInactiveClientDiscoveryData
- DeleteObsoleteAlerts
- DeleteObsoleteClientDiscoveryData
- DeleteObsoleteForestDiscoverySitesAndSubnets
- DeleteUnusedApplicationRevisions
- EvaluateProvisionedAmtComputerCertificates
- ExportSiteDatabaseTransactionLog
- MonitorKeys
- RebuildIndexes
- ResetAmtComputerPasswords
- SiteDatabase
- SummarizeClientAccessLicenseWeeklyUsageData
- SummarizeInstalledSoftwareData
- SummarizeSoftwareMeteringFileUsageData
- SummarizeSoftwareMeteringMonthlyUsageData
- UpdateStatistics

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
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: SetMaintenanceTasksByTaskName
Aliases: MaintenanceTaskName, TaskName, ItemName

Required: True
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
Indicates whether Configuration Manager runs the maintenance task immediately.

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
{{ Fill SiteBackupPath Description }}

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
{{ Fill SqlBackupPath Description }}

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
The acceptable value for this parameter is UpdateApplicationCatalogTables.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_SQLTask

## NOTES

## RELATED LINKS

[Get-CMSiteMaintenanceTask](Get-CMSiteMaintenanceTask.md)
