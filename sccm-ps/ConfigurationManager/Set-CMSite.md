---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Set-CMSite
---

# Set-CMSite

## SYNOPSIS

Configure a Configuration Manager site.

## SYNTAX

### SetByObject (Default)
```
Set-CMSite [-AddActiveDirectoryForest <IResultObject[]>] [-AddCertificateByPath <String[]>]
 [-AddClientRequestServiceType <ClientRequestServiceType>] [-ClientCertificateCustomStoreName <String>]
 [-ClientCertificateSelectionCriteriaType <ClientCertificateSelectionCriteriaType>]
 [-ClientCertificateSelectionCriteriaValue <String>]
 [-ClientCheckCertificateRevocationListForSiteSystem <Boolean>]
 [-ClientComputerCommunicationType <ClientComputerCommunicationType>] [-Comment <String>]
 [-ConcurrentSendingDelayBeforeRetryingMins <Int32>] [-EnableLowFreeSpaceAlert <Boolean>]
 [-EnableWakeOnLan <Boolean>] [-FreeSpaceThresholdCriticalGB <Int32>] [-FreeSpaceThresholdWarningGB <Int32>]
 -InputObject <IResultObject> [-MaximumConcurrentSendingForAllSite <Int32>]
 [-MaximumConcurrentSendingForPerSite <Int32>] [-MaximumNumberOfSendingWakeupPacketBeforePausing <Int32>]
 [-PassThru] [-PortForClientRequestServiceType <Int32>] [-PromotePassiveSiteToActive]
 [-RemoveActiveDirectoryForest <IResultObject[]>] [-RemoveCertificateByKey <String[]>]
 [-RemoveClientRequestServiceType <ClientRequestServiceType>] [-RequireSha256 <Boolean>]
 [-RequireSigning <Boolean>] [-RetryInstallPassiveSite] [-RetryNumberForConcurrentSending <Int32>]
 [-RetryNumberOfSendingWakeupPacketTransmission <Int32>] [-SendingWakeupPacketBeforePausingWaitSec <Int32>]
 [-SendingWakeupPacketTransmissionDelayMins <Int32>] [-SendingWakeupPacketTransmissionOffsetMins <Int32>]
 [-SiteSystemCollectionBehavior <CollectionBehaviorType>]
 [-TakeActionForMultipleCertificateMatchCriteria <TakeActionForMultipleCertificateMatchCriteria>]
 [-ThreadNumberOfSendingWakeupPacket <Int32>] [-ThresholdOfSelectCollectionByDefault <Int32>]
 [-ThresholdOfSelectCollectionMax <Int32>] [-UseCustomWebsite <Boolean>] [-UseEncryption <Boolean>]
 [-UsePkiClientCertificate <Boolean>] [-UseSmsGeneratedCert <Boolean>]
 [-WakeOnLanTransmissionMethodType <WakeOnLanTransmissionMethodType>] [-WakeOnLanType <WakeOnLanType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMSite [-AddActiveDirectoryForest <IResultObject[]>] [-AddCertificateByPath <String[]>]
 [-AddClientRequestServiceType <ClientRequestServiceType>] [-ClientCertificateCustomStoreName <String>]
 [-ClientCertificateSelectionCriteriaType <ClientCertificateSelectionCriteriaType>]
 [-ClientCertificateSelectionCriteriaValue <String>]
 [-ClientCheckCertificateRevocationListForSiteSystem <Boolean>]
 [-ClientComputerCommunicationType <ClientComputerCommunicationType>] [-Comment <String>]
 [-ConcurrentSendingDelayBeforeRetryingMins <Int32>] [-EnableLowFreeSpaceAlert <Boolean>]
 [-EnableWakeOnLan <Boolean>] [-FreeSpaceThresholdCriticalGB <Int32>] [-FreeSpaceThresholdWarningGB <Int32>]
 [-MaximumConcurrentSendingForAllSite <Int32>] [-MaximumConcurrentSendingForPerSite <Int32>]
 [-MaximumNumberOfSendingWakeupPacketBeforePausing <Int32>] -Name <String> [-PassThru]
 [-PortForClientRequestServiceType <Int32>] [-PromotePassiveSiteToActive]
 [-RemoveActiveDirectoryForest <IResultObject[]>] [-RemoveCertificateByKey <String[]>]
 [-RemoveClientRequestServiceType <ClientRequestServiceType>] [-RequireSha256 <Boolean>]
 [-RequireSigning <Boolean>] [-RetryInstallPassiveSite] [-RetryNumberForConcurrentSending <Int32>]
 [-RetryNumberOfSendingWakeupPacketTransmission <Int32>] [-SendingWakeupPacketBeforePausingWaitSec <Int32>]
 [-SendingWakeupPacketTransmissionDelayMins <Int32>] [-SendingWakeupPacketTransmissionOffsetMins <Int32>]
 [-SiteSystemCollectionBehavior <CollectionBehaviorType>]
 [-TakeActionForMultipleCertificateMatchCriteria <TakeActionForMultipleCertificateMatchCriteria>]
 [-ThreadNumberOfSendingWakeupPacket <Int32>] [-ThresholdOfSelectCollectionByDefault <Int32>]
 [-ThresholdOfSelectCollectionMax <Int32>] [-UseCustomWebsite <Boolean>] [-UseEncryption <Boolean>]
 [-UsePkiClientCertificate <Boolean>] [-UseSmsGeneratedCert <Boolean>]
 [-WakeOnLanTransmissionMethodType <WakeOnLanTransmissionMethodType>] [-WakeOnLanType <WakeOnLanType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetBySiteCodeMandatory
```
Set-CMSite [-AddActiveDirectoryForest <IResultObject[]>] [-AddCertificateByPath <String[]>]
 [-AddClientRequestServiceType <ClientRequestServiceType>] [-ClientCertificateCustomStoreName <String>]
 [-ClientCertificateSelectionCriteriaType <ClientCertificateSelectionCriteriaType>]
 [-ClientCertificateSelectionCriteriaValue <String>]
 [-ClientCheckCertificateRevocationListForSiteSystem <Boolean>]
 [-ClientComputerCommunicationType <ClientComputerCommunicationType>] [-Comment <String>]
 [-ConcurrentSendingDelayBeforeRetryingMins <Int32>] [-EnableLowFreeSpaceAlert <Boolean>]
 [-EnableWakeOnLan <Boolean>] [-FreeSpaceThresholdCriticalGB <Int32>] [-FreeSpaceThresholdWarningGB <Int32>]
 [-MaximumConcurrentSendingForAllSite <Int32>] [-MaximumConcurrentSendingForPerSite <Int32>]
 [-MaximumNumberOfSendingWakeupPacketBeforePausing <Int32>] [-PassThru]
 [-PortForClientRequestServiceType <Int32>] [-PromotePassiveSiteToActive]
 [-RemoveActiveDirectoryForest <IResultObject[]>] [-RemoveCertificateByKey <String[]>]
 [-RemoveClientRequestServiceType <ClientRequestServiceType>] [-RequireSha256 <Boolean>]
 [-RequireSigning <Boolean>] [-RetryInstallPassiveSite] [-RetryNumberForConcurrentSending <Int32>]
 [-RetryNumberOfSendingWakeupPacketTransmission <Int32>] [-SendingWakeupPacketBeforePausingWaitSec <Int32>]
 [-SendingWakeupPacketTransmissionDelayMins <Int32>] [-SendingWakeupPacketTransmissionOffsetMins <Int32>]
 [-SiteCode <String>] [-SiteSystemCollectionBehavior <CollectionBehaviorType>]
 [-TakeActionForMultipleCertificateMatchCriteria <TakeActionForMultipleCertificateMatchCriteria>]
 [-ThreadNumberOfSendingWakeupPacket <Int32>] [-ThresholdOfSelectCollectionByDefault <Int32>]
 [-ThresholdOfSelectCollectionMax <Int32>] [-UseCustomWebsite <Boolean>] [-UseEncryption <Boolean>]
 [-UsePkiClientCertificate <Boolean>] [-UseSmsGeneratedCert <Boolean>]
 [-WakeOnLanTransmissionMethodType <WakeOnLanTransmissionMethodType>] [-WakeOnLanType <WakeOnLanType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use the **Set-CMSite** cmdlet to configure one or more Configuration Manager sites. You can specify a site to configure by using a site name or a site code, or you can use the [Get-CMSite](Get-CMSite.md) cmdlet to specify a site.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a new Active Directory forest

This command adds a new Active Directory forest to which the site is published.

```powershell
$newForest = New-CMActiveDirectoryForest -ForestFqdn "tsqa.contoso.com"

Set-CMSite -SiteCode "XYZ" -AddActiveDirectoryForest $newForest
```

### Example 2: Change the warning alert threshold for free disk space

This command changes the warning threshold for free disk space on the site database server to 15 GB.

```powershell
Set-CMSite -SiteCode "XYZ" -FreeSpaceThresholdWarningGB 15
```

### Example 3: Promote a site server to active mode

This command first uses the **Get-CMSite** cmdlet to get the **ADC** site. It then passes that object through the pipeline to the **Set-CMSite** cmdlet, which promotes the site server in passive mode to be the active site server.<!-- 7648486 -->

```powershell
Get-CMSite -SiteCode "ADC" | Set-CMSite -PromotePassiveSiteToActive
```

### Example 4: Add trusted root certification authorities (CA)

This example adds the certificate in the exported file **cc.cer** to the **XYZ** site as a trusted root CA.

```powershell
Set-CMSite -SiteCode "XYZ" -AddCertificateByPath "D:\Secure\Certs\cc.cer"
```

## PARAMETERS

### -AddActiveDirectoryForest

Specifies an array of Active Directory forest objects to which the site is published. To get an Active Directory forest object, use the [Get-CMActiveDirectoryForest](Get-CMActiveDirectoryForest.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddCertificateByPath

Specifies an array of paths to trusted root certification authorities.

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

### -AddClientRequestServiceType

Specifies a service type to add for a port that Configuration Manager uses to communicate with clients in this site.

```yaml
Type: ClientRequestServiceType
Parameter Sets: (All)
Aliases:
Accepted values: WakeOnLanUdp, ClientNotificationTcp, ClientRequestHttpTcp, ClientRequestsHttpsTcp, ClientRequestHttpTcpDefault, ClientRequestsHttpsTcpDefault

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientCertificateCustomStoreName

Specify the store name where the client certificate is located in the Computer store when you don't use the default store of Personal.

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

### -ClientCertificateSelectionCriteriaType

Specifies the criteria type to match in a client certificate when more than one certificate is available. Use the **-ClientCertificateSelectionCriteriaValue** parameter to specify the value.

```yaml
Type: ClientCertificateSelectionCriteriaType
Parameter Sets: (All)
Aliases:
Accepted values: ClientAuthentication, CertificateSubjectContainsString, CertificateSubjectOrSanIncludesAttributes, CertificateSubjectOrSanIncludesAtrributes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientCertificateSelectionCriteriaValue

Specifies a value for the **-ClientCertificateSelectionCriteriaType** parameter.

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

### -ClientCheckCertificateRevocationListForSiteSystem

Indicates whether clients check the Certificate Revocation List (CRL) for site systems.

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

### -ClientComputerCommunicationType

Specifies the communication method for the site systems that use IIS. To use HTTPS, the servers need a valid PKI web server certificate for server authentication.

```yaml
Type: ClientComputerCommunicationType
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment

Specifies a comment for a Configuration Manager site to help identify it.

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

### -ConcurrentSendingDelayBeforeRetryingMins

A site can send data concurrently to multiple sites. If it needs to retry, this integer value specifies the number of minutes to delay before it retries. By default, the value is `1`. Use the **-RetryNumberForConcurrentSending** parameter to specify the number of retries.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ConcurrentSendingDelayBeforeRetryingMinutes

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

### -EnableLowFreeSpaceAlert

Generate an alert when the free disk space on the site database server is low. Use the **-FreeSpaceThresholdWarningGB** and **-FreeSpaceThresholdCriticalGB** parameters to specify the specific thresholds.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: GenerateAlertWhenFreeDiskSpaceOnSiteDatabaseIsLow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWakeOnLan

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

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

### -FreeSpaceThresholdCriticalGB

When **-EnableLowFreeSpaceAlert** is `$true`, the site raises a _critical_ alert when the free disk space falls below this value. Specify an integer for the free disk space in GB on the site database server.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CriticalAlertWhenFreeDiskSpaceFallBelowFollowingValueGB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FreeSpaceThresholdWarningGB

When **-EnableLowFreeSpaceAlert** is `$true`, the site raises a _warning_ alert when the free disk space falls below this value. Specify an integer for the free disk space in GB on the site database server.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: WarningAlertWhenFreeDiskSpaceFallBelowFollowingValueGB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies a Configuration Manager site object to configure. To get a Configuration Manager site object, use the [Get-CMSite](Get-CMSite.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumConcurrentSendingForAllSite

A site can send data concurrently to multiple sites. This value specifies the maximum number of simultaneous communications to all sites. By default, the value is `5`.

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

### -MaximumConcurrentSendingForPerSite

A site can send data concurrently to multiple sites. This value specifies the maximum number of simultaneous communications to any single site. By default, the value is `3`.

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

### -MaximumNumberOfSendingWakeupPacketBeforePausing

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

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

### -Name

Specifies the name of a Configuration Manager site to configure.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
Aliases: SiteName

Required: True
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

### -PortForClientRequestServiceType

When you use the **-AddClientRequestServiceType** parameter, use this parameter to specify a port number for client requests.

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

### -PromotePassiveSiteToActive

Use this parameter to promote a site server in passive mode to the active site server. For more information, see [Site server high availability in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/site-server-high-availability).

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

### -RemoveActiveDirectoryForest

Specifies an array of Active Directory forest objects. When removed, this site doesn't publish to that forest.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCertificateByKey

Specifies an array of certificates to remove.

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

### -RemoveClientRequestServiceType

Specifies a service type to remove as a port that Configuration Manager uses to communicate with clients in this site.

```yaml
Type: ClientRequestServiceType
Parameter Sets: (All)
Aliases:
Accepted values: WakeOnLanUdp, ClientNotificationTcp, ClientRequestHttpTcp, ClientRequestsHttpsTcp, ClientRequestHttpTcpDefault, ClientRequestsHttpsTcpDefault

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireSha256

When clients sign data and communicate with site systems by using HTTP, this option requires the clients to use SHA-256 to sign the data. Clients must support this hash algorithm. This option applies to clients that don't use PKI certificates.

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

### -RequireSigning

This option requires that clients sign data when they send to management points.

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

### -RetryInstallPassiveSite

Use this parameter to retry the installation for a site server in passive mode that previously failed.

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

### -RetryNumberForConcurrentSending

A site can send data concurrently to multiple sites. If it needs to retry, this integer value specifies the number of times to retry a failed communication. By default, the value is `2`. Use the **-ConcurrentSendingDelayBeforeRetryingMins** parameter to specify the delay in minutes before it retries.

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

### -RetryNumberOfSendingWakeupPacketTransmission

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

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

### -SendingWakeupPacketBeforePausingWaitSec

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SendingWakeupPacketBeforePausingWaitSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendingWakeupPacketTransmissionDelayMins

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SendingWakeupPacketTransmissionDelayMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendingWakeupPacketTransmissionOffsetMins

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SendingWakeupPacketTransmissionOffsetMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode

Specifies the Configuration Manager site code to configure.

```yaml
Type: String
Parameter Sets: SetBySiteCodeMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemCollectionBehavior

For [deployment verification](/mem/configmgr/core/servers/manage/settings-to-manage-high-risk-deployments), specify the behavior to take when the selected collection includes computers that host site systems roles.

- `Block`: Don't create the deployment
- `Warn`: Require verification before creating the deployment

```yaml
Type: CollectionBehaviorType
Parameter Sets: (All)
Aliases: BehaviorWhenCollectionIncludesComputerHostSiteSystemRole
Accepted values: Block, Warn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TakeActionForMultipleCertificateMatchCriteria

Specifies the action to take if multiple certificates match criteria.

```yaml
Type: TakeActionForMultipleCertificateMatchCriteria
Parameter Sets: (All)
Aliases:
Accepted values: FailSelectionAndSendErrorMessage, SelectCertificateWithLongestValidityPeriod

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreadNumberOfSendingWakeupPacket

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

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

### -ThresholdOfSelectCollectionByDefault

For [deployment verification](/mem/configmgr/core/servers/manage/settings-to-manage-high-risk-deployments), configure the default collection size limit. The **Select Collection** window hides collections with membership that exceeds this default value. Specify `0` to disable.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SizeOfCustomCollectionCanSelectByDefault

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThresholdOfSelectCollectionMax

For [deployment verification](/mem/configmgr/core/servers/manage/settings-to-manage-high-risk-deployments), configure the maximum collection size limit. The **Select Collection** window always hides collections that have more members than this maximum size. Specify `0` to disable.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SizeOfCustomCollectionCanSelectMaximum

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseCustomWebsite

Indicates whether to use a custom web site. By default, Configuration Manager site system servers that require IIS to communicate with clients use the default web site.

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

### -UseEncryption

Enable this option to use 3DES to encrypt the client inventory data and state messages that are sent to the management point.

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

### -UsePkiClientCertificate

Indicates whether to use a PKI client certificate for client authentication when available.

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

### -UseSmsGeneratedCert

Use this parameter to enable or disable the site property to **Use Configuration Manager-generated certificates for HTTP site systems**. For more information, see [Enhanced HTTP](/mem/configmgr/core/plan-design/hierarchy/enhanced-http).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UseConfigurationManagerGeneratedCertificateForHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeOnLanTransmissionMethodType

Specifies the type of transmission method to use for Wake On LAN transmissions.

```yaml
Type: WakeOnLanTransmissionMethodType
Parameter Sets: (All)
Aliases:
Accepted values: Unicast, SubnetDirectedBroadcasts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WakeOnLanType

This parameter is for an earlier version of the feature. Instead, use the client settings for wake on LAN with the [Set-CMClientSettingPowerManagement](Set-CMClientSettingPowerManagement.md) cmdlet.

For more information, see [How to configure Wake on LAN in Configuration Manager](/mem/configmgr/core/clients/deploy/configure-wake-on-lan).

```yaml
Type: WakeOnLanType
Parameter Sets: (All)
Aliases:
Accepted values: UseAmtPowerOnCommandsOrWakeupPackets, UseAmtPowerOnCommandsOnly, UseWakeupPacketsOnly

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

## NOTES

## RELATED LINKS

[Get-CMSite](Get-CMSite.md)
