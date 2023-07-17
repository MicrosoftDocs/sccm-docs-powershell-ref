---
description: Modify an automatic deployment rule (ADR) for software updates.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/02/2021
schema: 2.0.0
title: Set-CMSoftwareUpdateAutoDeploymentRule
---

# Set-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Modify an automatic deployment rule (ADR) for software updates.

## SYNTAX

### SearchByNameMandatory (Default)
```
Set-CMSoftwareUpdateAutoDeploymentRule [-AddToExistingSoftwareUpdateGroup <Boolean>] [-AlertTime <Int32>]
 [-AlertTimeUnit <TimeUnitType>] [-AllowRestart <Boolean>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-Architecture <ArchitectureType[]>] [-ArticleId <String[]>] [-AvailableImmediately <Boolean>]
 [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>] [-BulletinId <String[]>] [-CMTag <CMTagTypes[]>]
 [-CollectionName <String>] [-ContentSize <String[]>] [-CustomSeverity <SeverityType[]>]
 [-DateReleasedOrRevised <DateReleasedOrRevisedType>] [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>]
 [-DeadlineTimeUnit <TimeUnitType>] [-DeploymentPackage <IResultObject>] [-DeploymentPackageName <String>]
 [-DeploymentRing <DeploymentRing>] [-DeployWithoutLicense <Boolean>] [-Description <String>]
 [-DisableOperationManager <Boolean>] [-DownloadFromInternet <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>] [-EnabledAfterCreate <Boolean>] [-Force]
 [-GenerateFailureAlert <Boolean>] [-GenerateOperationManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>]
 [-Language <String[]>] [-LanguageSelection <String[]>] [-Location <String>] [-MicrosoftAsVendor <Boolean>]
 -Name <String> [-NewName <String>] [-NoInstallOnRemote <Boolean>] [-NoInstallOnUnprotected <Boolean>]
 [-O365LanguageSelection <String[]>] [-PassThru] [-Product <String[]>] [-Required <String[]>]
 [-RequirePostRebootFullScan <Boolean>] [-RunType <RunType>] [-Schedule <IResultObject>]
 [-SendWakeupPacket <Boolean>] [-Severity <SeverityType[]>] [-SoftDeadlineEnabled <Boolean>]
 [-SuccessPercentage <Int32>] [-Superseded <Boolean>] [-SuppressRestartServer <Boolean>]
 [-SuppressRestartWorkstation <Boolean>] [-Title <String[]>] [-UpdateClassification <String[]>]
 [-UpdateDeploymentWaitDay <Int32>] [-UpdateDescription <String[]>] [-UseBranchCache <Boolean>]
 [-UserNotification <UserNotificationType>] [-UseUtc <Boolean>] [-Vendor <String[]>]
 [-VerboseLevel <VerboseLevelType>] [-WriteFilterHandling <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMSoftwareUpdateAutoDeploymentRule [-AddToExistingSoftwareUpdateGroup <Boolean>] [-AlertTime <Int32>]
 [-AlertTimeUnit <TimeUnitType>] [-AllowRestart <Boolean>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-Architecture <ArchitectureType[]>] [-ArticleId <String[]>] [-AvailableImmediately <Boolean>]
 [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>] [-BulletinId <String[]>] [-CMTag <CMTagTypes[]>]
 [-CollectionName <String>] [-ContentSize <String[]>] [-CustomSeverity <SeverityType[]>]
 [-DateReleasedOrRevised <DateReleasedOrRevisedType>] [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>]
 [-DeadlineTimeUnit <TimeUnitType>] [-DeploymentPackage <IResultObject>] [-DeploymentPackageName <String>]
 [-DeploymentRing <DeploymentRing>] [-DeployWithoutLicense <Boolean>] [-Description <String>]
 [-DisableOperationManager <Boolean>] [-DownloadFromInternet <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>] [-EnabledAfterCreate <Boolean>] [-Force]
 [-GenerateFailureAlert <Boolean>] [-GenerateOperationManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>]
 -Id <String[]> [-Language <String[]>] [-LanguageSelection <String[]>] [-Location <String>]
 [-MicrosoftAsVendor <Boolean>] [-NewName <String>] [-NoInstallOnRemote <Boolean>]
 [-NoInstallOnUnprotected <Boolean>] [-O365LanguageSelection <String[]>] [-PassThru] [-Product <String[]>]
 [-Required <String[]>] [-RequirePostRebootFullScan <Boolean>] [-RunType <RunType>] [-Schedule <IResultObject>]
 [-SendWakeupPacket <Boolean>] [-Severity <SeverityType[]>] [-SoftDeadlineEnabled <Boolean>]
 [-SuccessPercentage <Int32>] [-Superseded <Boolean>] [-SuppressRestartServer <Boolean>]
 [-SuppressRestartWorkstation <Boolean>] [-Title <String[]>] [-UpdateClassification <String[]>]
 [-UpdateDeploymentWaitDay <Int32>] [-UpdateDescription <String[]>] [-UseBranchCache <Boolean>]
 [-UserNotification <UserNotificationType>] [-UseUtc <Boolean>] [-Vendor <String[]>]
 [-VerboseLevel <VerboseLevelType>] [-WriteFilterHandling <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMSoftwareUpdateAutoDeploymentRule [-AddToExistingSoftwareUpdateGroup <Boolean>] [-AlertTime <Int32>]
 [-AlertTimeUnit <TimeUnitType>] [-AllowRestart <Boolean>]
 [-AllowSoftwareInstallationOutsideMaintenanceWindow <Boolean>] [-AllowUseMeteredNetwork <Boolean>]
 [-Architecture <ArchitectureType[]>] [-ArticleId <String[]>] [-AvailableImmediately <Boolean>]
 [-AvailableTime <Int32>] [-AvailableTimeUnit <TimeUnitType>] [-BulletinId <String[]>] [-CMTag <CMTagTypes[]>]
 [-CollectionName <String>] [-ContentSize <String[]>] [-CustomSeverity <SeverityType[]>]
 [-DateReleasedOrRevised <DateReleasedOrRevisedType>] [-DeadlineImmediately <Boolean>] [-DeadlineTime <Int32>]
 [-DeadlineTimeUnit <TimeUnitType>] [-DeploymentPackage <IResultObject>] [-DeploymentPackageName <String>]
 [-DeploymentRing <DeploymentRing>] [-DeployWithoutLicense <Boolean>] [-Description <String>]
 [-DisableOperationManager <Boolean>] [-DownloadFromInternet <Boolean>]
 [-DownloadFromMicrosoftUpdate <Boolean>] [-Enable <Boolean>] [-EnabledAfterCreate <Boolean>] [-Force]
 [-GenerateFailureAlert <Boolean>] [-GenerateOperationManagerAlert <Boolean>] [-GenerateSuccessAlert <Boolean>]
 -InputObject <IResultObject> [-Language <String[]>] [-LanguageSelection <String[]>] [-Location <String>]
 [-MicrosoftAsVendor <Boolean>] [-NewName <String>] [-NoInstallOnRemote <Boolean>]
 [-NoInstallOnUnprotected <Boolean>] [-O365LanguageSelection <String[]>] [-PassThru] [-Product <String[]>]
 [-Required <String[]>] [-RequirePostRebootFullScan <Boolean>] [-RunType <RunType>] [-Schedule <IResultObject>]
 [-SendWakeupPacket <Boolean>] [-Severity <SeverityType[]>] [-SoftDeadlineEnabled <Boolean>]
 [-SuccessPercentage <Int32>] [-Superseded <Boolean>] [-SuppressRestartServer <Boolean>]
 [-SuppressRestartWorkstation <Boolean>] [-Title <String[]>] [-UpdateClassification <String[]>]
 [-UpdateDeploymentWaitDay <Int32>] [-UpdateDescription <String[]>] [-UseBranchCache <Boolean>]
 [-UserNotification <UserNotificationType>] [-UseUtc <Boolean>] [-Vendor <String[]>]
 [-VerboseLevel <VerboseLevelType>] [-WriteFilterHandling <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMSoftwareUpdateAutoDeploymentRule** cmdlet modifies an automatic deployment rule (ADR) for software updates. To get an existing rule, use the [Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, Configuration Manager adds updates that qualify for the rule to a software update group.
The Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify the language selection and name of a rule

This command modifies the automatic deployment rule named **DeploymentRule07**. It specifies **Portuguese (Brazil)** for the Windows software update files that the site downloads. The command also changes the name of the rule to **DeploymentRule07Revised**.

```PowerShell
Set-CMSoftwareUpdateAutoDeploymentRule -Name "DeploymentRule07" -NewName "DeploymentRule07Revised" -Description "ADR downloads Portuguese (Brazil) files." -LanguageSelection "Portuguese (Brazil)"
```

### Example 2: Configure the deployment package

The following examples demonstrate different methods to configure the deployment package.

```PowerShell
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackageName $null
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackageName $packageName
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackage $null
Set-CMSoftwareUpdateAutoDeploymentRule -Name $ReferenceADRName -DeploymentPackage $package
```

### Example 3: Modify an ADR for multiple languages

This example changes the ADR to use the **Language** criteria for three languages: English, Hungarian, and Chinese (Simplified, PRC). It also changes to these languages for the Windows and Office 365 update binaries to download.

```powershell
Set-CMSoftwareUpdateAutoDeploymentRule -Name "Multi-language ADR" -Language "English","Hungarian","Chinese (Simplified, PRC)" -LanguageSelection "English","Hungarian","Chinese (Simplified, PRC)" -O365LanguageSelection "English (United States)","Hungarian (Hungary)","Chinese (Simplified, PRC)"
```

## PARAMETERS

### -AddToExistingSoftwareUpdateGroup

Indicates whether the rule adds to an existing update group. If this value is `$True`, each time the rule runs and finds new updates, it adds them to an existing update group. If this value is `$False`, it creates a new update group. Specify the existing update group or assign a name for the new update group by using the **DeploymentPackageName** parameter.

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

Specifies an integer offset from an update deployment deadline. The rule uses this value to specify when the rule generates alerts. Specify a time unit by using the **-AlertTimeUnit** parameter.

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

Specifies a unit of time for the **-AlertTime** parameter.

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

Indicates whether to allow a computer to restart if the update deployment takes place outside of a maintenance window. A maintenance window is a specified period of time used for computer maintenance and updates.

- If this value is `$True`, Configuration Manager restarts the computer, if necessary, to complete the update.
- If this value is `$False`, Configuration Manager doesn't restart the computer.

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

Indicates whether the update deployment takes place even if scheduled outside of a maintenance window. A maintenance window is a specified period of time used for computer maintenance and updates.

- If this value is `$True`, Configuration Manager deploys the update even the scheduled time falls outside the service window.
- If this value is `$False`, Configuration Manager doesn't deploy the update outside the service window. It waits until it can deploy in a service window.

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

Indicates whether to allow clients to download content over a metered internet connection after the deadline, which may incur additional expense.

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

### -Architecture

Use this parameter to set the **Architecture** property filter on the Software Updates page of the ADR properties.

```yaml
Type: ArchitectureType[]
Parameter Sets: (All)
Aliases: Architectures
Accepted values: Arm64, Itanium, X64, X86

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ArticleId

Specifies an array of criteria, as strings, for software updates. The rule adds software updates that have article IDs that meet specified criteria to the software update group.

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

Indicates whether this rule deploys updates as soon as the updates become available. If you select a value of `$False`, use the **-AvailableTime** and **-AvailableTimeUnit** parameters to specify how long after the rule runs to deploy the updates.

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

Specifies a period of time as an integer. Configuration Manager deploys the updates this long after the rule runs. Specify a time unit by using the **-AvailableTimeUnit** parameter.

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

Specifies a unit of time for the **-AvailableTime** parameter.

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

Specifies an array of criteria, as strings, for software updates. The rule adds software updates that have bulletin IDs that meet specified criteria to the software update group.

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

### -CMTag

This property is reserved for future use.

```yaml
Type: CMTagTypes[]
Parameter Sets: (All)
Aliases:
Accepted values: None, UUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify a collection name as the target for the automatic deployment rule.

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

### -ContentSize

Use this parameter to set the **Content Size (KB)** property filter on the Software Updates page of the ADR properties.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ContentSizes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomSeverity

Specifies an array of custom severity types for software updates. The rule adds software updates that have custom severity levels that meet specified criteria to the software update group.

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

Specifies a date released or revised for software updates. The rule adds software updates that have a date that meets specified criteria to the software update group.

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

Indicates whether to impose the deadline as soon as the rule runs. If you specify a value of `$False`, use the **-DeadlineTime** and **-DeadlineTimeUnit** parameters to specify how long after the rule runs to set the deadline. After the deadline, Configuration Manager installs required updates.

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

Specifies a period of time as an integer. The deadline for updates is this long after the rule runs. Specify a time unit by using the **-DeadlineTimeUnit** parameter.

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

Specifies a unit of time for the **-DeadlineTime** parameter.

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

### -DeploymentPackage

Use this parameter to set the deployment package for the existing software update auto deployment rule. To not require a package, set the value to `$null`.

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

### -DeploymentPackageName

Use this parameter to set the deployment package for the existing software update auto deployment rule. To not require a package, set the value to `$null`.

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

### -DeployWithoutLicense

Indicates whether the rule deploys updates without licenses.

- If you specify a value of `$True`, Configuration Manager deploys all updates for this rule and approves any license agreements.
- If this value is `$False`, Configuration Manager deploys only updates that don't include a license or for which the license agreement has been approved.

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

### -Description

Specifies a description for the automatic deployment rule for software updates.

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

Indicates whether to disable System Center Operations Manager alerts during software updates.

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

### -DownloadFromInternet

Indicates whether computers download software updates from the internet. If you specify a value of `$False`, specify an alternative location where computers can download updates by using the **-Location** parameter.

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

Indicates whether computers download content from Microsoft Update if that content is unavailable on a preferred distribution point of remote distribution point.

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

Specify whether the automatic deployment rule is enabled after you create it.

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

Indicates whether to enable software deployment for the associated software update group after this rule runs. If this value is `$False`, deploy the software update group manually.

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

### -GenerateFailureAlert

If the rule fails, create a Configuration Manager alert.

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

### -GenerateOperationManagerAlert

Indicates whether to generate Operations Manager alerts during a software update.

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

Indicates whether to generate an alert for successful deployment.

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

### -Id

Specify an array of automatic deployment rule IDs to configure. This value is the **AutoDeploymentID** property of the ADR object.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an automatic deployment rule object. To get an ADR object, use the [Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

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

### -Language

Specify a string array of language criteria for software updates. The rule adds software updates that have languages that meet specified criteria to the software update group.

Use the format of the language as displayed in the console. For example:

- `English`
- `Hungarian`
- `Chinese (Simplified, PRC)`

The format for the string array is: `"English","Hungarian","Chinese (Simplified, PRC)"`

> [!TIP]
> If you run this cmdlet on a computer where Windows has a localized UI, the language names may be different. For example, the English version of Windows uses "Danish", but the Danish version of Windows uses "Dansk".

This parameter overwrites any existing values with the values that you specify.

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

Specify a string array of languages. Clients download software updates available in the specified languages, and language-neutral updates.

Use the format of the language as displayed in the console. For example:

- `English`
- `Hungarian`
- `Chinese (Simplified, PRC)`

The format for the string array is: `"English","Hungarian","Chinese (Simplified, PRC)"`

> [!TIP]
> If you run this cmdlet on a computer where Windows has a localized UI, the language names may be different. For example, the English version of Windows uses "Danish", but the Danish version of Windows uses "Dansk".

This parameter overwrites any existing values with the values that you specify.

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

Specifies a location in your network where computers can download software updates. In order to use this location, specify a value of `$False` for the **-DownloadFromInternet** parameter.

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

Indicates whether the rule includes only updates that have Microsoft as the vendor.

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

Specifies a name for the automatic deployment rule for software updates.

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

### -NewName

Specify a new name for the ADR.

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

### -NoInstallOnRemote

Indicates whether to disallow installation of updates on remote systems.

- If you specify a value of `$True`, if the client is within a slow or unreliable network boundary, or when the client uses a fallback source location for content, then Configuration Manager doesn't install software updates.
- If you specify a value of `$False`, installation proceeds.


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

Indicates whether to disallow installation of updates on unprotected systems.

- If you specify a value of `$True`, if software updates aren't available on any preferred distribution points, Configuration Manager doesn't download and install software updates.
- If you specify a value of `$False`, installation proceeds.

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

### -O365LanguageSelection

Use this parameter to set the **Office 365 Client Update** language selection. Specify a string array of languages. Clients download software updates available in the specified languages, and language-neutral updates.

Use the format of the language as displayed in the console for the **Windows Update** language selection. This format is the same as the with the **LanguageSelection** parameter. For example:

- `English`
- `Hungarian`
- `Chinese (Simplified, PRC)`

The format for the string array is: `"English","Hungarian","Chinese (Simplified, PRC)"`

> [!TIP]
> If you run this cmdlet on a computer where Windows has a localized UI, the language names may be different. For example, the English version of Windows uses "Danish", but the Danish version of Windows uses "Dansk".

You currently can't specify with this parameter all of the languages that are available in the Configuration Manager console. For example, you can't specify "Irish (Ireland)" or "Maltese (Malta)".<!-- CMADO-7059972 -->

Starting in version 2103, you need to specify a language with a country/region name. This change aligns this parameter with the options in the Configuration Manager console. For example, `-O365LanguageSelection "English (United States)"`

This parameter overwrites any existing values with the values that you specify.

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

### -Product

Specifies an array of criteria, as strings, for software updates. The rule adds software updates for products that meet specified criteria to the software update group.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Products

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Required

Specifies an array of criteria, as strings, for software updates. The rule adds software updates identified by required that meet specified criteria to the software update group.

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

### -RequirePostRebootFullScan

Use this parameter to set the following option on the **User Experience** page of the ADR deployment settings: **If any update in this deployment requires a system restart, run updates deployment evaluation cycle after restart**.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RunEvaluationAfterRestart

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunType

Specify the recurring schedule for when the site evaluates the ADR.

If you specify `RunTheRuleOnSchedule`, specify a schedule by using the **-Schedule** parameter.

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

Specifies a schedule object for the deployment. To obtain a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet. Specify a schedule for this parameter if you specify a value of `RunTheRuleOnSchedule` for the **-RunType** parameter.

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

Indicates whether to send a wake up packet to computers before the deployment begins.

- If this value is `$True`, Configuration Manager wakes a computer from sleep.
- If this value is `$False`, it doesn't wake computers from sleep.

For computers to wake, you must first configure Wake On LAN.

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

Specifies an array of severity levels for software updates. The rule adds software updates for specified severity types to the software update group.

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

### -SoftDeadlineEnabled

Use this parameter to set the following option on the **Deployment Schedule** page of the ADR deployment settings: **Delay enforcement of this deployment according to user preferences, up to the grace period defined in client settings**.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DelayEnforcementAndUpToGracePeriod

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuccessPercentage

Specifies a percentage for client compliance as an integer from 0 to 99. If compliance falls below this percentage, Configuration Manager produces optional alerts.

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

Indicates whether the rule adds updates superseded by other updates.

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

Indicates whether to suppress a required update for a server. Some software updates require a system restart to complete the installation process.

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

Indicates whether to suppress a required update for a workstation. Some software updates require a system restart to complete the installation process.

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

Specifies an array of criteria, as strings, for software updates. The rule adds software updates that have titles that meet specified criteria to the software update group.

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

Specifies an array of criteria, as strings, for software updates. The rule adds software updates that have update classifications that meet specified criteria to the software update group.

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

Specifies an array of criteria, as strings, for software updates. The rule adds software updates that have update descriptions that meet specified criteria to the software update group.

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

Indicates whether to use Windows BranchCache for this update deployment. If you specify a value of `$True`, clients share content on the same subnet.

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

Specifies the type of user notification.

- `DisplayAll`: Display in Software Center and show all notifications.
- `DisplaySoftwareCenterOnly`: Display in Software Center, and only show notifications of computer restarts.
- `HideAll`: Hide in Software Center and all notifications.

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

### -UseUtc

Indicates whether to use Coordinated Universal Time (UTC).

- If this value is `$True`, Configuration Manager uses UTC for this deployment.
- If this value is `$False`, Configuration Manager uses local time.

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

### -Vendor
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: Vendors

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VerboseLevel

Specifies the level of detail you want clients to report for deployments that this rule creates.

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

### -WriteFilterHandling

Indicates whether to enable write filters for embedded devices.

- For a value of `$True`, the device commits changes during a maintenance window. This action requires a restart.
- For a value of `$False`, the device saves changes in an overlay and commits them later.

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

### System.Object
## NOTES

## RELATED LINKS

[Disable-CMSoftwareUpdateAutoDeploymentRule](Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSoftwareUpdateAutoDeploymentRule](New-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md)
