# ConfigurationManager_Cmdlets
## 1610_release_notes

# System Center Configuration Manager Cmdlet Library changes for Current Branch 1610

 >[!NOTE]
 > The 1604 version of the System Center Configuration Manager Cmdlet
 > Library is the baseline for these changes.

##Important changes
###Administrator console allows for launching the Integrated Scripting Environment (ISE)
From the administrator console, an additional option was added to launch the ISE: "Connect via Windows PowerShell ISE".

###Cmdlet update check
The Cmdlet Library will no longer check for updated versions. This check is no longer necessary since the Cmdlet Library now ships simultaneously with Configuration Manager releases.

###Get-CM* cmdlets may support "Fast" mode and may return a warning if it is not used
Some Get cmdlets now have a *Fast* parameter. This parameter allows the cmdlet to return objects without automatically refreshing lazy properties. Retrieving lazy property values can cause additional network traffic and can slow down cmdlet execution. If lazy properties are not used, Fast should be supplied as a cmdlet parameter.

To provide visibility into this change, cmdlets that support *Fast* will write a warning to the console if it is not used in a case where its presence may be beneficial. This warning can be suppressed by setting $CMPSSuppressFastNotUsedCheck = $True.

##How to provide feedback or report issues
Many of the fixes and improvements described in this document are a result of customer feedback. To leave feedback and bug reports, go to http://go.microsoft.com/fwlink/?LinkId=529220 (a Microsoft Account is required).

##Known issues
These are known issues with the Cmdlet Library that are not resolved in this release.

###Cannot import ConfigurationManager.psd1 module by using the logical name
If the path to the ConfigurationManager.psd1 module is added to the PSMODULEPATH environment variable, it cannot be imported by using Import-Module ConfigurationManager.

####Workaround
*  Use the full path to the module
*  https://gallery.technet.microsoft.com/Make-Configuration-Manager-04474a87

    > [!NOTE]
    > This workaround is supplied by the user community and is not tested or supported by Microsoft.

###Add-CMEnrollmentProxyPoint
Cmdlet may not properly configure the enrollment proxy point if there are multiple enrollment points for the primary site, or if the enrollment point is on a separate server.

####Workaround
*  Use the administrator console for this configuration.

###Get-CMAadConditionalAccessPolicy/Set-CMAadConditionalAccessPolicy
64-bit PowerShell environment is required for these cmdlets.

####Workaround
*  None

##New cmdlets
These are newly-added cmdlets for this release that add new functionality or enhance the functionality of existing cmdlets.

###Client settings
New cmdlets have been written to improve the experience around modifying client settings. These cmdlets replace the **Set-CMClientSetting** cmdlet, which is now deprecated. These cmdlets support using the object pipeline from the **Get-CMClientSetting** cmdlet for modifying user-defined client settings.

*  Set-CMClientSettingBackgroundIntelligentTransfer
*  Set-CMClientSettingClientCache
*  Set-CMClientSettingClientPolicy
*  Set-CMClientSettingCloudService
*  Set-CMClientSettingComplianceSetting
*  Set-CMClientSettingComputerAgent
*  Set-CMClientSettingComputerRestart
*  Set-CMClientSettingEndpointProtection
*  Set-CMClientSettingEnrollment
*  Set-CMClientSettingGeneral
*  Set-CMClientSettingHardwareInventory
*  Set-CMClientSettingMeteredInternetConnection
*  Set-CMClientSettingPowerManagement
*  Set-CMClientSettingRemoteTool
*  Set-CMClientSettingSoftwareDeployment
*  Set-CMClientSettingSoftwareInventory
*  Set-CMClientSettingSoftwareMetering
*  Set-CMClientSettingSoftwareUpdate
*  Set-CMClientSettingStateMessaging
*  Set-CMClientSettingUserAndDeviceAffinity

###Conditional access policy
New cmdlets have been written to support Azure Active Directory (Azure AD) conditional access policy settings.
*  Get-CMAadConditionalAccessPolicy
*  Set-CMAadConditionalAccessPolicy

####Example

```
PR1:\> Get-CMAadConditionalAccessPolicy -AccountId 752c1e46-ddd2-4ffc-8f15-23623328c823 -ServicePrincipalType ExchangeOnline -UserCredential (Get-Credential)
```

```
PR1:\> Set-CMAadConditionalAccessPolicy -AccountId 752c1e46-ddd2-4ffc-8f15-23623328c823 -ServicePrincipalType ExchangeOnline -Enabled $true -TargetedDevicePlatforms Windows,WindowsPhone -WindowsDeviceState Compliant -IncludedSecurityGroup All_Users -UserCredential (Get-Credential)
```

###Copy-CMCollection
This cmdlet can be used to clone an existing collection to a new one.

###Endpoint protection
New cmdlets for advanced threat protection policy management:

*  Get-CMAdvancedThreatProtectionPolicy
*  New-CMAdvancedThreatProtectionPolicy
*  Remove-CMAdvancedThreatProtectionPolicy
*  Set-CMAdvancedThreatProtectionPolicy

###Get/Set-CMSiteSummaryTask
These cmdlets can be used to get and set site summary tasks.

###Invoke-CMPromotePreProductionClient
This cmdlet can be used to promote the pre-production client to production status.

####Example

```
PR1:\> Invoke-CMPromotePreProductionClient -Force
```

###Migration
New cmdlets for migration jobs:
*  Get-CMMigrationJob
*  Set-CMMigrationJob

###Rename-CMCategory
This cmdlet can be used to rename a category.

####Example

```
PR1:\> Get-CMCategory -Name MyCategoryName | Rename-CMCategory -NewName MyCategoryNewName -CategoryType AppCategories`
```

##Cmdlet changes
The following changes have been made to existing cmdlets for this release. Changes may be new functionality, bug fixes, or deprecations, and may be breaking. If you use one of the cmdlets or feature areas listed in this section, please carefully review the changes to understand how they may affect your use.

###Miscellaneous changes
####Bugs that were fixed
Deployment type cmdlets that require a *Url* parameter may not validate the parameter value for correctness (for example, **Add-CMGooglePlayDeploymentType**, **Set-CMWindowsPhoneStoreDeploymentType**).

Deployment type cmdlets that support Mobile Application Management (MAM) may not add these details to the application model causing the "App Configuration Policies" tab to be missing from the administrator console.

Add-CM<*technology*>DeploymentType cmdlets do not create deployment types using the same naming convention as the administrator console.

Deployment type cmdlets that require a file instead of a file path (for example, **Add-CMMsiDeploymentType**) will now report a clearer failure cause if an unexpected argument is specified for the *ContentLocation* parameter.

####Non-breaking changes
Provider data representing \__GENERIC WMI objects now display more data to the Windows PowerShell console.

###"Connect via Windows PowerShell ISE" from administrator console
####Bugs that were fixed
The generated script did not run because of an invalid path to the ConfigurationManager module. If an invalid script has already been generated, remove the existing %TEMP%\ISEConnect_sitecode - sitename.ps1 file and relaunch the ISE from the administrator console.

The generated script may be unreadable when an administrator console language pack is installed. If an invalid script has already been generated, remove the existing %TEMP%\ISEConnect_sitecode - sitename.ps1 file and relaunch ISE from the administrator console.

An invalid path error may be raised when launching the ISE from the administrator console.

###Add-CMDeploymentType
####Bugs that were fixed
Cmdlet may return an "Unexpected site version" warning.

###Add-CMDeviceCollectionQueryMembershipRule
####Bugs that were fixed
Cmdlet does not verify the validity of the query specified by the *QueryExpression* parameter.
Cannot create query rules with duplicate names (does not align with administrator console behavior).

###Add-CMDriverToDriverPackage
####Bugs that were fixed
Pipelined object may be disposed by the cmdlet.

###Add-CMEndpointProtectionPoint
####Bugs that were fixed
Adding an endpoint protection point for the first time to a site may result in an incorrect default client settings configuration.

###Add-CMIntuneSubscription
####Bugs that were fixed
*ContactEmail* parameter does not perform validation for correctness.

###Add-CMMsiDeploymentType
####Bugs that were fixed
*EnableBranchCache* parameter value is ignored.

####Non-breaking changes
Added *InstallationBehaviorType* parameter.

###Add-CMScriptDeploymentType
####Bugs that were fixed
*EnableBranchCache* parameter value is ignored.

####Non-breaking changes
Added *InstallationBehaviorType* parameter.

###Add-CMUserCollectionQueryMembershipRule
####Bugs that were fixed
Cmdlet does not verify the validity of the query specified by the *QueryExpression* parameter.

Cannot create query rules with duplicate names (does not align with administrator console behavior).

###Block-CMDevice
####Non-breaking changes
Cmdlet now accepts pipelined object from **Get-CMDevice**.

###Export-CMUserCollection
####Breaking changes
Cmdlet now requires that the *ExportFilePath* argument end in a .mof file extension.

###Get-CMCategory
####Non-breaking changes
Improved validation of *CategoryType* parameter.

###Get-CMClientSetting
####Bugs that were fixed
*SettingType* parameter may be ignored.

###Get-CMDeploymentTypeDependency
####Bugs that were fixed
Unexpected dependencies may be returned by the cmdlet.

###Get-CMDeviceAction
####Bugs that were fixed
Cannot view the new passcode for a PinReset action.

###Get-CMResource
####Bugs that were fixed
Fast parameter is missing.

###Get-CMSiteRole
####Breaking changes
When connected to a primary site and no *SiteCode* parameter is specified, only roles specific to the connected site will be returned. This change was made to have parity and consistency with the administrator console. For instance, if you have a CAS and are running the cmdlet on a primary site, only site roles for the current site code will be used. Site roles for all sites will be returned when running from a CAS.

To restore the previous behavior, the *AllSites* parameter can be used to query all sites within the hierarchy from any connected site.

###Get-CMSoftwareUpdate
####Bugs that were fixed
*UpdateGroup* parameter value may be disposed by the cmdlet.

###Import-CMAntimalwarePolicy
####Bugs that were fixed
Policies exported from earlier versions of Configuration Manager may fail to properly import.

###Import-CMAntimalwarePolicy
####Bugs that were fixed
Policy may fail to import or may be created with validation errors.

Cmdlet allows you to import a file that has already been imported.

###Import-CMComputerInformation
####Breaking changes
*CollectionName* parameter is now mandatory.

####Non-breaking changes
Added support for importing computers by their fully qualified domain name.

###Import-CMDriver
####Breaking changes
If a partial driver import occurs, the cmdlet will no longer fail. It will instead warn that some drivers were not successfully imported. In an event where no drivers can be imported, the cmdlet will still fail.

###Import-CMDriverPackage
####Non-breaking changes
New *ImportActionType* parameter to control the behavior when a package already exists.

###Import-CMPackage
####Non-breaking changes
New *ImportActionType* parameter to control the behavior when a package already exists.

###Import-CMSecurityRole
####Bugs that were fixed
Cmdlet allows invalid *NewRoleName* parameter values to be used.

###Import-CMTaskSequence
####Non-breaking changes
New *ImportActionType* parameter to control the behavior when a package already exists.

###Invoke-CMDeviceAction
####Bugs that were fixed
Cmdlet may fail with an exception if certain discovery information is not available for the targeted device.

###Invoke-CMDeviceRetire
####Bugs that were fixed
Cmdlet silently fails when user does not have permission to invoke the retire operation.

Cmdlet does not fail with a clear error message when attempting to retire an unsupported device.

Cmdlet does not fail with a clear error message when attempting to retire a wiped device.

####Non-breaking changes
New *Cancel* parameter to cancel a pending device retire.

###Invoke-CMDeviceWipe
####Bugs that were fixed
Cmdlet silently fails when user does not have permission to invoke the wipe operation.

Cmdlet does not fail with a clear error message when attempting to wipe an unsupported device.

May not be able to wipe Intune-managed device.

####Non-breaking changes
New *Cancel* parameter to cancel a pending device wipe.

###Invoke-CMSoftwareUpdateAutoDeploymentRule
####Bugs that were fixed
Pipelined object may be disposed by the cmdlet.

###Move-CMObject
####Bugs that were fixed
Cmdlet fails to find an object to move.

###New-CMBootableMedia
####Bugs that were fixed
Cmdlet does not properly validate *CertificateExpireTime* and *CertificateStartTime* parameter values.

###New-CMCaptureMedia
####Breaking changes
Removed unneeded *PrestartCommand* and *PrestartPackage* parameters.

###New-CMCategory
####Bugs that were fixed
Cmdlet allows for creation of unsupported GlobalCondition category type.

####Non-breaking changes
Improved validation of *CategoryType* parameter.

###New-CMClientSetting
####Breaking changes
*SettingType* parameter is now mandatory.

###New-CMComputerAssociation
####Non-breaking changes
Performance improvements.

###New-CMDeviceVariable
####Bugs that were fixed
Cannot create device variables for a primary site member from the CAS.

Pipelined collection object may be disposed by the cmdlet.

###New-CMGlobalCondition
####Bugs that were fixed
*InstanceName* parameter value length is not validated.

####Non-breaking changes
Added the ability to create base64 and xml setting data types.

###New-CMPowerManagementCustomPlan
####Bugs that were fixed
*DisplayOffMinAC* and *DisplayOffMinDC* parameters are not configured in resultant plan.

###New-CMPrestageMedia
####Non-breaking changes
Added *MediaPassword*, *TaskSequence*, and *IncludeApplicationDependency* parameters.

###New-CMQuery
####Bugs that were fixed
Cmdlet does not validate if the query name already exists.

###New-CMTaskSequence
####Bugs that were fixed
Rollback is not configured when *UpgradeOperatingSystem* parameter is used.

Updates and application steps are not placed in the expected positions when *UpgradeOperatingSystem* parameter is used.

###New-CMWindowsEnrollmentProfile
####Bugs that were fixed
Enrollment profile may not contain valid intranet configuration.

###Remove-CMAdministrativeUser
####Breaking changes
Removed the non-functional *RoleName* parameter.

###Remove-CMContentDistribution
####Bugs that were fixed
Pipelined object may be disposed by the cmdlet.

###Remove-CMDeviceVariable
####Bugs that were fixed
Cmdlet will silently fail if trying to remove a variable that does not exist.

Cannot remove device variables for a primary site member from the CAS.

Cmdlet may reject a valid pipelined collection member object.

###Remove-CMIntuneSubscription
####Bugs that were fixed
Cmdlet may fail silently or with an unclear error message if a Microsoft Intune subscription does not exist.

###Remove-CMMaintenanceWindow
####Bugs that were fixed
Cmdlet may ignore the *Name* parameter and remove additional maintenance windows.

####Non-breaking changes
Cmdlet supports *DisableWildcardHandling* parameter hint for *Name* parameter.

###Remove-CMMulticastServicePoint
####Bugs that were fixed
Specifying the parameter *RemoveWDS* with a value of **false** may still cause the WDS feature to be removed.

###Set-CMAppVVirtualEnvironment
####Bugs that were fixed
*AddApplicationGroup* parameter does not verify whether the group has already been added.

###Set-CMBaselineDeployment
####Bugs that were fixed
Cmdlet may silently ignore *OverrideServiceWindow* if enforcement is not enabled for the deployment.

###Set-CMBoundaryGroup
####Bugs that were fixed
*DefaultSiteCode* parameter does not allow null value for clearing the setting.

###Set-CMClientSetting
####Deprecations
Cmdlet has been deprecated and replaced with a feature-specific cmdlet. See [New Cmdlets](#New-Cmdlets) for more details.

###Set-CMCollectionMembershipEvaluationComponent
####Deprecations
*SiteSystemServerName* parameter has been deprecated.

###Set-CMCollectionPowerManagement
####Bugs that were fixed
Cannot change a power management policy from NeverApply to Apply.

###Set-CMConditionalAccessPolicy
####Bugs that were fixed
Cmdlet may fail to modify excluded collections when specifying a policy by using the *Name* or *Id* parameters.

###Set-CMDeploymentType
####Bugs that were fixed
Cmdlet may return an "Unexpected site version" warning.

###Set-CMDeviceVariable
####Bugs that were fixed
Cmdlet will silently fail if trying to set a variable that does not exist.

Cannot configure device variables for a primary site member from the CAS.

Cmdlet may reject a valid pipelined collection member object.

####Non-breaking changes
New *PassThru* parameter to return the resultant device variable.

###Set-CMDistributionPoint
####Bugs that were fixed
Cmdlet may return unexpected warnings about multicast service point configuration.

###Set-CMFileReplicationRoute
####Bugs that were fixed
Cannot set *FileReplicationAccountName* without specifying a replication mode.

###Set-CMGlobalCondition
####Bugs that were fixed
*InstanceName* parameter value length is not validated.

###Set-CMIntuneSubscription
####Bugs that were fixed
*ContactEmail* parameter does not perform validation for correctness.

###Set-CMIntuneSubscriptionAppleMdmProperty
####Bugs that were fixed
Cmdlet may not warn when certain required parameter dependencies are not met.

###Set-CMIntuneSubscriptionPassportForWorkProperty
####Bugs that were fixed
*EnableBiometrics* parameter value may be ignored.

###Set-CMIntuneSubscriptionWindowsPhoneProperty
####Bugs that were fixed
Cmdlet may not fail when certain invalid parameter combinations are used.

###Set-CMMigrationJob
####Bugs that were fixed
Specifying the *UtcTime* parameter without the *MigrationJobSchedule* parameter may result in an invalid migration job configuration.

###Set-CMMigrationSource
####Bugs that were fixed
Cmdlet will silently fail if trying to create a migration source with a name that already exists.

####Non-breaking changes
Cmdlet will attempt to expand the *SourceSiteServerName* parameter value if a fully qualified domain name is not used.

###Set-CMMsiDeploymentType
####Non-breaking changes
Added *InstallationBehaviorType* parameter.

###Set-CMScriptDeploymentType
####Non-breaking changes
Added *InstallationBehaviorType* parameter.

###Set-CMSite
####Bugs that were fixed
Cmdlet may fail if *SiteCode* parameter is used.

####Non-breaking changes
Removed unused extra parameter sets (SetSecurityScopeByName, SetSecurityScopeBySiteCode, and SetSecurityScopeByValue).

###Set-CMSiteMaintenanceTask
####Breaking changes
*SiteCode* parameter has been removed.

####Deprecations
*SummaryTask* parameter has been deprecated. *TaskName* should be used instead.

####Non-breaking changes
Accepts pipelined input from **Get-CMSiteMaintenanceTask**.

Several usability improvements.

Added *TaskName* parameter for setting a task by its name.

###Set-CMSoftwareUpdateDeployment
####Non-breaking changes
Improved the output when using Confirm or WhatIf.

###Set-CMSoftwareUpdatePointComponent
####Bugs that were fixed
Cannot specify "Local Publisher" as a value for the *AddCompany* parameter.

###Set-CMSoftwareUpdateSummarizationSchedule
####Non-breaking changes
Improved the output when using *Confirm* or *WhatIf*.

###Start-CMBaselineDeployment
####Bugs that were fixed
Cmdlet may will silently ignore OverrideServiceWindow if enforcement is not enabled for the deployment.

###Start-CMContentDistribution
###Bugs that were fixed
Pipelined object may be disposed by the cmdlet.

###Start-CMTaskSequenceDeployment
####Bugs that were fixed
Deployment may not be correctly created if the *DeploymentOption* parameter is not specified.

Cmdlet may return a warning that the *PercentSuccess* or *PercentFailure* parameters are ignored when they are not specified.

###Non-breaking changes
If *DeploymentOption* is not specified, a value of DownloadContentLocallyWhenNeededByRunningTaskSequence is implied.

###Unblock-CMDevice
####Non-breaking changes
Cmdlet now accepts pipelined object from **Get-CMDevice**.

###Unlock-CMObject
####Non-breaking changes
Cmdlet will now fail if attempting to unlock an object that is locked by a different SMS Provider session. In previous releases, this would silently fail.

Added *Force* parameter to attempt to unlock objects that may be locked by a different SMS Provider session. This can be used to recover from a scenario where an object was locked by an administrator console that unexpectedly quit without releasing the object lock.
