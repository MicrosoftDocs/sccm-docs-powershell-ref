---
title: Version 2002 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2002. 
ms.date: 03/20/2020
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Configuration Manager Cmdlet Library changes for version 2002

*Applies to: Configuration Manager (current branch)*

> [!NOTE]  
> Configuration Manager current branch version 110 is the baseline for these changes. For more information, see [Configuration Manager Cmdlet Library changes for version 1906](https://docs.microsoft.com/powershell/sccm/1910-release-notes).

## Important changes

### New cmdlets

#### New-CMSoftwareUpdatePhase

Use this cmdlet to create a deployment phase for software update.

``` PowerShell
New-CMSoftwareUpdatePhase `
 -CollectionName "MyCollection" `
 -PhaseName "MySUPhase"`
 -UserNotificationOption DisplaySoftwareCenterOnly
```

#### New-CMTaskSequencePhase

Use this cmdlet to create a deployment phase for a task sequence.

``` PowerShell
New-CMTaskSequencePhase -CollectionName "MyCollection" -PhaseName "MyTSPhase" -UserNotification DisplayAll -AllowRemoteDP $true
```

#### Get-CMPhase

Use this cmdlet to get the deployment phase for a specific instance or a phased deployment.

``` PowerShell
Get-CMPhase -Id "66DEDF86-D0CB-457D-88BE-47E3FAC92A47"
$myPhasedDeployment | Get-CMPhase
```

#### New-CMApplicationAutoPhasedDeployment

Use this cmdlet to create a phased deployment for an application by generating two phases with same settings.

``` PowerShell
New-CMApplicationAutoPhasedDeployment -ApplicationName "myApp" -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
 
$myApp | New-CMApplicationAutoPhasedDeployment -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

#### New-CMSoftwareUpdateAutoPhasedDeployment

Use this cmdlet to create a phased deployment for software updates by generating two phases with same settings.

``` PowerShell
New-CMSoftwareUpdateAutoPhasedDeployment -SoftwareUpdateName "myUpdateName" -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
$myUpdate | New-CMSoftwareUpdateAutoPhasedDeployment -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

#### New-CMSoftwareUpdateManualPhasedDeployment

Use this cmdlet to create a phased deployment for software updates. You'll need to add new customized deployment phases with the cmdlet New-CMSoftwareUpdatePhase first.

``` PowerShell
$phase1 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM001" -PhaseName "test01" -UserNotificationOption DisplaySoftwareCenterOnly
$phase2 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM003" -PhaseName "test02" -UserNotificationOption DisplaySoftwareCenterOnly
New-CMSoftwareUpdateManualPhasedDeployment -SoftwareUpdateNames ("myUpdateA", "myUpdateB") -Name "myPhaseDeployment" -AddPhases ($phase1, $phase2)
 
$phase3 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM001" -PhaseName "test03" -UserNotificationOption DisplaySoftwareCenterOnly
$phase4 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM003" -PhaseName "test04" -UserNotificationOption DisplaySoftwareCenterOnly
New-CMSoftwareUpdateManualPhasedDeployment -SoftwareUpdateGroupName "myGroup" -Name "myPhaseDeploymentForGroup" -AddPhases ($phase3, $phase4)
```

#### New-CMTaskSequenceAutoPhasedDeployment

Use this cmdlet to create a phased deployment for a task sequence by generating two phases with same settings.

``` PowerShell
New-CMTaskSequenceAutoPhasedDeployment -TaskSequenceName "myTaskSequenceName" -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
 
$myTS | New-CMTaskSequenceAutoPhasedDeployment -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

#### New-CMTaskSequenceManualPhasedDeployment

Use this cmdlet to create a phased deployment for a task sequence. You'll need to add new customized deployment phases with the cmdlet New-CMTaskSequencePhase first.

``` PowerShell
$phase1 = New-CMTaskSequencePhase -CollectionId "SMSDM001" -PhaseName "test01" -UserNotification DisplayAll
$phase2 = New-CMTaskSequencePhase -CollectionId "SMSDM003" -PhaseName "test02" -UserNotification HideAll
New-CMTaskSequenceManualPhasedDeployment -TaskSequenceName "myTaskSequence" -Name "phasedDeployment" -AddPhases ($phase1, $phase2)
 
$phase3 = New-CMTaskSequencePhase -CollectionId "SMSDM001" -PhaseName "test03" -UserNotification DisplayAll
$phase4 = New-CMTaskSequencePhase -CollectionId "SMSDM003" -PhaseName "test04" -UserNotification HideAll
$myTaskSequence | New-CMTaskSequenceManualPhasedDeployment -Name "phasedDeployment" -AddPhases ($phase3, $phase4)
```

#### Get-CMApplicationPhasedDeployment

Use this cmdlet to get the phased deployment for an application.

``` PowerShell
Get-CMApplicationPhasedDeployment -Name "myPhasedDeploymentName"
 
Get-CMApplicationPhasedDeployment -ApplicationName "myApplicationName"
```

#### Get-CMSoftwareUpdatePhasedDeployment

Use this cmdlet to get the phased deployment for software updates.

``` PowerShell
Get-CMSoftwareUpdatePhasedDeployment -Name "myPhasedDeploymentName"
 
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName "myUpdateName"
```

#### Get-CMTaskSequencePhasedDeployment

Use this cmdlet to get the phased deployment for a task sequence.

``` PowerShell
Get-CMTaskSequencePhasedDeployment -Name "myPhasedDeploymentName"
 
Get-CMTaskSequencePhasedDeployment -TaskSequenceName "myTaskSequenceName"
```

#### Get-CMPhasedDeploymentStatus

Use this cmdlet to get the status of a specific phased deployment.

``` PowerShell
Get-CMPhasedDeploymentStatus -Name "myPhasedDeploymentName"
 
$myPhasedDeployment | Get-CMPhasedDeploymentStatus -Catalog $catalog
```

#### Move-CMPhasedDeploymentToNext

Use this cmdlet to move the specified phased deployment to the next phase.

``` PowerShell
Move-CMPhasedDeploymentToNext -Name "myPhasedDeploymentName"  
 
$myPhasedDeployment | Move-CMPhasedDeploymentToNext -Force
```

#### Resume-CMPhasedDeployment

Use this cmdlet to resume the phased deployment from the suspend status.

``` PowerShell
Resume-CMPhasedDeployment -Name "myPhasedDeploymentName"  
 
$myPhasedDeployment | Resume-CMPhasedDeployment -Force
```

#### Suspend-CMPhasedDeployment

Use this cmdlet to suspend the specified phased deployment.

``` PowerShell
Suspend-CMPhasedDeployment -Name "myPhasedDeploymentName"
  
$myPhasedDeployment | Suspend-CMPhasedDeployment -Force
```

#### Remove-CMApplicationPhasedDeployment

Use this cmdlet to remove a phased deployment for an application.

``` PowerShell
Remove-CMApplicationPhasedDeployment -ApplicationName "myApplicationName"
 
Remove-CMApplicationPhasedDeployment -Name "myPhasedDeploymentName"
 
$myPhasedDeployment | Remove-CMApplicationPhasedDeployment -Force
```

#### Remove-CMSoftwareUpdatePhasedDeployment

Use this cmdlet to remove a phased deployment for software updates.

``` PowerShell
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName "mySoftwareUpdateName"
 
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupName "mySoftwareUpdateGroupName"
 
Remove-CMSoftwareUpdatePhasedDeployment -Name "myPhasedDeploymentName"
 
$myPhasedDeployment | Remove-CMSoftwareUpdatePhasedDeployment -Force
```

#### Remove-CMTaskSequencePhasedDeployment

Use this cmdlet to remove a phased deployment for a task sequence.

``` PowerShell
Remove-CMTaskSequencePhasedDeployment -TaskSequenceName "myTaskSequenceName"
 
Remove-CMTaskSequencePhasedDeployment -Name "myPhasedDeploymentName"
 
$myPhasedDeployment | Remove-CMTaskSequencePhasedDeployment -Force
```

#### Add-CMPassiveSite

Use this cmdlet to add a passive site.

```powershell
Add-CMPassiveSite -InputObject $SiteSystem -InstallDirectory $InstallPath -SourceFilePathOption CopySourceFileFromActiveSite
Add-CMPassiveSite -SiteCode $SiteCode -SiteSystemServerName $SiteSystemServerName -InstallDirectory $InstallPath -SourceFilePathOption UseLocalSourceDirectory -LocalSourceDirectory $LocalSourcePath
```

#### Get-CMThirdPartyUpdateCategory

Use this cmdlet to get third-party update categories.

```powershell
Get-CMThirdPartyUpdateCategory
Get-CMThirdPartyUpdateCategory -Catalog $catalog
Get-CMThirdPartyUpdateCategory -CatalogId $catalogId -Id $categoryId
Get-CMThirdPartyUpdateCategory -CatalogName $catalogName -Name $categoryName
$catalog | Get-CMThirdPartyUpdateCategory -ParentId $parentId -PublishOption $publishOption
```

#### Move-CMContentLibrary

Use this cmdlet to move the content library before adding a passive site.

```powershell
Move-CMContentLibrary -InputObject $Site -NewLocation $NewLocationPath
Move-CMContentLibrary -SiteCode $SiteCode -NewLocation $NewLocationPath
```

#### Set-CMThirdPartyUpdateCategory

Use this cmdlet to modify third-party update categories.

```powershell
Set-CMThirdPartyUpdateCategory -Catalog $catalog -Id $categoryId -PublishOption $publishOption -EnableCategories $true
$catalog | Set-CMThirdPartyUpdateCategory -Name $categoryName -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -CatalogId $catalogId -ParentId $parentId -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -CatalogName $catalogName -Name $categoryName -ParentId $parentId -PublishOption $publishOption -EnableCategories $true
Set-CMThirdPartyUpdateCategory -Categories $categories -PublishOption $publishOption -EnableCategories $true
```

### Deprecated cmdlets

None

## Known issues

None

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
#### Breaking changes
#### Bugs that were fixed
#### Non-breaking changes
#### Deprecations
-->

### Add-CMDeviceCollectionQueryMembershipRule

#### Non-breaking changes

Added more error handling for the query rule.

### Add-CMMsiDeploymentType

#### Non-breaking changes

Added the following new parameters to allow you to configure the repair command and directory options when creating deployment type:
- RepareCommand
- RepairWorkingDirectory

#### Bugs that were fixed

Missing parameters to configure repair command and directory option when creating deployment type.

### Add-CMScriptDeploymentTypes

#### Breaking changes

The -ContentLocation will no longer accept an empty folder.

#### Bugs that were fixed

The -ContentLocation shouldn't allow an empty folder.
 
### Add-CMUserCollectionQueryMembershipRule

#### Non-breaking changes

Added more error handling for the query rule.

### Import-CMSoftwareLicense

#### Non-breaking changes

Fixed a parameter bounding issue for -Timeout.

### New-CMApplicationDeployment

#### Non-breaking changes

Added the following new parameter to allow you to configure the repair application option when creating a deployment for an application:
- AllowRepairApp

#### Bugs that were fixed

Missing parameter to configure repair application option when creating deployment for application.

### New-CMSiteSystem

#### Non-breaking changes

Corrected the validation for the -SiteSystemServerName and -PublicFqdn.

#### Bugs that were fixed

Wrong limitation for the specified -SiteSystemServerName and -PublicFqdn.

### New-CMTSRule

#### Non-breaking changes

The -ReferencedVariableName now accept variable name that begins with underscore.

#### Bugs that were fixed

The -ReferencedVariableName doesn't allow user to specify variable name that begins with underscore.

### Set-CMApplicationDeployment

#### Non-breaking changes

Added the following new parameter to allow you to configure the repair application option when you set the deployment for an application:
- AllowRepairApp

#### Bugs that were fixed

Missing parameter to configure repair application option when set deployment for application.

### Set-CMMsiDeploymentType

#### Non-breaking changes

Added the following new parameters to allow you to configure repair command and directory options when you set the deployment type:
- RepareCommand
- RepairWorkingDirectory

#### Bugs that were fixed

Missing parameters to configure repair command and directory option when set deployment type.

### Set-CMSite

#### Non-breaking changes

Added the following new parameter to allow you to retry the installation for a failed passive site:
- RetryInstallPassiveSite

Added the following new parameter to allow you to promote a passive site to active:
- PromotePassiveSiteToActive

### Set-CMScriptDeploymentTypes

#### Breaking changes

The -ContentLocation will no longer accept an empty folder.

#### Bugs that were fixed

The -ContentLocation shouldn't allow an empty folder.

### Set-CMThirdPartyUpdateCatalog

#### Non-breaking changes

- The cmdlet now supports setting 'Sync Schedule' for a catalog.
- Modified an internal function call due to a native method change.

##### Example

```PowerShell
Set-CMThirdPartyUpdateCatalog -Name $name –Schedule $schedule
```

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To submit bug reports, use [send a smile in the Configuration Manager console](https://docs.microsoft.com/sccm/core/understand/find-help#product-feedback). For new feature requests, use [UserVoice](https://configurationmanager.uservoice.com).
