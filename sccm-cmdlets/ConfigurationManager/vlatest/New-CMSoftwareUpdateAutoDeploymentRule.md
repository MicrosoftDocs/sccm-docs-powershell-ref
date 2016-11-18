---
external help file: AdminUI.PS.Sum.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 1860D065-B2D0-4CDE-A75F-56F44FE40FD6
---

# New-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Creates Configuration Manager deployment rules for automatic software updates.

## SYNTAX

### NewByCollection (Default)
```
New-CMSoftwareUpdateAutoDeploymentRule -Name <String> [-Description <String>] -Collection <IResultObject>
 [-AddToExistingSoftwareUpdateGroup <Boolean>] [-EnabledAfterCreate <Boolean>] [-Enable <Boolean>]
 [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>] [-DeployWithoutLicense <Boolean>]
 [-ArticleId <String[]>] [-BulletinId <String[]>] [-CustomSeverity <SeverityType[]>]
 [-DateReleasedOrRevised <DateReleasedOrRevisedType>] [-UpdateDescription <String[]>] [-Language <String[]>]
 [-Required <String[]>] [-Severity <SeverityType[]>] [-Superseded <Boolean>] [-Title <String[]>]
 [-UpdateClassification <String[]>] [-Product <String[]>] [-MicrosoftAsVendor <Boolean>] [-RunType <RunType>]
 [-Schedule <IResultObject>] [-UseUtc <Boolean>] [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>]
 [-AvailableTimeUnit <TimeUnitType>] [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>]
 [-DeadlineTimeUnit <TimeUnitType>] [-UserNotification <UserNotificationType>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowRestart <Boolean>]
 [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>] [-WriteFilterHandling <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>] [-AlertTime <Int32>]
 [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-DeploymentPackageName <String>] [-DeploymentPackage <IResultObject>] [-DownloadFromInternet <Boolean>]
 [-Location <String>] [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>]
 [-LanguageSelection <String[]>] [-IsServicingPlan] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewByCollectionName
```
New-CMSoftwareUpdateAutoDeploymentRule -Name <String> [-Description <String>] -CollectionName <String>
 [-AddToExistingSoftwareUpdateGroup <Boolean>] [-EnabledAfterCreate <Boolean>] [-Enable <Boolean>]
 [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>] [-DeployWithoutLicense <Boolean>]
 [-ArticleId <String[]>] [-BulletinId <String[]>] [-CustomSeverity <SeverityType[]>]
 [-DateReleasedOrRevised <DateReleasedOrRevisedType>] [-UpdateDescription <String[]>] [-Language <String[]>]
 [-Required <String[]>] [-Severity <SeverityType[]>] [-Superseded <Boolean>] [-Title <String[]>]
 [-UpdateClassification <String[]>] [-Product <String[]>] [-MicrosoftAsVendor <Boolean>] [-RunType <RunType>]
 [-Schedule <IResultObject>] [-UseUtc <Boolean>] [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>]
 [-AvailableTimeUnit <TimeUnitType>] [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>]
 [-DeadlineTimeUnit <TimeUnitType>] [-UserNotification <UserNotificationType>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowRestart <Boolean>]
 [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>] [-WriteFilterHandling <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>] [-AlertTime <Int32>]
 [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-DeploymentPackageName <String>] [-DeploymentPackage <IResultObject>] [-DownloadFromInternet <Boolean>]
 [-Location <String>] [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>]
 [-LanguageSelection <String[]>] [-IsServicingPlan] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewByCollectionId
```
New-CMSoftwareUpdateAutoDeploymentRule -Name <String> [-Description <String>] -CollectionId <String>
 [-AddToExistingSoftwareUpdateGroup <Boolean>] [-EnabledAfterCreate <Boolean>] [-Enable <Boolean>]
 [-SendWakeupPacket <Boolean>] [-VerboseLevel <VerboseLevelType>] [-DeployWithoutLicense <Boolean>]
 [-ArticleId <String[]>] [-BulletinId <String[]>] [-CustomSeverity <SeverityType[]>]
 [-DateReleasedOrRevised <DateReleasedOrRevisedType>] [-UpdateDescription <String[]>] [-Language <String[]>]
 [-Required <String[]>] [-Severity <SeverityType[]>] [-Superseded <Boolean>] [-Title <String[]>]
 [-UpdateClassification <String[]>] [-Product <String[]>] [-MicrosoftAsVendor <Boolean>] [-RunType <RunType>]
 [-Schedule <IResultObject>] [-UseUtc <Boolean>] [-AvailableImmediately <Boolean>] [-AvailableTime <Int32>]
 [-AvailableTimeUnit <TimeUnitType>] [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>]
 [-DeadlineTimeUnit <TimeUnitType>] [-UserNotification <UserNotificationType>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowRestart <Boolean>]
 [-SuppressRestartServer <Boolean>] [-SuppressRestartWorkstation <Boolean>] [-WriteFilterHandling <Boolean>]
 [-GenerateSuccessAlert <Boolean>] [-SuccessPercentage <Int32>] [-AlertTime <Int32>]
 [-AlertTimeUnit <TimeUnitType>] [-DisableOperationManager <Boolean>]
 [-GenerateOperationManagerAlert <Boolean>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-UseBranchCache <Boolean>] [-DownloadFromMicrosoftUpdate <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-DeploymentPackageName <String>] [-DeploymentPackage <IResultObject>] [-DownloadFromInternet <Boolean>]
 [-Location <String>] [-DeploymentRing <DeploymentRing>] [-UpdateDeploymentWaitDay <Int32>]
 [-LanguageSelection <String[]>] [-IsServicingPlan] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSoftwareUpdateAutoDeploymentRule** cmdlet creates Microsoft System Center Configuration Manager deployment rules for automatic software updates.

System Center Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, System Center Configuration Manager adds updates that qualify for the rule to a software update group.
The System Center Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

## EXAMPLES

### Example 1: Create an automatic deployment rule
```
PS C:\>New-CMSoftwareUpdateAutoDeploymentRule -CollectionName "Desktops" -DeploymentPackageName "Updates123" -Name "DeploymentRule07" -ArticleId "117"
```

This command creates a deployment rule named DeploymentRule07 for the collection named Desktops and the deployment package named Updates123.
The rule deploys updates that have an article ID that contains 117.

### Example 2: Create an automatic deployment rule that uses a schedule
```
PS C:\>$Schedule = New-CMSchedule -DayOfWeek Wednesday
PS C:\> New-CMSoftwareUpdateAutoDeploymentRule -CollectionName "Laptops" -DeploymentPackageName "Updates235" -Name "DeploymentRule22" -AddToExistingSoftwareUpdateGroup $False -AlertTime 4 -AlertTimeUnit Weeks -AllowRestart $True -AllowSoftwareInstallationOutsideMaintenanceWindow $True -AllowUseMeteredNetwork $True -ArticleId "test" -AvailableImmediately $False -AvailableTime 5 -AvailableTimeUnit Months -CustomSeverity Critical -DateReleasedOrRevised Last1day -DeadlineImmediately $False -DeadlineTime $True -DeadlineTimeUnit Hours -DeployWithoutLicense $True -Description "Standard updates for our laptop systems." -DisableOperationManager $True -DownloadFromInternet $False -DownloadFromMicrosoftUpdate $True -EnabledAfterCreate $False -GenerateOperationManagerAlert $True -GenerateSuccessAlert $True -Language "Catalan" -LanguageSelection "English" -Location "\\k\aS_O15_Client_Dev_1" -MicrosoftAsVendor $True -NoInstallOnRemote $False -NoInstallOnUnprotected $True -RunType RunTheRuleOnSchedule -Schedule $Schedule -SendWakeUpPacket $True -SuccessPercent 99 -Superseded $True -SuppressRestartServer $True -SuppressRestartWorkstation $True -UpdateClassification "Critical Updates" -UseBranchCache $False -UserNotification DisplayAll -UseUtc $True -VerboseLevel AllMessages -WriteFilterHandling $True
```

This example creates an automatic deployment rule that uses a defined schedule.
Deployment occurs according to the schedule.

The first command creates a schedule for the Wednesday day of the week, and stores the schedule object in the $Schedule variable.
For more information, see help for **New-CMSchedule**.

The second command creates an automatic deployment rule for updates that uses the schedule object stored in the $Schedule variable.
This command specifies values for many parameters.

## PARAMETERS

### -AddToExistingSoftwareUpdateGroup


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

### -AlertTime


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AlertTimeUnit


```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases: 
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowRestart


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

### -AllowSoftwareInstallationOutsideMaintenanceWindow


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

### -AllowUseMeteredNetwork


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

### -ArticleId


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableImmediately


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

### -AvailableTime


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AvailableTimeUnit


```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases: 
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BulletinId


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection


```yaml
Type: IResultObject
Parameter Sets: NewByCollection
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId


```yaml
Type: String
Parameter Sets: NewByCollectionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName


```yaml
Type: String
Parameter Sets: NewByCollectionName
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

### -CustomSeverity


```yaml
Type: SeverityType[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Low, Moderate, Important, Critical

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DateReleasedOrRevised


```yaml
Type: DateReleasedOrRevisedType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Last1Hour, LastHour, Last2Hours, Last3Hours, Last4Hours, Last8Hours, Last12Hours, Last16Hours, Last20Hours, Last1Day, LastDay, Last2Days, Last3Days, Last4Days, Last5Days, Last6Days, Last7Days, Last14Days, Last21Days, Last28Days, LastMonth, Last1Month, Last2Months, Last3Months, Last4Months, Last5Months, Last6Months, Last7Months, Last8Months, Last9Months, Last10Months, Last11Months, Last1Year, LastYear, Last12Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeadlineImmediately


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

### -DeadlineTime


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeadlineTimeUnit


```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases: 
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeployWithoutLicense


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

### -DeploymentPackage


```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: InputObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeploymentPackageName


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

### -DeploymentRing


```yaml
Type: DeploymentRing
Parameter Sets: (All)
Aliases: 
Accepted values: CB, Release, BusinessMainstream, Cbb, Ltsb

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description


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

### -DisableOperationManager


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

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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

### -DownloadFromInternet


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

### -DownloadFromMicrosoftUpdate


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

### -Enable


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: Enabled, EnableDeployment

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnabledAfterCreate


```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableAfterCreate

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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

### -GenerateOperationManagerAlert


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

### -GenerateSuccessAlert


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

### -IsServicingPlan


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

### -Language


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Languages, UpdateLocales, UpdateLocale

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LanguageSelection


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location


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

### -MicrosoftAsVendor


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

### -Name


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

### -NoInstallOnRemote


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

### -NoInstallOnUnprotected


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

### -Product


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Required


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunType


```yaml
Type: RunType
Parameter Sets: (All)
Aliases: 
Accepted values: DoNotRunThisRuleAutomatically, RunTheRuleAfterAnySoftwareUpdatePointSynchronization, RunTheRuleOnSchedule

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule


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

### -SendWakeupPacket


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

### -Severity


```yaml
Type: SeverityType[]
Parameter Sets: (All)
Aliases: Severities
Accepted values: None, Low, Moderate, Important, Critical

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuccessPercentage


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Superseded


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

### -SuppressRestartServer


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

### -SuppressRestartWorkstation


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

### -Title


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Titles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateClassification


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: UpdateClassifications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateDeploymentWaitDay


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: UpdateDeploymentWaitDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateDescription


```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseBranchCache


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

### -UserNotification


```yaml
Type: UserNotificationType
Parameter Sets: (All)
Aliases: 
Accepted values: DisplayAll, DisplaySoftwareCenterOnly, HideAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VerboseLevel


```yaml
Type: VerboseLevelType
Parameter Sets: (All)
Aliases: 
Accepted values: OnlyErrorMessages, OnlySuccessAndErrorMessages, AllMessages

Required: False
Position: Named
Default value: None
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

### -WriteFilterHandling


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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMSoftwareUpdateAutoDeploymentRule](./Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](./Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](./Get-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](./Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](./Remove-CMSoftwareUpdateAutoDeploymentRule.md)

[Set-CMSoftwareUpdateAutoDeploymentRule](./Set-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSchedule](./New-CMSchedule.md)


