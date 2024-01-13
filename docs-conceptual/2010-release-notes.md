---
title: Version 2010 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 2010. 
ms.date: 12/21/2020
ms.topic: conceptual
ms.localizationpriority: low
ms.author: banreetkaur
author: Banreet
manager: apoorvseth
ROBOTS: NOINDEX
---

# Configuration Manager cmdlet library changes for version 2010

*Applies to: Configuration Manager (current branch)*

These release notes summarize changes to the Configuration Manager cmdlet library in version 2010.

Starting in version 2010, the Configuration Manager PowerShell cmdlet library now offers support for PowerShell 7. For more information, see [Support for PowerShell version 7](overview.md#support-for-powershell-version-7).<!--6023299-->

> [!NOTE]  
> Configuration Manager current branch version 2002 is the baseline for these changes. For more information, see [Configuration Manager cmdlet library changes for version 2006](2006-release-notes.md).

## Cloud management gateway

<!--6978300-->

With more customers managing remote devices now, this release includes several new and improved Windows PowerShell cmdlets for the [cloud management gateway (CMG)](/mem/configmgr/core/clients/manage/cmg/overview). You can use these cmdlets to automate the creation, configuration, and management of the CMG service and Azure Active Directory (Azure AD) requirements.

> [!NOTE]
> While some of the new cmdlets might work with other Azure services, they're only tested with the **Cloud management** connection to support the CMG.

For example, an Azure administrator first creates the two required apps in Azure Active Directory (Azure AD). Then you write a script that uses the following cmdlets to deploy a CMG:

1. **Import-CMAADServerApplication**: Create the Azure AD server app definition in Configuration Manager.
1. **Import-CMAADClientApplication**: Create the Azure AD client app definition in Configuration Manager.
1. Use **Get-CMAADApplication** to get the app objects, and then pass to **New-CMCloudManagementAzureService** to create the Azure service connection in Configuration Manager.
1. **New-CMCloudManagementGateway**: Create the CMG service in Azure.
1. **Add-CMCloudManagementGatewayConnectionPoint**: Create the CMG connection point site system.

### New cmdlets for CMG

- [Get-CMAADApplication](/powershell/module/configurationmanager/Get-CMAADApplication): Get the Azure Active Directory (Azure AD) app object from the site.
- [Get-CMAzureService](/powershell/module/configurationmanager/Get-CMAzureService): Get the Azure service.
- [Import-CMAADClientApplication](/powershell/module/configurationmanager/Import-CMAADClientApplication): Import the client app from Azure AD, and define it for the Configuration Manager site.
- [Import-CMAADServerApplication](/powershell/module/configurationmanager/Import-CMAADServerApplication): Import the web/server app from Azure AD, and define it for the Configuration Manager site.
- [New-CMCloudManagementAzureService](/powershell/module/configurationmanager/New-CMCloudManagementAzureService): Create the Azure service for **Cloud Management** in Configuration Manager.
- [Remove-CMAzureService](/powershell/module/configurationmanager/Remove-CMAzureService): Remove the Azure service.
- [Set-CMCloudManagementAzureService](/powershell/module/configurationmanager/Set-CMCloudManagementAzureService): Modify the settings of the Azure service for **Cloud Management** in Configuration Manager.

### Updated cmdlets for CMG

The following existing cmdlets have significant improvements. For more information, see the following release notes:

- [New-CMCloudManagementGateway](#new-cmcloudmanagementgateway)
- [Set-CMCloudManagementGateway](#set-cmcloudmanagementgateway)

### Existing cmdlets for CMG

You can continue to use the following existing CMG cmdlets:

- [Add-CMCloudManagementGatewayConnectionPoint](/powershell/module/configurationmanager/Add-CMCloudManagementGatewayConnectionPoint)
- [Get-CMCloudManagementGateway](/powershell/module/configurationmanager/Get-CMCloudManagementGateway)
- [Get-CMCloudManagementGatewayConnectionPoint](/powershell/module/configurationmanager/Get-CMCloudManagementGatewayConnectionPoint)
- [New-CMCloudManagementGateway](/powershell/module/configurationmanager/New-CMCloudManagementGateway)
- [Remove-CMCloudManagementGateway](/powershell/module/configurationmanager/Remove-CMCloudManagementGateway)
- [Remove-CMCloudManagementGatewayConnectionPoint](/powershell/module/configurationmanager/Remove-CMCloudManagementGatewayConnectionPoint)
- [Set-CMCloudManagementGateway](/powershell/module/configurationmanager/Set-CMCloudManagementGateway)
- [Set-CMCloudManagementGatewayConnectionPoint](/powershell/module/configurationmanager/Set-CMCloudManagementGatewayConnectionPoint)
- [Start-CMCloudManagementGateway](/powershell/module/configurationmanager/Start-CMCloudManagementGateway)
- [Stop-CMCloudManagementGateway](/powershell/module/configurationmanager/Stop-CMCloudManagementGateway)

## New cmdlets

<!-- - [<cmdlet>](/powershell/module/configurationmanager/) -->

### Application management

- [Add-CMCIDetectionMethod](/powershell/module/configurationmanager/Add-CMCIDetectionMethod): Specify how the client detects an application.
- [Get-CMApplicationGroupDeployment](/powershell/module/configurationmanager/Get-CMApplicationGroupDeployment): Get the deployment of an application group.
- [New-CMApplicationGroupDeployment](/powershell/module/configurationmanager/New-CMApplicationGroupDeployment): Create a deployment for an application group.
- [Remove-CMApplicationGroupDeployment](/powershell/module/configurationmanager/Remove-CMApplicationGroupDeployment): Remove the deployment of an application group.
- [Set-CMApplicationGroupDeployment](/powershell/module/configurationmanager/Set-CMApplicationGroupDeployment): Configure the deployment of an application group.

### Collection management

- [Get-CMCollectionDependency](/powershell/module/configurationmanager/Get-CMCollectionDependency): Get the limiting collection for the target collection.
- [Get-CMCollectionDependent](/powershell/module/configurationmanager/Get-CMCollectionDependent): Get a collection's dependent relationships.
- [Get-CMCollectionEvaluationStatus](/powershell/module/configurationmanager/Get-CMCollectionEvaluationStatus): Get the status of collection evaluation.
- [Get-CMCollectionFullEvaluationStatus](/powershell/module/configurationmanager/Get-CMCollectionFullEvaluationStatus): Get the full evaluation status for a collection.
- [Get-CMCollectionIncrementalEvaluationStatus](/powershell/module/configurationmanager/Get-CMCollectionIncrementalEvaluationStatus): Get the incremental evaluation status for a collection.
- [Get-CMCollectionInfoFromEvaluationQueue](/powershell/module/configurationmanager/Get-CMCollectionInfoFromEvaluationQueue): Get collection information from the evaluation queue.
- [Get-CMCollectionInfoFromFullEvaluationQueue](/powershell/module/configurationmanager/Get-CMCollectionInfoFromFullEvaluationQueue): Get collection information from the full evaluation queue.
- [Get-CMCollectionInfoFromIncrementalEvaluationQueue](/powershell/module/configurationmanager/Get-CMCollectionInfoFromIncrementalEvaluationQueue): Get collection information from the incremental evaluation queue.
- [Get-CMCollectionInfoFromManualEvaluationQueue](/powershell/module/configurationmanager/Get-CMCollectionInfoFromManualEvaluationQueue): Get collection information from the manual evaluation queue.
- [Get-CMCollectionInfoFromNewEvaluationQueue](/powershell/module/configurationmanager/Get-CMCollectionInfoFromNewEvaluationQueue): Get collection information from the new evaluation queue.

### Windows 10 edition upgrade

- [New-CMWindows10EditionUpgrade](/powershell/module/configurationmanager/new-CMWindows10EditionUpgrade): Create a Windows 10 edition upgrade policy.
- [Remove-CMWindows10EditionUpgrade](/powershell/module/configurationmanager/Remove-CMWindows10EditionUpgrade): Remove a Windows 10 edition upgrade policy.
- [Set-CMWindows10EditionUpgrade](/powershell/module/configurationmanager/Set-CMWindows10EditionUpgrade): Configure a Windows 10 edition upgrade policy.

### Microsoft Edge browser profiles

- [Get-CMMicrosoftEdgeBrowserProfiles](/powershell/module/configurationmanager/Get-CMMicrosoftEdgeBrowserProfiles): Get a policy for a Microsoft Edge Legacy browser profile.
- [New-CMMicrosoftEdgeBrowserProfiles](/powershell/module/configurationmanager/New-CMMicrosoftEdgeBrowserProfiles): Create a policy to manage Microsoft Edge Legacy browser settings.
- [Set-CMMicrosoftEdgeBrowserProfiles](/powershell/module/configurationmanager/Set-CMMicrosoftEdgeBrowserProfiles): Configure a policy for a Microsoft Edge Legacy browser profile.

### OneDrive for Business profiles

- [Get-CMOneDriveBusinessProfile](/powershell/module/configurationmanager/Get-CMOneDriveBusinessProfile): Get a policy for a OneDrive for Business profile.
- [New-CMOneDriveBusinessProfile](/powershell/module/configurationmanager/New-CMOneDriveBusinessProfile): Create a OneDrive for Business profile policy.
- [Set-CMOneDriveBusinessProfile](/powershell/module/configurationmanager/Set-CMOneDriveBusinessProfile): Configure a OneDrive for Business profile policy.

## Deprecated and removed cmdlets

The following cmdlets for Configuration Manager hybrid environments are no longer available:

- Add-CMAndroidDeploymentType
- Add-CMGooglePlayDeploymentType
- Add-CMIosAppStoreDeploymentType
- Add-CMIosDeploymentType
- Set-CMAndroidDeploymentType
- Set-CMGooglePlayDeploymentType
- Set-CMIosAppStoreDeploymentType
- Set-CMIosDeploymentType

For more information, see [What happened to hybrid MDM?](/mem/configmgr/mdm/understand/what-happened-to-hybrid)

The following cmdlet is deprecated:

- [Set-CMClientSetting](/powershell/module/configurationmanager/Set-CMClientSetting)

## Known issues

None

## Cmdlet changes

The following changes have been made to existing cmdlets in this version. Changes may be new functionality, bug fixes, or deprecation. Some changes may be breaking. If you use one of the cmdlets or feature areas listed in this section, carefully review the changes to understand how they may affect your use.

<!-- Template
### Cmdlet name
For more information, see [](/powershell/module/configurationmanager/).
**Breaking changes**
**Bugs that were fixed**
**Non-breaking changes**
**Deprecations**
-->

### Add-CMComplianceSettingRegistryKeyValue

For more information, see [Add-CMComplianceSettingRegistryKeyValue](/powershell/module/configurationmanager/Add-CMComplianceSettingRegistryKeyValue).

**Non-breaking changes**

Parameter **ExpectedValue** can accept an empty value.

### Add-CMDistributionPoint

For more information, see [Add-CMDistributionPoint](/powershell/module/configurationmanager/Add-CMDistributionPoint).

**Bugs that were fixed**

Fixed an issue for distribution point creation.

### Add-CMDeviceCollectionDirectMembershipRule

For more information, see [Add-CMDeviceCollectionDirectMembershipRule](/powershell/module/configurationmanager/Add-CMDeviceCollectionDirectMembershipRule).

**Bugs that were fixed**

Fixed an issue for duplicated device number check.

### Add-CMManagementPoint

For more information, see [Add-CMManagementPoint](/powershell/module/configurationmanager/Add-CMManagementPoint).

**Bugs that were fixed**

Fixed an issue for cloud management gateway support.

### Add-CMPassiveSite

For more information, see [Add-CMPassiveSite](/powershell/module/configurationmanager/Add-CMPassiveSite).

**Bugs that were fixed**

Fixed an issue for passive site in hierarchy.

### Add-CMTaskSequenceStep

For more information, see [Add-CMTaskSequenceStep](/powershell/module/configurationmanager/Add-CMTaskSequenceStep).

**Bugs that were fixed**

Fixed a policy size issue when using multiple PowerShell steps that contain large scripts.

### Add-CMWindowsAppxDeploymentType

For more information, see [Add-CMWindowsAppxDeploymentType](/powershell/module/configurationmanager/Add-CMWindowsAppxDeploymentType).

**Non-breaking changes**

Added function to support MSIX.

### Approve-CMDevice

For more information, see [Approve-CMDevice](/powershell/module/configurationmanager/Approve-CMDevice).

**Non-breaking changes**

Fixed an issue when working with **Get-CMDevice**.

### Enable-CMSiteFeature

For more information, see [Enable-CMSiteFeature](/powershell/module/configurationmanager/Enable-CMSiteFeature).

**Non-breaking changes**

Added new flags to support cloud features.

### Get-CMScript

For more information, see [Get-CMScript](/powershell/module/configurationmanager/Get-CMScript).

**Non-breaking changes**

Added new parameter **ScriptGuid** to support query by script GUID.

### Get-CMSiteFeature

For more information, see [Get-CMSiteFeature](/powershell/module/configurationmanager/Get-CMSiteFeature).

**Non-breaking changes**

Added new flags to support cloud features.

### Get-CMSoftwareUpdate

For more information, see [Get-CMSoftwareUpdate](/powershell/module/configurationmanager/Get-CMSoftwareUpdate).

**Non-breaking changes**

Added new parameter **Vendor** to specify the source of the software update.

**Example:**

```powershell
Get-CMSoftwareUpdate -Name $Update -Vendor "Microsoft​"
```

### Get-CMStatusMessageQuery

For more information, see [Get-CMStatusMessageQuery](/powershell/module/configurationmanager/Get-CMStatusMessageQuery).

**Bugs that were fixed**

Fixed an issue for parameter **ShowMessage**.

### Import-CMDriver

For more information, see [Import-CMDriver](/powershell/module/configurationmanager/Import-CMDriver).

**Non-breaking changes**

Added new parameter **AdministrativeCategoryName** to specify a name for the driver category.

**Example:**

```PowerShell
Import-CMDriver -UncFileLocation $DriverFolder -ImportFolder -ImportDuplicateDriverOption AppendCategory -AdministrativeCategory "Video drivers"
```

### Invoke-CMAnalyzePackage

For more information, see [Invoke-CMAnalyzePackage](/powershell/module/configurationmanager/Invoke-CMAnalyzePackage).

**Breaking changes**

Removed **Package** parameter. Pipe the package object, or use the **InputObject** parameter.

**Non-breaking changes**

Added pipeline support and the **InputObject** parameter.

**Example:**

```PowerShell
$pkg | Invoke-CMAnalyzePackage
```

### Invoke-CMClientAction

For more information, see [Invoke-CMClientAction](/powershell/module/configurationmanager/Invoke-CMClientAction).

**Bugs that were fixed**

Fixed pipeline issue for parameter **Collection**.

**Example:**

```PowerShell
Get-CMCollection -Name "deviceCol1" | Invoke-CMClientAction -ActionType ClientNotificationRequestUsersPolicyNow
```

### Invoke-CMConvertPackage

For more information, see [Invoke-CMConvertPackage](/powershell/module/configurationmanager/Invoke-CMConvertPackage).

**Breaking changes**

Removed **Package** parameter. Pipe the package object, or use the **InputObject** parameter.

**Non-breaking changes**

Added pipeline support and the **InputObject** parameter.

**Example:**

```powershell
$pkg | Invoke-CMConvertPackage
```

### Invoke-CMReport

For more information, see [Invoke-CMReport](/powershell/module/configurationmanager/Invoke-CMReport).

**Bugs that were fixed**

Fixed an issue for parameter **Path**.

### Invoke-CMScript

For more information, see [Invoke-CMScript](/powershell/module/configurationmanager/Invoke-CMScript).

**Non-breaking changes**

Add parameter **ScriptParameter** to pass parameters to the target script.

**Example:**

```PowerShell
$Hash = @{"FolderName"="c:\test\test1"; "FileName"="test2"}

Invoke-CMScript -ScriptGuid $scriptGuid -Device (Get-CMDevice -Name $targetPCName) -ScriptParameter $Hash
```

### New-CMBMSClientConfigureCheckIntervalPolicy

For more information, see [New-CMBMSClientConfigureCheckIntervalPolicy](/powershell/module/configurationmanager/New-CMBMSClientConfigureCheckIntervalPolicy).

**Bugs that were fixed**

Fixed an issue when creating a new policy setting instance.

### New-CMBoundary

For more information, see [New-CMBoundary](/powershell/module/configurationmanager/New-CMBoundary).

**Non-breaking changes**

Added VPN option in BoundaryType parameter.

### New-CMBootableMedia

For more information, see [New-CMBootableMedia](/powershell/module/configurationmanager/New-CMBootableMedia).

**Non-breaking changes**

Add parameter **SiteCode**.

### New-CMCloudManagementGateway

For more information, see [New-CMCloudManagementGateway](/powershell/module/configurationmanager/New-CMCloudManagementGateway).

**Non-breaking changes**

The following parameters are new:

- CARootCert
- EnableCloudDPFunction
- EnableStorageQuota
- EnableTrafficOut
- EnforceProtocol
- Force
- GroupName
- IsUsingExistingGroup
- ServerAppClientID
- ServiceCertPassword
- ServiceCertPath
- ServiceName
- StorageCriticalPct
- StorageQuotaGB
- StorageWarningPct
- TrafficOutStopService

The following parameters are updated:

- CheckClientCertRevocation
- EnvironmentSetting
- Region
- SubscriptionId
- TrafficCriticalPct
- TrafficWarningPct

**Breaking changes**

The following parameters are removed from this cmdlet:

- GovernmentSubscription
- ManagementCertificatePassword
- ManagementCertificatePath
- PassThru
- RootCertificatePath
- ServiceCertificatePassword
- ServiceCertificatePath
- ServiceCName

### New-CMCoManagementPolicy

For more information, see [New-CMCoManagementPolicy](/powershell/module/configurationmanager/New-CMCoManagementPolicy).

**Non-breaking changes**

Added multi-session applicability

Added ARM64 applicability

### New-CMComplianceRuleFileFolderDate

For more information, see [New-CMComplianceRuleFileFolderDate](/powershell/module/configurationmanager/New-CMComplianceRuleFileFolderDate).

**Non-breaking changes**

Adjusted the cmdlet logic to process the values from parameters **Modification** and **Creation** to align with other cmdlets.

### New-CMComplianceRuleFileFolderSimple

For more information, see [New-CMComplianceRuleFileFolderSimple](/powershell/module/configurationmanager/New-CMComplianceRuleFileFolderSimple).

**Breaking changes**

Changed the type of the parameter **PropertyType** from _FileFolderProperty_ to _SimpleFileFolderProperty_ type.

### New-CMDetectionClauseDirectory

For more information, see [New-CMDetectionClauseDirectory](/powershell/module/configurationmanager/New-CMDetectionClauseDirectory).

**Breaking changes**

Changed the type of the parameter **ExpressionOperator** from _RuleExpressionOperator_ to _FileFolderRuleExpressionOperator_ type.

### New-CMDetectionClauseFile

For more information, see [New-CMDetectionClauseFile](/powershell/module/configurationmanager/New-CMDetectionClauseFile).

**Breaking changes**

Changed the type of the parameter **ExpressionOperator** from _RuleExpressionOperator_ to _FileFolderRuleExpressionOperator_ type.

### New-CMDetectionClauseMacBundle

For more information, see [New-CMDetectionClauseMacBundle](/powershell/module/configurationmanager/New-CMDetectionClauseMacBundle).

**Breaking changes**

Changed the type of the parameter **ExpressionOperator** from _RuleExpressionOperator_ to _MacRuleExpressionOperator_ type.

**Bugs that were fixed**

Fixed an issue for parameter **PropertyType**.

### New-CMDetectionClauseMacPackage

For more information, see [New-CMDetectionClauseMacPackage](/powershell/module/configurationmanager/New-CMDetectionClauseMacPackage).

**Breaking changes**

Changed the type of the parameter **ExpressionOperator** from _RuleExpressionOperator_ to _MacRuleExpressionOperator_ type.

### New-CMDetectionClauseRegistryKeyValue

For more information, see [New-CMDetectionClauseRegistryKeyValue](/powershell/module/configurationmanager/New-CMDetectionClauseRegistryKeyValue).

**Breaking changes**

Changed the type of the parameter **ExpressionOperator** from _RuleExpressionOperator_ to _RegistryValueRuleExpressionOperator_ type.

### New-CMDetectionClauseWindowsInstaller

For more information, see [New-CMDetectionClauseWindowsInstaller](/powershell/module/configurationmanager/New-CMDetectionClauseWindowsInstaller).

**Breaking changes**

Changed the type of the parameter **ExpressionOperator** from _RuleExpressionOperator_ to _WindowsInstallerRuleExpressionOperator_ type.

### New-CMDriverPackage

For more information, see [New-CMDriverPackage](/powershell/module/configurationmanager/New-CMDriverPackage).

**Bugs that were fixed**

Fixed an issue for parameter **DriverModel**.

### New-CM*PhasedDeployment

For more information, see the following articles:

- [New-CMApplicationAutoPhasedDeployment](/powershell/module/configurationmanager/New-CMApplicationAutoPhasedDeployment)
- [New-CMSoftwareUpdateAutoPhasedDeployment](/powershell/module/configurationmanager/New-CMSoftwareUpdateAutoPhasedDeployment)
- [New-CMSoftwareUpdateManualPhasedDeployment](/powershell/module/configurationmanager/New-CMSoftwareUpdateManualPhasedDeployment)
- [New-CMTaskSequenceAutoPhasedDeployment](/powershell/module/configurationmanager/New-CMTaskSequenceAutoPhasedDeployment)
- [New-CMTaskSequenceManualPhasedDeployment](/powershell/module/configurationmanager/New-CMTaskSequenceManualPhasedDeployment)

**Bugs that were fixed**

Fixed an issue for parameter **WhatIf**.

**Non-breaking changes**

Added validation for duplicated phase name.

### New-CMPrestageMedia

For more information, see [New-CMPrestageMedia](/powershell/module/configurationmanager/New-CMPrestageMedia).

**Non-breaking changes**

Add parameter **SiteCode**.

### New-CMProgram

For more information, see [New-CMProgram](/powershell/module/configurationmanager/New-CMProgram).

**Breaking changes**

Renamed the type `RenameWithUnc` to `RunWithUnc` for parameter **DriveMode**.

### New-CMSoftwareUpdateDeployment

For more information, see [New-CMSoftwareUpdateDeployment](/powershell/module/configurationmanager/New-CMSoftwareUpdateDeployment).

**Non-breaking changes**

Added new parameter **DeployWithNoPackage** for non-downloaded software update.

### New-CMStandaloneMedia

For more information, see [New-CMStandaloneMedia](/powershell/module/configurationmanager/New-CMStandaloneMedia).

**Bugs that were fixed**

Fixed an issue for parameter **PrestartPackage**

### New-CMTaskSequence

For more information, see [New-CMTaskSequence](/powershell/module/configurationmanager/New-CMTaskSequence).

**Bugs that were fixed**

Fixed a policy size issue when you use multiple PowerShell steps that contain large scripts.

### New-CMTaskSequenceDeployment

For more information, see [New-CMTaskSequenceDeployment](/powershell/module/configurationmanager/New-CMTaskSequenceDeployment).

**Bugs that were fixed**

Fixed an issue for parameter **AllowFallback**.

**Non-breaking changes**

Added validation for parameter **Schedule** to avoid duplicated value with existing assignment.

### New-CMTaskSequenceMedia

For more information, see [New-CMTaskSequenceMedia](/powershell/module/configurationmanager/New-CMTaskSequenceMedia).

**Non-breaking changes**

Changed timeout in media creation from one day to three days.

### New-CMTSPartitionSetting

For more information, see [New-CMTSPartitionSetting](/powershell/module/configurationmanager/New-CMTSPartitionSetting).

**Bugs that were fixed**

Fixed an issue for parameter **EnableQuickFormat**.

### New-CMTSStepEnableBitLocker

For more information, see [New-CMTSStepEnableBitLocker](/powershell/module/configurationmanager/New-CMTSStepEnableBitLocker).

**Bugs that were fixed**

Fixed an issue for user-specified encryption method.

### New-CMTSStepOfflineEnableBitLocker

For more information, see [New-CMTSStepOfflineEnableBitLocker](/powershell/module/configurationmanager/New-CMTSStepOfflineEnableBitLocker).

**Bugs that were fixed**

Fixed an issue for user-specified encryption method.

### New-CMTSStepPreStartCheck

For more information, see [New-CMTSStepPreStartCheck](/powershell/module/configurationmanager/New-CMTSStepPreStartCheck).

**Bugs that were fixed**

Fixed an issue for new check readiness step.

Fixed an issue for parameter **OSLanguageId**.

**Non-breaking changes**

Add a new parameter for UEFI check, **CheckUefi**.

### Remove-CMTaskSequenceGroup

For more information, see [Remove-CMTaskSequenceGroup](/powershell/module/configurationmanager/Remove-CMTaskSequenceGroup).

**Bugs that were fixed**

Fixed a policy size issue when you use multiple PowerShell steps that contain large scripts.

### Set-CM*PhasedDeployment

For more information, see the following articles:

- [Set-CMApplicationPhasedDeployment](/powershell/module/configurationmanager/Set-CMApplicationPhasedDeployment)
- [Set-CMSoftwareUpdatePhasedDeployment](/powershell/module/configurationmanager/Set-CMSoftwareUpdatePhasedDeployment)
- [Set-CMTaskSequencePhasedDeployment](/powershell/module/configurationmanager/Set-CMTaskSequencePhasedDeployment)

**Bugs that were fixed**

Fixed an issue for parameter **WhatIf**.

### Set-CMBoundary

For more information, see [Set-CMBoundary](/powershell/module/configurationmanager/Set-CMBoundary).

**Non-breaking changes**

Added `VPN` option in **BoundaryType**.

### Set-CMClientSettingComputerRestart

For more information, see [Set-CMClientSettingComputerRestart](/powershell/module/configurationmanager/Set-CMClientSettingComputerRestart).

**Non-breaking changes**

Added a new parameter **NoRebootEnforcement**.

### Set-CMClientSettingSoftwareUpdate

For more information, see [Set-CMClientSettingSoftwareUpdate](/powershell/module/configurationmanager/Set-CMClientSettingSoftwareUpdate).

**Non-breaking changes**

Added parameters:

- **EnableInstallation**
- **ThreadPriority**
- **EnableDynamicUpdate**

**Example:**

```powershell
Set-CMClientSettingSoftwareUpdate -InputObject $testsetting -Enable $true -ScanSchedule $Sch1 -DeploymentEvaluationSchedule $Sch2 -BatchingTimeout 3 -TimeUnit Days -EnforceMandatory $true -Office365ManagementType $false -EnableThirdPartyUpdates $true -EnableDeltaDownload $true -EnableInstallation $true -ThreadPriority Normal -EnableDynamicUpdate $true
```

### Set-CMCloudManagementGateway

For more information, see [Set-CMCloudManagementGateway](/powershell/module/configurationmanager/Set-CMCloudManagementGateway).

**Non-breaking changes**

The following parameters are new:

- CARootCert
- EnableCloudDPFunction
- EnableStorageQuota
- EnableTrafficOut
- EnforceProtocol
- RemoveCertThumbprints
- StorageCriticalPct
- StorageQuotaGB
- StorageWarningPct
- TrafficOutStopService
- VMInstanceCount

**Breaking changes**

The following parameters are removed from this cmdlet:

- VMInstancesCount

### Set-CMDiscoveryMethod

For more information, see [Set-CMDiscoveryMethod](/powershell/module/configurationmanager/Set-CMDiscoveryMethod).

**Bugs that were fixed**

Fixed an issue for parameter **AddGroupDiscoveryScope**.

### Set-CMDistributionPoint

For more information, see [Set-CMDistributionPoint](/powershell/module/configurationmanager/Set-CMDistributionPoint).

**Non-breaking changes**

Added parameters to support Microsoft Connected Cache:

- **EnableDoinc**
- **DiskSpaceUnit**
- **DiskSpaceDoinc**
- **LocalDriveDoinc**
- **RetainDoincCache**
- **AgreeDoincLicense**

**Example:**

```powershell
$dp | Set-CMDistributionPoint -EnableDoinc $true -AgreeDoincLicense $true

$dp | Set-CMDistributionPoint -RetainDoincCache $true -EnableDoinc $true -AgreeDoincLicense $true

$dp | Set-CMDistributionPoint -LocalDriveDoinc "Z:" -DiskSpaceDoinc 9000 -DiskSpaceUnit GB
```

### Set-CMDriverPackage

For more information, see [Set-CMDriverPackage](/powershell/module/configurationmanager/Set-CMDriverPackage).

**Bugs that were fixed**

Fixed an issue for parameter **DriverModel**.

### Set-CMManagementPoint

For more information, see [Set-CMManagementPoint](/powershell/module/configurationmanager/Set-CMManagementPoint).

**Bugs that were fixed**

Fixed an issue for cloud management gateway support.

### Set-CMProgram

For more information, see [Set-CMProgram](/powershell/module/configurationmanager/Set-CMProgram).

**Breaking changes**

Renamed the type `RenameWithUnc` to `RunWithUnc` for parameter **DriveMode**.

### Set-CMSiteMaintenanceTask

For more information, see [Set-CMSiteMaintenanceTask](/powershell/module/configurationmanager/Set-CMSiteMaintenanceTask).

**Non-breaking changes**

Added the following new parameters for configuring **Site backup destination** and **SQL backup destination** for environments with a remote SMS Provider:

- **SiteBackupPath**
- **SqlBackupPath**

**Example:**

```powershell
Set-CMSiteMaintenanceTask -Name $TaskName  -SiteBackupPath "c:\site-backup" -SqlBackupPath "c:\sql-backup" -BeginTime (Get-Date) -DaysOfWeek Sunday,Monday -EnableAlert $true -Enabled $true
```

### Set-CMSoftwareUpdateAutoDeploymentRule

For more information, see [Set-CMSoftwareUpdateAutoDeploymentRule](/powershell/module/configurationmanager/Set-CMSoftwareUpdateAutoDeploymentRule).

**Bugs that were fixed**

Fixed an issue for input object from **Get-CMSoftwareUpdateAutoDeploymentRule** with **Fast** option.

### Set-CMSoftwareUpdateDeploymentPackage

For more information, see [Set-CMSoftwareUpdateDeploymentPackage](/powershell/module/configurationmanager/Set-CMSoftwareUpdateDeploymentPackage).

**Bugs that were fixed**

Fixed an issue for parameters **RemoveExpired** and **RemoveSuperceded**.

### Set-CMSoftwareUpdateGroup

For more information, see [Set-CMSoftwareUpdateGroup](/powershell/module/configurationmanager/Set-CMSoftwareUpdateGroup).

**Bugs that were fixed**

Fixed an issue for adding non-downloaded software update.

### Set-CMStatusFilterRule

For more information, see [Set-CMStatusFilterRule](/powershell/module/configurationmanager/Set-CMStatusFilterRule).

**Bugs that were fixed**

Fixed an issue for **Name** parameter to make sure it consists with **Get-CMStatusFilterRule**.

### Set-CMTaskSequenceDeployment

For more information, see [Set-CMTaskSequenceDeployment](/powershell/module/configurationmanager/Set-CMTaskSequenceDeployment).

**Bugs that were fixed**

Fixed an issue for parameter **ScheduleEvent**.

Fixed an issue for parameter **AllowFallback**.

**Non-breaking changes**

Added validation for parameter **Schedule** to avoid duplicated value with existing assignment.

Added new parameters to configure Schedule:

- **ClearSchedule**
- **RemoveSchedule**
- **AddSchedule**

Added new parameters to configure ScheduleEvent:

- **ClearScheduleEvent**
- **RemoveScheduleEvent**
- **AddScheduleEvent**

**Example:**

```powershell
$ReferenceDeployment | Set-CMTaskSequenceDeployment -AddSchedule $schedule1, $schedule2

$ReferenceDeployment | Set-CMTaskSequenceDeployment -AddScheduleEvent LogOn, LogOff
```

### Set-CMTSStep*

**Bugs that were fixed**

Fixed a policy size issue when you use multiple PowerShell steps that contain large scripts.

### Set-CMTSStepEnableBitLocker

For more information, see [Set-CMTSStepEnableBitLocker](/powershell/module/configurationmanager/Set-CMTSStepEnableBitLocker).

**Bugs that were fixed**

Fixed an issue for user-specified encryption method.

### Set-CMTSStepOfflineEnableBitLocker

For more information, see [Set-CMTSStepOfflineEnableBitLocker](/powershell/module/configurationmanager/Set-CMTSStepOfflineEnableBitLocker).

**Bugs that were fixed**

Fixed an issue for user-specified encryption method.

### Set-CMTSStepPreStartCheck

For more information, see [Set-CMTSStepPreStartCheck](/powershell/module/configurationmanager/Set-CMTSStepPreStartCheck).

**Non-breaking changes**

Added a new parameter for UEFI check:, **CheckUefi**.

### Set-CMWindowsAppxDeploymentType

For more information, see [Set-CMWindowsAppxDeploymentType](/powershell/module/configurationmanager/Set-CMWindowsAppxDeploymentType).

**Non-breaking changes**

Added function to support MSIX.

### Start-CMCloudManagementGateway

For more information, see [Start-CMCloudManagementGateway](/powershell/module/configurationmanager/Start-CMCloudManagementGateway).

**Bugs that were fixed**

Corrected the validation for CMG status.

### Start-CMContentDistribution

For more information, see [Start-CMContentDistribution](/powershell/module/configurationmanager/Start-CMContentDistribution).

**Non-breaking changes**

Added aliases for parameter **DeploymentPackageId** and **DeploymentPackageName** for better understanding.

### Stop-CMCloudManagementGateway

For more information, see [Stop-CMCloudManagementGateway](/powershell/module/configurationmanager/Stop-CMCloudManagementGateway).

**Bugs that were fixed**

Corrected the validation for CMG status.

## How to provide feedback or report issues

Many of the fixes and improvements described in this article are a result of your feedback.

To send feedback, use the Configuration Manager console. For more information, see [Feedback for PowerShell](/mem/configmgr/core/understand/product-feedback#feedback-for-powershell).
