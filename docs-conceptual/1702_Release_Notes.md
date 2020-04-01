---
title: Version 1702 release notes
titleSuffix: Configuration Manager
description: Release notes for the changes to PowerShell cmdlets in Configuration Manager version 1702. 
ms.date: 03/27/2017
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# System Center Configuration Manager Cmdlet Library changes for Current Branch 1702

 >[!NOTE]
 > System Center Configuration Current Branch 1610 is the baseline for these changes. See [System Center Configuration Manager Cmdlet Library changes for Current Branch 1610](https://docs.microsoft.com/powershell/sccm/configurationmanager/1610_release_notes) for more details.

## Important changes
### Documentation library updates
For the latest cmdlet library documentation, see [ConfigurationManager module reference](https://docs.microsoft.com/powershell/module/configurationmanager/?view=sccm-ps).

### Removed cmdlets
The following cmdlets are no longer supported and have been removed:

-   Add-CMNokiaDeploymentType

-   Add-CMOutOfBandServicePoint

-   Add-CMSystemHealthValidatorPoint

-   Clear-CMAmtAuditLog

-   Disable-CMAmtAuditLog

-   Enable-CMAmtAuditLog

-   Enable-CMAutomaticAmtProvisioning

-   Get-CMAutomaticAmtProvisioningStatus

-   Get-CMCmdletUpdateCheck

-   Get-CMOutOfBandManagementComponent

-   Get-CMOutOfBandServicePoint

-   Get-CMSystemHealthValidatorPoint

-   Get-CMSystemHealthValidatorPointComponent

-   New-CMWiredProfileObject

-   New-CMWirelessProfileObject

-   Remove-CMAmtProvisioningData

-   Remove-CMNokiaDeploymentType

-   Remove-CMOutOfBandServicePoint

-   Remove-CMSystemHealthValidatorPoint

-   Send-CMCmdletUpdateCheck

-   Set-CMCmdletUpdateCheck

-   Set-CMNokiaDeploymentType

-   Set-CMOutOfBandManagementComponent

-   Set-CMOutOfBandServicePoint

-   Set-CMSystemHealthValidatorPointComponent

-   Update-CMAmtProvisioning

### Support for importing the ConfigurationManager module by using the logical name
There is now support for importing the ConfigurationManager module by using a logical name or path.

If the C:\\Program Files (x86)\\Microsoft Configuration Manager\\AdminConsole\\bin or equivalent path is added to the
[PSModulePath](https://docs.microsoft.com/powershell/scripting/developer/module/modifying-the-psmodulepath-installation-path?view=powershell-7) variable, the following can be used:

`Import-Module ConfigrationManager`

Otherwise, the following can be used:

`Import-Module 'C:\Program Files (x86)\Microsoft Configuration Manager\AdminConsole\bin\ConfigurationManager'`

## How to provide feedback or report issues
Many of the fixes and improvements described in this document are a result of customer feedback. To leave feedback and bug reports, use [UserVoice](https://configurationmanager.uservoice.com).

## Known issues
These are known issues with the Cmdlet Library that are not resolved in this release.

### Get-CMAadConditionalAccessPolicy and Set-CMAadConditionalAccessPolicy
64-bit PowerShell environment is required for these cmdlets.

#### Workaround

-   None

## New cmdlets
These are newly-added cmdlets for this release that add new functionality or enhance the functionality of existing cmdlets.

### iOS enrollment profile
New cmdlets have been added for configuring iOS enrollment profiles.

-   Get-CMIosEnrollmentProfile

-   New-CMIosEnrollmentProfile

-   Remove-CMIosEnrollmentPRofile

-   Set-CMIosEnrollmentProfile

### Cloud management gateway cmdlets
New cmdlets have been added for configuring cloud management gateway site roles.

-   Add-CMCloudManagementGatewayConnectionPoint

-   Get-CMCloudManagementGateway

-   Get-CMCloudManagementGatewayConnectionPoint

-   New-CMCloudManagementGateway

-   Remove-CMCloudManagementGateway

-   Remove-CMCloudManagementGatewayConnectionPoint

-   Set-CMCloudManagementGateway

-   Set-CMCloudManagementGatewayConnectionPoint

-   Start-CMCloudManagementGateway

-   Stop-CMCloudManagementGateway

### Data Warehouse Service point cmdlets
New cmdlets have been added for configuring Data Warehouse Service point site roles.

-   Add-CMDataWarehouseServicePoint

-   Get-CMDataWarehouseServicePoint

-   Remove-CMDataWarehouseServicePoint

-   Set-CMDataWarehouseServicePoint

### Deployment cmdlets
Several new cmdlets have been written and improvements made around deployment and deployment monitoring scenarios.

#### Content distribution status
**Get-CMDistributionStatus** is a new cmdlet that can be used to get the distribution status of any content object such as applications, settings, or program packages.

#### Get deployments
Cmdlets have been created to get the object associated with an actual deployment.

-   Get-CMApplicationDeployment

-   Get-CMBaselineDeployment

-   Get-CMConfigurationPolicyDeployment

-   Get-CMPackageDeployment

-   Get-CMSoftwareUpdateDeployment

-   Get-CMTaskSequenceDeployment

#### Deployment creation
Cmdlets have been created for creating new deployments. These cmdlets supersede pre-existing Start-CM\*Deployment cmdlets.

-   New-CMApplicationDeployment

-   New-CMBaselineDeployment

-   New-CMConfigurationPolicyDeployment

-   New-CMPackageDeployment

-   New-CMSoftwareUpdateDeployment

-   New-TaskSequenceDeployment

#### Improved object pipeline support
Set-CM\*Deployment, Remove-CM\*Deployment, and Get-CM\*DeploymentStatus now fully support the object pipeline.

#### Start-CM\<feature\>Deployment cmdlets have been deprecated
The following Start-CM\<feature\>Deployment cmdlets have been deprecated. The replacement cmdlets may differ in parameter names but should have identical, and in some cases improved, functionality.

-   Start-CMApplicationDeployment (replaced by New-CMApplicationDeployment)

-   Start-CMPackageDeployment (replaced by New-CMPackageDeployment)

-   Start-CMBaselineDeployment (replaced by New-CMBaselineDeployment)

-   Start-CMConfigurationPolicyDeployment (replaced by New-CMConfigurationPolicyDeployment)

-   Start-CMTaskSequenceDeployment (replaced by New-CMTaskSequenceDeployment)

-   Start-CMSoftwareUpdateDeployment (replaced by New-CMSoftwareUpdateDeployment)

### Get-CMResultantSettings
This cmdlet will retrieve the resultant client settings for a collection, device, or user.

### Operating system upgrade package updates
New cmdlets have been added for creating and modifying operating system upgrade package update schedules.

-   Clear-CMOperatingSystemUpgradeUpdateSchedule

-   Get-CMOperatingSystemUpgradeUpdateSchedule

-   New-CMOperatingSystemUpgradeUpdateSchedule

-   Remove-CMOperatingSystemUpgradeUpdateSchedule

### Remove-CMSoftwareUpdateFromGroup
This cmdlet will remove a software update from a software update group.

## Cmdlet changes
The following changes have been made to existing cmdlets for this release. Changes may be new functionality, bug fixes, or deprecations, and may be breaking. If you use one of the cmdlets or feature areas listed in this section, please carefully review the changes to understand how they may affect your use.

### Miscellaneous changes
#### Bugs that were fixed
Large SMS\_EmbeddedPropertyList objects used by certain provider classes may not be properly consumed by the cmdlet framework, leading to undefined behavior when getting or setting these values.

Certain combinations of changes to antimalware policies or client settings can cause an invalid policy to be generated. When in this state, the SMS Provider will return an "Instance is not a valid client agent config" error.

Cmdlets for configuring management points and software update points have added the *EnableCloudGateway* parameter to enable these roles for use with the cloud management gateway.

### Site maintenance window configuration
#### Non-breaking changes
CMMaintenanceWindow cmdlets now support configuring maintenance windows for sites. The output of **Get-CMSite** can be pipelined into **New**, **Remove**, or **Set-CMMaintenanceWindow** to configure the maintenance windows for a site.

### Add-CMDeploymentType
#### Breaking changes
Support for creating Nokia deployment types has been removed.

### Add-CMDeviceAfinityToUser
#### Bugs that were fixed
Cmdlet may fail unexpectedly with an **ObjectNotFound** error.

### Add-CMDistributionPoint
#### Bugs that were fixed
Cmdlet allows you to configure a distribution point as Internet-capable when HTTPS is not enabled.

#### Non-breaking changes
Added *AllowProxyTraffic* parameter.

Previously unused *InstallInternetServer* parameter now changes distribution point configuration.

#### Deprecations
*UseComputerAccount* parameter has been deprecated. To use a computer account, set *UserName* to $null.

### Add-CMEnrollmentPoint
#### Bugs that were fixed
Enrollment point role missing configuration settings in created object.

### Add-CMEnrollmentProxyPoint
#### Non-breaking changes
Added *ServiceHost* parameter to allow specifying a remote enrollment point.

### Add-CMIntuneSubscription
#### Bugs that were fixed
*ContactEmail* parameter cannot be set to null or empty value.

### Add-CMMulticastServicePoint
#### Bugs that were fixed
*UserName* does not validate for correct DOMAIN\\user formatting.

*StartUdpPort* and *EndUdpPort* parameters do not validate values for certain incorrect configurations.

*StartIPAddress* and *EndIPAddress* parameters do not validate values for certain incorrect configurations.

#### Non-breaking changes
*UseAnyRangeIP* parameter added.

#### Deprecations
*ClientTransferRate* parameter is no longer supported.

### Approve-CMUserDeviceAffinityRequest
#### Bugs that were fixed
Cmdlet allows approving a previously processed affinity request.

### Convert-CMSchedule
#### Bugs that were fixed
*InputObject* parameter does not accept pipelined schedule object.

### Deny-CMUserDeviceAffinityRequest
#### Bugs that were fixed
Cmdlet allows denying a previously processed affinity request.

### Get-CMAlert
#### Bugs that were fixed
Cannot retrieve client health or endpoint protection alerts.

### Get-CMSiteStatusMessage
#### Non-breaking changes
*ComputerName*, *Severity*, and *SiteCode* parameters now accept array values.

Added *MessageId*, *Module*, *Component*, and *FilterHashTable* parameters for further filtering.

All string-based filter parameters now accept wildcards.

### Get-CMWindowsEnrollmentProfilePackage
#### Bugs that were fixed
Cannot specify cmdlet without parameters.

### Import-CMComputerInformation
#### Breaking changes
Cmdlet will fail if importing a record that already exists and the new *MergeIfExist* parameter is not specified.

### Import-CMDriver
### Bugs that were fixed
When *ImportFolder* is used, driver packages may use more space than expected.

### Install-CMClient
#### Non-breaking changes
Added support for pipelined objects from **Get-CMDevice** and **Get-CMResource**.

### Invoke-CMRemoteControl
#### Bugs that were fixed
Cmdlet does not accept a pipelined object from **Get-CMSiteSystemServer**.

Cannot target a site system server for remote control if it is not also a client machine.

### New-CMActiveDirectoryForest
#### Non-breaking changes
Added *UserName* parameter to allow for configuring the discovery account.

Added *AddPublishingSite* parameter.

### New-CMApplicationDeployment
#### Non-breaking changes
Added *UpdateSupersedence* parameter.

### New-CMBoundaryGroup
#### Breaking changes
FastLink is the only supported value for the hash table in the *AddSiteSystemServer* parameter. Support for all other values has been removed.

### New-CMCertificateProfilePfx
#### Bugs that were fixed
*KeyStorageProvider* parameter value may not apply as expected to the newly created certificate profile.

### New-CMGlobalCondition
#### Breaking changes
Support for creating Nokia global conditions has been removed.

### New-CMProgram
#### Non-breaking changes
Added *AddSupportedOperatingSystemPlatform* parameter.

### New-CMSoftwareUpdateAutoDeploymentRule
#### Bugs that were fixed
*MicrosoftAsVendor* parameter value may not be applied to rule.

#### Non-breaking changes
Added *Vendor* parameter to support third-party patches.

Added *GenerateFailureAlert* parameter.

### New-CMSoftwareUpdateDeployment
#### Non-breaking changes
Added *RequirePostRebootFullScan* parameter.

### New-CMStandaloneMedia
#### Non-breaking changes

Added *MediaStartDate* and *MediaExpirationDate* parameters to support media expiration.

Added *Application*, *DriverPackage*, and *Package* parameters for adding additional media content.

### New-CMStatusMessageQuery
#### Bugs that were fixed
Created query may not appear in the expected administrator console location.

### New-CMWindowsEnrollmentProfile
#### Bugs that were fixed
*EnrollmentProxyPoint* parameter can be set to a null or empty value.

*SiteCode* parameter value may cause validation error to occur in administrator console.

### Remove-CMResource
#### Bugs that were fixed
Removal of a resource does not remove state migration associations.

### Remove-CMWindowsEnrollmentProfilePackage
#### Bugs that were fixed
**AmbiguousParameterSet** error may be raised when running the cmdlet.

### Set-CMActiveDirectoryForest
#### Non-breaking changes
Added *UserName* parameter to allow for configuring the discovery account.

Added *AddPublishingSite* and *RemovePublishingSite* parameters.

### Set-CMAdvancedThreatProtectionPolicy
#### Bugs that were fixed
Increasing or decreasing priority may cause an **ObjectNotFound** error to be returned.

### Set-CMAntimalwarePolicy
#### Bugs that were fixed
*WhatIf* may not display the expected policy name.

Real-time protection settings cannot be changed when using a pipelined object.

#### Non-breaking changes
Cmdlet now accepts pipelined input from **Get-CMAntimalwarePolicy**.

### Set-CMApplication
#### Non-breaking changes
Added *AddSupportContact*, *AddOwner*, *RemoveSupportContact*, *RemoveOwner*, *ClearSupportContact*, and *ClearOwner* parameters to support in-place modifications of support contacts or owners.

### Set-CMAppVVirtualEnvironment
#### Bugs that were fixed
*PassThru* does not return the most up-to-date object.

### Set-CMBaseline
#### Bugs that were fixed
*PassThru* does not return an SMS\_ConfigurationItem object.

#### Non-breaking changes
Added *ClearRequiredConfigurationItem*, *ClearProhibitedConfigurationItem*, *ClearOptionalConfigurationItem*, *ClearOSConfigurationItem*, *ClearSoftwareUpdate*, *ClearBaseline*, *RemoveRequiredConfigurationItem*, *RemoveOptionalConfigurationItem*, *RemoveProhibitedConfigurationItem* *RemoveOSConfigurationItem*, *RemoveSoftwareUpdate*, *RemoveBaseline*, *AddSoftwareUpdate*, and *AddBaseline* parameters.

### Set-CMBoundaryGroup
#### Breaking changes
FastLink is the only supported value for the hash table in the *AddSiteSystemServer* parameter. Support for all other values has been removed.

### Set-CMCertificateProfileTrustedRootCA
#### Bugs that were fixed
Using object pipeline may cause a **ParameterBindingException** error.

### Set-CMClientPushInstallation
#### Non-breaking changes
Added *AddAccount* and *RemoveAccount* parameters to support in-place modifications of client push accounts.

### Set-CMClientSettingComputerAgent
#### Bugs that were fixed
*HealthAttestationUrl* parameter value is not required if *EnableHealthAttestation* or *UseOnPremisesHealthAttestation* are set to true.

### Set-CMComputerAssociation
#### Non-breaking changes
Added *MigrationId* parameter.

### Set-CMDeploymentType
#### Breaking changes
Support for modifying Nokia deployment types has been removed.

### Set-CMDiscoveryMethod
#### Bugs that were fixed
*PollingSchedule* value may not apply correctly to the discovery method.

### Set-CMDistributionPoint
#### Bugs that were fixed
Cmdlet allows you to configure a distribution point as Internet-capable when HTTPS is not enabled.

#### Non-breaking changes
Added *AllowProxyTraffic* parameter.

Previously unused *InstallInternetServer* parameter now changes distribution point configuration.

#### Deprecations
*UseComputerAccount* parameter has been deprecated. To use a computer account, set *UserName* to $null.

### Set-CMEmailNotificationComponent
#### Non-breaking changes
Added *UseSsl* parameter.

### Set-CMFileReplicationRoute
#### Bugs that were fixed
*FileReplicationAccountName* parameter cannot be set to null or empty value.

### Set-CMHierarchySetting
#### Non-breaking changes
Added *ExclusionCollection*, *ExclusionCollectionId*, *ExclusionCollectionName*, and *EnableExclusionCollection* parameters for configuring client upgrade exclusions.

### Set-CMIntuneSubscription
#### Bugs that were fixed
*ContactEmail* parameter cannot be set to null or empty value.

#### Non-breaking changes
*MaximumUserDevice* parameter now supports a value between 1 and 15.

### Set-CMIntuneSubscriptionWindowsPhoneProperty
#### Bugs that were fixed
Cmdlet may unexpectedly fail with an **AetCleanupFailure** error.

### Set-CMMaintenanceTask
#### Bugs that were fixed
*PassThru* parameter does not cause an object to be returned.

### Set-CMMulticastServicePoint
#### Bugs that were fixed
*UserName* parameter does not validate value for correct DOMAIN\\user formatting.

*StartUdpPort* and *EndUdpPort* parameters do not validate values for certain incorrect configurations.

*StartIPAddress* and *EndIPAddress* parameters do not validate values for certain incorrect configurations.

#### Non-breaking changes
*UseAnyRangeIP* parameter added.

#### Deprecations
*ClientTransferRate* parameter is no longer supported.

### Set-CMProgram
#### Non-breaking changes
Added *AddSupportedOperatingSystemPlatform*, *RemoveSupportedOperatingSystemPlatform*, and *RunOnAnyPlatform* parameters.

### Set-CMSite
#### Bugs that were fixed
*RemoveClientRequestServiceType* may not properly remove the specified value.

#### Non-breaking changes
Added *SiteSystemCollectionBehavior*, *ThresholdOfSelectCollectionMax*, *ThresholdOfSelectCollectionByDefault*, and *ThresholdOfSelectCollectionMax* parameters to configure device collection thresholds for a site.

### Set-CMSiteSummaryTask
#### Bugs that were fixed
*PassThru* parameter does not cause an object to be returned.

### Set-CMSoftwareUpdateAutoDeploymentRule
#### Bugs that were fixed
*MicrosoftAsVendor* parameter value may not be applied to rule.

#### Non-breaking changes
Added *Vendor* parameter to support third-party patches.

Added *GenerateFailureAlert* parameter.

### Set-CMSoftwareUpdateDeployment
#### Non-breaking changes
Added *RequirePostRebootFullScan* parameter.

### Set-CMSoftwareUpdatePointComponent
#### Bugs that were fixed
*EnableSynchronization* and *Schedule* parameter usage may cause improper warning to be generated, or schedule to not be modified as expected.

### Set-CMStatusFilterRule
#### Bugs that were fixed
Changes to *Priority* parameter value may not apply to the status filter rule.

### Set-CMTaskSequence
#### Deprecations
*UseDefaultText* parameter has been deprecated. To use the default text, set *CustomText* to $null.

### Set-CMWindowsEnrollmentProfile
#### Bugs that were fixed
*Authority* parameter is not available in all parameter sets.
