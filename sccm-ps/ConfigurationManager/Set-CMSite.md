---
description: Changes security scope settings for Configuration Manager sites.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSite
---

# Set-CMSite

## SYNOPSIS
Changes security scope settings for Configuration Manager sites.

## SYNTAX

### SetByObject (Default)
```
Set-CMSite -InputObject <IResultObject> [-Comment <String>] [-EnableWakeOnLan <Boolean>]
 [-WakeOnLanType <WakeOnLanType>] [-WakeOnLanTransmissionMethodType <WakeOnLanTransmissionMethodType>]
 [-RetryNumberOfSendingWakeupPacketTransmission <Int32>] [-SendingWakeupPacketTransmissionDelayMins <Int32>]
 [-MaximumNumberOfSendingWakeupPacketBeforePausing <Int32>] [-SendingWakeupPacketBeforePausingWaitSec <Int32>]
 [-ThreadNumberOfSendingWakeupPacket <Int32>] [-SendingWakeupPacketTransmissionOffsetMins <Int32>]
 [-AddClientRequestServiceType <ClientRequestServiceType>] [-PortForClientRequestServiceType <Int32>]
 [-RemoveClientRequestServiceType <ClientRequestServiceType>] [-UseCustomWebsite <Boolean>]
 [-MaximumConcurrentSendingForAllSite <Int32>] [-MaximumConcurrentSendingForPerSite <Int32>]
 [-RetryNumberForConcurrentSending <Int32>] [-ConcurrentSendingDelayBeforeRetryingMins <Int32>]
 [-AddActiveDirectoryForest <IResultObject[]>] [-RemoveActiveDirectoryForest <IResultObject[]>]
 [-ClientComputerCommunicationType <ClientComputerCommunicationType>] [-UsePkiClientCertificate <Boolean>]
 [-ClientCertificateCustomStoreName <String>]
 [-ClientCertificateSelectionCriteriaType <ClientCertificateSelectionCriteriaType>]
 [-ClientCertificateSelectionCriteriaValue <String>]
 [-TakeActionForMultipleCertificateMatchCriteria <TakeActionForMultipleCertificateMatchCriteria>]
 [-ClientCheckCertificateRevocationListForSiteSystem <Boolean>] [-AddCertificateByPath <String[]>]
 [-RemoveCertificateByKey <String[]>] [-EnableLowFreeSpaceAlert <Boolean>]
 [-FreeSpaceThresholdWarningGB <Int32>] [-FreeSpaceThresholdCriticalGB <Int32>] [-RequireSigning <Boolean>]
 [-RequireSha256 <Boolean>] [-UseEncryption <Boolean>] [-ThresholdOfSelectCollectionByDefault <Int32>]
 [-ThresholdOfSelectCollectionMax <Int32>] [-SiteSystemCollectionBehavior <CollectionBehaviorType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMSite -Name <String> [-Comment <String>] [-EnableWakeOnLan <Boolean>] [-WakeOnLanType <WakeOnLanType>]
 [-WakeOnLanTransmissionMethodType <WakeOnLanTransmissionMethodType>]
 [-RetryNumberOfSendingWakeupPacketTransmission <Int32>] [-SendingWakeupPacketTransmissionDelayMins <Int32>]
 [-MaximumNumberOfSendingWakeupPacketBeforePausing <Int32>] [-SendingWakeupPacketBeforePausingWaitSec <Int32>]
 [-ThreadNumberOfSendingWakeupPacket <Int32>] [-SendingWakeupPacketTransmissionOffsetMins <Int32>]
 [-AddClientRequestServiceType <ClientRequestServiceType>] [-PortForClientRequestServiceType <Int32>]
 [-RemoveClientRequestServiceType <ClientRequestServiceType>] [-UseCustomWebsite <Boolean>]
 [-MaximumConcurrentSendingForAllSite <Int32>] [-MaximumConcurrentSendingForPerSite <Int32>]
 [-RetryNumberForConcurrentSending <Int32>] [-ConcurrentSendingDelayBeforeRetryingMins <Int32>]
 [-AddActiveDirectoryForest <IResultObject[]>] [-RemoveActiveDirectoryForest <IResultObject[]>]
 [-ClientComputerCommunicationType <ClientComputerCommunicationType>] [-UsePkiClientCertificate <Boolean>]
 [-ClientCertificateCustomStoreName <String>]
 [-ClientCertificateSelectionCriteriaType <ClientCertificateSelectionCriteriaType>]
 [-ClientCertificateSelectionCriteriaValue <String>]
 [-TakeActionForMultipleCertificateMatchCriteria <TakeActionForMultipleCertificateMatchCriteria>]
 [-ClientCheckCertificateRevocationListForSiteSystem <Boolean>] [-AddCertificateByPath <String[]>]
 [-RemoveCertificateByKey <String[]>] [-EnableLowFreeSpaceAlert <Boolean>]
 [-FreeSpaceThresholdWarningGB <Int32>] [-FreeSpaceThresholdCriticalGB <Int32>] [-RequireSigning <Boolean>]
 [-RequireSha256 <Boolean>] [-UseEncryption <Boolean>] [-ThresholdOfSelectCollectionByDefault <Int32>]
 [-ThresholdOfSelectCollectionMax <Int32>] [-SiteSystemCollectionBehavior <CollectionBehaviorType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetBySiteCodeMandatory
```
Set-CMSite [-SiteCode <String>] [-Comment <String>] [-EnableWakeOnLan <Boolean>]
 [-WakeOnLanType <WakeOnLanType>] [-WakeOnLanTransmissionMethodType <WakeOnLanTransmissionMethodType>]
 [-RetryNumberOfSendingWakeupPacketTransmission <Int32>] [-SendingWakeupPacketTransmissionDelayMins <Int32>]
 [-MaximumNumberOfSendingWakeupPacketBeforePausing <Int32>] [-SendingWakeupPacketBeforePausingWaitSec <Int32>]
 [-ThreadNumberOfSendingWakeupPacket <Int32>] [-SendingWakeupPacketTransmissionOffsetMins <Int32>]
 [-AddClientRequestServiceType <ClientRequestServiceType>] [-PortForClientRequestServiceType <Int32>]
 [-RemoveClientRequestServiceType <ClientRequestServiceType>] [-UseCustomWebsite <Boolean>]
 [-MaximumConcurrentSendingForAllSite <Int32>] [-MaximumConcurrentSendingForPerSite <Int32>]
 [-RetryNumberForConcurrentSending <Int32>] [-ConcurrentSendingDelayBeforeRetryingMins <Int32>]
 [-AddActiveDirectoryForest <IResultObject[]>] [-RemoveActiveDirectoryForest <IResultObject[]>]
 [-ClientComputerCommunicationType <ClientComputerCommunicationType>] [-UsePkiClientCertificate <Boolean>]
 [-ClientCertificateCustomStoreName <String>]
 [-ClientCertificateSelectionCriteriaType <ClientCertificateSelectionCriteriaType>]
 [-ClientCertificateSelectionCriteriaValue <String>]
 [-TakeActionForMultipleCertificateMatchCriteria <TakeActionForMultipleCertificateMatchCriteria>]
 [-ClientCheckCertificateRevocationListForSiteSystem <Boolean>] [-AddCertificateByPath <String[]>]
 [-RemoveCertificateByKey <String[]>] [-EnableLowFreeSpaceAlert <Boolean>]
 [-FreeSpaceThresholdWarningGB <Int32>] [-FreeSpaceThresholdCriticalGB <Int32>] [-RequireSigning <Boolean>]
 [-RequireSha256 <Boolean>] [-UseEncryption <Boolean>] [-ThresholdOfSelectCollectionByDefault <Int32>]
 [-ThresholdOfSelectCollectionMax <Int32>] [-SiteSystemCollectionBehavior <CollectionBehaviorType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSite** cmdlet changes security scope settings for one or more Microsoft System Center Configuration Manager sites.
A security scope is a collection of permissions that, in conjunction with security roles, defines the configuration actions that an administrator can perform on the site.
You can use this cmdlet to change the type of a security scope action and the name of a security scope for a System Center Configuration Manager site.
You can specify a site for which you change security scope settings by using a site name or a site code, or you can use the [Get-CMSite](Get-CMSite.md) cmdlet to specify a site.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a site to a security scope by using a site name
```
PS XYZ:\> Set-CMSite -SecurityScopeAction AddMembership -SecurityScopeName "Scope22" -SiteName "CMSiteSystem"
```

This command assigns a custom security scope named Scope22 to a System Center Configuration Manager site named CMSiteSystem.

### Example 2: Remove a security scope for a site by using the site name
```
PS XYZ:\> Set-CMSite -SecurityScopeAction RemoveMembership -SecurityScopeName "Scope22" -SiteName "CMSiteSystem"
```

This command removes the custom security scope in the previous example from a System Center Configuration Manager site named CMSiteSystem.

## PARAMETERS

### -AddActiveDirectoryForest
Specifies an array of Active Directory Forest objects to publish in Active Directory Domain Services.
To obtain an Active Directory Forest object, use the [Get-ADForest](/powershell/module/addsadministration/get-adforest?view=win10-ps) cmdlet.

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
Specifies an array of paths to certificates.

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
Specifies a service type to add.
The acceptable values for this parameter are:

- ClientNotificationTcp
- ClientRequestHttpTcp
- ClientRequestHttpTcpDefault
- ClientRequestHttpsTcp
- ClientRequestHttpsTcpDefault
- WakeOnLanUdp

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
Specifies the name of a custom store that contains client certificates.

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
Specifies the criteria type to match in a client certificate, such as a string or attribute for a subject or an alternate name for a subject.

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
Specifies a value for the *ClientCertificateSelectionCriteriaType* parameter.

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
Indicates whether to check the Certificate Revocation List (CRL) for a certificate.

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
Specifies the communication type.
The acceptable values for this parameter are: HttpsOnly and HttpsOrHttp.

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
Specifies a comment for a Configuration Manager site.

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

### -EnableLowFreeSpaceAlert
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
Indicates whether to send Wake On LAN packets for scheduled activities such as deployments of software updates.

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

### -FreeSpaceThresholdCriticalGB
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
Specifies a Configuration Manager site object.
To obtain a Configuration Manager site object, use the [Get-CMSite](Get-CMSite.md) cmdlet.

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
Specifies the maximum number of simultaneous communications to all sites.

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
Specifies the maximum number of simultaneous communications to any single site.

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
Specifies the maximum number of wake up packets transmitted by this site server before pausing.

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
Specifies the name of a Configuration Manager site.

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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
Specifies a port number, such as 80 or 8080, for client requests.

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

### -RemoveActiveDirectoryForest
Specifies an array of Active Directory Forest objects to remove from Active Directory Domain Services.

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
Specifies a service type to remove.
The acceptable values for this parameter are:

- ClientNotificationTcp
- ClientRequestHttpTcp
- ClientRequestHttpTcpDefault
- ClientRequestHttpsTcp
- ClientRequestHttpsTcpDefault
- WakeOnLanUdp

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
Indicates whether to use the SHA-256 algorithm to sign communications.

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
Indicates whether to require Configuration Manager sites to sign communications with other sites.

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

### -RetryNumberForConcurrentSending
Specifies the number of times to retry a failed communication.

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
Specifies the number of times a wake up packet is sent to a target computer.

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
Specifies a site code for a Configuration Manager site to which you assign security scopes.

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
Specifies the action to take for multiple matches of certificate criteria.

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
Specifies the number of threads a site server uses when sending wake up packets.

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
Indicates whether to use a custom web site.
Use a custom web site when you do not want to use the default web site.

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
Indicates whether to use encryption for communication between sites.

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
Indicates whether to use a PKI certificate management solution.

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
Specifies the type of Wake On LAN packet to use.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMSite](Get-CMSite.md)
