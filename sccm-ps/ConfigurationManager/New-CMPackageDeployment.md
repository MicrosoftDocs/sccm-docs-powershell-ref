---
description: Deploy a legacy package to a collection.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 06/16/2021
schema: 2.0.0
title: New-CMPackageDeployment
---

# New-CMPackageDeployment

## SYNOPSIS

Deploy a legacy package to a collection.

## SYNTAX

### DeployStandardProgramByPackageValue (Default)
```
New-CMPackageDeployment [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>]
 [-DeployPurpose <DeployPurposeType>] [-FastNetworkOption <FastNetworkOptionType>] [-Package] <IResultObject>
 [-PersistOnWriteFilterDevice <Boolean>] -ProgramName <String> [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType>]
 [-SendWakeupPacket <Boolean>] [-SlowNetworkOption <SlowNetworkOptionType>] [-SoftwareInstallation <Boolean>]
 [-StandardProgram] [-SystemRestart <Boolean>] [-UseUtcForAvailableSchedule <Boolean>]
 [-UseUtcForExpireSchedule <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByPackageName
```
New-CMPackageDeployment [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>]
 [-DeployPurpose <DeployPurposeType>] [-FastNetworkOption <FastNetworkOptionType>] -PackageName <String>
 [-PersistOnWriteFilterDevice <Boolean>] -ProgramName <String> [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType>]
 [-SendWakeupPacket <Boolean>] [-SlowNetworkOption <SlowNetworkOptionType>] [-SoftwareInstallation <Boolean>]
 [-StandardProgram] [-SystemRestart <Boolean>] [-UseUtcForAvailableSchedule <Boolean>]
 [-UseUtcForExpireSchedule <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByPackageId
```
New-CMPackageDeployment [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>]
 [-DeployPurpose <DeployPurposeType>] [-FastNetworkOption <FastNetworkOptionType>] -PackageId <String>
 [-PersistOnWriteFilterDevice <Boolean>] -ProgramName <String> [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType>]
 [-SendWakeupPacket <Boolean>] [-SlowNetworkOption <SlowNetworkOptionType>] [-SoftwareInstallation <Boolean>]
 [-StandardProgram] [-SystemRestart <Boolean>] [-UseUtcForAvailableSchedule <Boolean>]
 [-UseUtcForExpireSchedule <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployStandardProgramByProgramValue
```
New-CMPackageDeployment [-AllowFallback <Boolean>] [-AllowSharedContent <Boolean>]
 [-DeployPurpose <DeployPurposeType>] [-FastNetworkOption <FastNetworkOptionType>]
 [-PersistOnWriteFilterDevice <Boolean>] [-Program] <IResultObject> [-RerunBehavior <RerunBehaviorType>]
 [-RunFromSoftwareCenter <Boolean>] [-Schedule <IResultObject[]>] [-ScheduleEvent <ScheduleEventType>]
 [-SendWakeupPacket <Boolean>] [-SlowNetworkOption <SlowNetworkOptionType>] [-SoftwareInstallation <Boolean>]
 [-StandardProgram] [-SystemRestart <Boolean>] [-UseUtcForAvailableSchedule <Boolean>]
 [-UseUtcForExpireSchedule <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageName
```
New-CMPackageDeployment [-DeployPurpose <DeployPurposeType>] [-DeviceProgram] -PackageName <String>
 -ProgramName <String> [-RecurUnit <RecurUnitType>] [-RecurValue <Int32>] [-Rerun <Boolean>]
 [-UseUtc <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageId
```
New-CMPackageDeployment [-DeployPurpose <DeployPurposeType>] [-DeviceProgram] -PackageId <String>
 -ProgramName <String> [-RecurUnit <RecurUnitType>] [-RecurValue <Int32>] [-Rerun <Boolean>]
 [-UseUtc <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByPackageValue
```
New-CMPackageDeployment [-DeployPurpose <DeployPurposeType>] [-DeviceProgram] [-Package] <IResultObject>
 -ProgramName <String> [-RecurUnit <RecurUnitType>] [-RecurValue <Int32>] [-Rerun <Boolean>]
 [-UseUtc <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployDeviceProgramByProgramValue
```
New-CMPackageDeployment [-DeployPurpose <DeployPurposeType>] [-DeviceProgram] [-Program] <IResultObject>
 [-RecurUnit <RecurUnitType>] [-RecurValue <Int32>] [-Rerun <Boolean>] [-SendWakeupPacket <Boolean>]
 [-UseUtc <Boolean>] [-DistributeCollectionName <String>] [-DistributeContent]
 [-DistributionPointGroupName <String>] [-DistributionPointName <String>] [-AvailableDateTime <DateTime>]
 [-Comment <String>] [-DeadlineDateTime <DateTime>] [-UseMeteredNetwork <Boolean>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to deploy a package to resources in a collection.
You can specify the collection by ID, name, or pass an object.

For other deployment settings that you can't configure with this cmdlet, use [Set-CMPackageDeployment](Set-CMPackageDeployment.md).

For more information, see [Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs#deploy-packages-and-programs).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Deploy a package by ID

This command creates a deployment of the package with ID **XYZ00001** to the collection with ID **XYZ0003F**.

```powershell
$pkgId = "XYZ00001"
$collId = "XYZ0003F"
New-CMPackageDeployment -StandardProgram -PackageId $pkgId -ProgramName "ScanState" -CollectionID $collId -Comment "Use USMT to scan for data" -DeployPurpose Available
```

### Example 2: Deploy a package as required with a deadline

The first command sets a variable for a deadline to 10 days from now at 8:00 PM.
The second command creates a schedule object based on that deadline that recurs daily.
The third command creates the package deployment with that schedule.

```powershell
[datetime]$DeadlineTime = (Get-Date -Hour 20 -Minute 0 -Second 0).AddDays(10)

$NewScheduleDeadline = New-CMSchedule -Start $DeadlineTime -Nonrecurring

$pkgId = "XYZ00001"
$progName = "Run"
$collId = "XYZ0003F"

New-CMPackageDeployment -StandardProgram -PackageId $pkgId -ProgramName $progName -DeployPurpose Required -CollectionId $collId -FastNetworkOption DownloadContentFromDistributionPointAndRunLocally -SlowNetworkOption DownloadContentFromDistributionPointAndLocally -RerunBehavior RerunIfFailedPreviousAttempt -Schedule $NewScheduleDeadline
```

## PARAMETERS

### -AllowFallback

Allow clients to use distribution points from the default site boundary group.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowSharedContent

Allow clients to use distribution points from a neighbor boundary group.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableDateTime

Specify when this deployment is _available_.

Use **-DeadlineDateTime** to specify when the deployment _expires_, and **-Schedule** to specify the deployment assignment, or _deadline_.

To get a **DateTime** object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection

Specify a collection object as the target for this package deployment. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specify a collection ID as the target for this package deployment.

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

### -CollectionName

Specify a collection name as the target for this package deployment.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Comment

Specify an optional comment for this package deployment.

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

### -Confirm

Add this parameter to prompt for confirmation before running the cmdlet.

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

### -DeadlineDateTime

Use this parameter to specify when the deployment _expires_.

Use **-AvailableDateTime** to specify when the deployment is _available_, and **-Schedule** to specify the deployment assignment, or _deadline_.

To get a **DateTime** object, use the [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) cmdlet.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeployPurpose

Specify whether this deployment is available for users to install, or it's required to install at the deadline.

```yaml
Type: DeployPurposeType
Parameter Sets: (All)
Aliases:
Accepted values: Available, Required

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceProgram

If the program for the package that you're deploying is a device-type program, specify this parameter.

Otherwise, use the **StandardProgram** parameter. The standard program type is for computers with the Configuration Manager client.

```yaml
Type: SwitchParameter
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
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

### -DistributeCollectionName

The site distributes content to the distribution point groups that are associated with this collection name.

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

### -DistributeContent

Add this parameter to distribute the package content when you create this deployment. Clients can't install the package until you distribute content to distribution points that the clients can access.

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

### -DistributionPointGroupName

The site distributes content to this distribution point group.

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

### -DistributionPointName

The site distributes content to this distribution point.

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

### -FastNetworkOption

Specify the behavior when the client uses a distribution point from the current boundary group:

- Run program from distribution point
- Download content from distribution point and run locally

If you don't specify this parameter, it uses `DownloadContentFromDistributionPointAndRunLocally` by default. This option is more secure, because the client validates the content hash before it runs the program.

```yaml
Type: FastNetworkOptionType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:
Accepted values: RunProgramFromDistributionPoint, DownloadContentFromDistributionPointAndRunLocally

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

### -Package

Specify a package object with the program to deploy. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: DeployStandardProgramByPackageValue, DeployDeviceProgramByPackageValue
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PackageId

Specify the ID of the package with the program to deploy. This ID is a standard package ID, for example `XYZ007E3`.

```yaml
Type: String
Parameter Sets: DeployStandardProgramByPackageId, DeployDeviceProgramByPackageId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName

Specify the name of the package with the program to deploy.

```yaml
Type: String
Parameter Sets: DeployStandardProgramByPackageName, DeployDeviceProgramByPackageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistOnWriteFilterDevice

Configure how the client handles the write filter on Windows Embedded devices.

- `$true`: Commit changes at the deadline or during a maintenance window. A restart is required.
- `$false`: Apply content on the overlay and commit later.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Program

Specify a program object to deploy. To get this object, use the [Get-CMProgram](Get-CMProgram.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: DeployStandardProgramByProgramValue, DeployDeviceProgramByProgramValue
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ProgramName

Specify the name of the program in the package to deploy.

```yaml
Type: String
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue
Aliases: StandardProgramName, DeviceProgramName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurUnit

Specify a unit for a recurring deployment. Use the **RecurValue** parameter to specify the value for this unit.

```yaml
Type: RecurUnitType
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases:
Accepted values: Minutes, Hours, Days

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecurValue

Specify how often the deployment recurs.

This parameter depends on the unit type specified in the **RecurUnit** parameter:

- **Hours**: This value can be between `1` and `23`
- **Days**: Between `1` and `31`
- **Minutes**: Between `1` and `59`

```yaml
Type: Int32
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rerun

Indicate whether the deployment reruns:

- `$True`: The deployment runs again for clients as specified in the **RerunBehavior** parameter. This value is the default.
- `$False`: The deployment doesn't run again.

```yaml
Type: Boolean
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RerunBehavior

Specify whether the program reruns on a computer.

- `NeverRerunDeployedProgram`: Doesn't rerun, even if the deployment failed or files changed.
- `AlwaysRerunProgram`: Rerun as scheduled, even if the deployment succeeded. You can use this value for recurring deployments. This value is the default.
- `RerunIfFailedPreviousAttempt`: Rerun as scheduled, if the deployment failed on the previous attempt.
- `RerunIfSucceededOnPreviousAttempt`: Rerun only if the previous attempt succeeded.

```yaml
Type: RerunBehaviorType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:
Accepted values: NeverRerunDeployedProgram, AlwaysRerunProgram, RerunIfFailedPreviousAttempt, RerunIfSucceededOnPreviousAttempt

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunFromSoftwareCenter

Allow users to run the program independently of assignments.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases: AllowUsersRunIndependently

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule

Use this parameter to specify the deployment assignment, or _deadline_.

Use **-AvailableDateTime** to specify when the deployment is _available_, and **-DeadlineDateTime** to specify when the deployment _expires_.

Specify an array of schedule objects. A schedule object defines the mandatory assignment schedule for a deployment. To create a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScheduleEvent

Specify the event type that determines when the package deployment runs.

```yaml
Type: ScheduleEventType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:
Accepted values: AsSoonAsPossible, LogOn, LogOff

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendWakeupPacket

Indicates whether to send a wake-up packet to computers before the deployment begins. If this value is `$True`, Configuration Manager wakes a computer from sleep. If this value is `$False`, it doesn't wake computers from sleep. For computers to wake, first configure Wake On LAN.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue, DeployDeviceProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SlowNetworkOption

Specify the behavior when the client uses a distribution point from a neighbor boundary group or the default site boundary group:

- Do not run program
- Download content from distribution point and run locally
- Run program from distribution point

If you don't specify this parameter, it uses `DoNotRunProgram` by default.

```yaml
Type: SlowNetworkOptionType
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:
Accepted values: DoNotRunProgram, DownloadContentFromDistributionPointAndLocally, RunProgramFromDistributionPoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareInstallation

When the installation deadline is reached, set this parameter to `$true` to allow the package to install outside the maintenance window.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardProgram

Use this parameter for standard program types. This type is for computers with the Configuration Manager client.

If the program for the package that you're deploying is a device-type program, use the **DeviceProgram** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SystemRestart

When the installation deadline is reached, set this parameter to `$true` to allow system restart if necessary outside the maintenance window.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseMeteredNetwork

Indicates whether to allow clients on a metered internet connection to download content after the installation deadline, which might incur more cost.

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

### -UseUtc

Indicates whether clients use Coordinated Universal Time (UTC) to determine the availability of a program. UTC time makes the deployment available at the same time for all computers. If you don't specify this parameter, or set it to `$false`, the client uses its local time.

```yaml
Type: Boolean
Parameter Sets: DeployDeviceProgramByPackageName, DeployDeviceProgramByPackageId, DeployDeviceProgramByPackageValue, DeployDeviceProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtcForAvailableSchedule

Indicates whether clients use Coordinated Universal Time (UTC) to determine the availability of a program. UTC time makes the deployment available at the same time for all computers. If you don't specify this parameter, or set it to `$false`, the client uses its local time.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseUtcForExpireSchedule

Indicates whether clients use Coordinated Universal Time (UTC) to determine when a program is expired. UTC time expires the deployment at the same time for all computers. If you don't specify this parameter, or set it to `$false`, the client uses its local time.

```yaml
Type: Boolean
Parameter Sets: DeployStandardProgramByPackageValue, DeployStandardProgramByPackageName, DeployStandardProgramByPackageId, DeployStandardProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet isn't run.

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

[Get-CMPackageDeployment](Get-CMPackageDeployment.md)
[Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)
[Set-CMPackageDeployment](Set-CMPackageDeployment.md)
[Remove-CMPackageDeployment](Remove-CMPackageDeployment.md)
[Get-CMPackage](Get-CMPackage.md)

[Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs#deploy-packages-and-programs)
