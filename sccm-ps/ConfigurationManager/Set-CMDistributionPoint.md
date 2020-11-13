---
description: Configure a distribution point
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/24/2020
schema: 2.0.0
title: Set-CMDistributionPoint
---

# Set-CMDistributionPoint

## SYNOPSIS

Configure a distribution point.

## SYNTAX

### SetByValue (Default)
```
Set-CMDistributionPoint [-AddBoundaryGroupName <String[]>] [-AddMacAddressForRespondingPxeRequest <String[]>]
 [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>] [-AllowProxyTraffic <Boolean>]
 [-AllowPxeResponse <Boolean>] [-CertificateExpirationTimeUtc <DateTime>] [-CertificatePassword <SecureString>]
 [-CertificatePath <String>] [-ClearMacAddressForRespondingPxeRequest]
 [-ClientCommunicationType <ComputerCommunicationType>] [-ClientConnectionType <ClientConnectionTypes>]
 [-ClientTransferRate <NetworkProfile>] [-ContentMonitoringPriority <Priority>]
 [-ContentValidationSchedule <IResultObject>] [-Description <String>] [-EnableAnonymous <Boolean>]
 [-EnableBranchCache <Boolean>] [-EnableContentValidation <Boolean>] [-EnableLedbat <Boolean>]
 [-EnableMulticast <Boolean>] [-EnableNonWdsPxe <Boolean>] [-EnablePullDP <Boolean>] [-EnablePxe <Boolean>]
 [-EnableScheduledMulticast <Boolean>] [-EnableUnknownComputerSupport <Boolean>] [-EndIPAddress <String>]
 [-EndUdpPort <Int32>] [-Force] [-InputObject] <IResultObject> [-KeepWds <Boolean>]
 [-MacAddressForRespondingPxeRequest <String[]>] [-MinimumSessionSize <Int32>]
 [-MulticastMaximumClientCount <Int32>] [-PassThru] [-PxePassword <SecureString>]
 [-PxeServerResponseDelaySec <Int32>] [-ReassignSiteCode <String>] [-RemoveBoundaryGroupName <String[]>]
 [-RemoveMacAddressForRespondingPxeRequest <String[]>] [-RespondToAllNetwork] [-SessionStartDelayMins <Int32>]
 [-SourceDistributionPoint <String[]>] [-SourceDPRank <Int32[]>] [-StartIPAddress <String>]
 [-StartUdpPort <Int32>] [-UseAnyRangeIP] [-UseComputerAccount] [-UserDeviceAffinity <UserDeviceAffinityType>]
 [-UserName <String>] [-EnableDoinc <Boolean>] [-DiskSpaceUnit <DiskSpaceEnum>] [-DiskSpaceDoinc <Int32>]
 [-LocalDriveDoinc <String>] [-RetainDoincCache <Boolean>] [-AgreeDoincLicense <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMDistributionPoint [-AddBoundaryGroupName <String[]>] [-AddMacAddressForRespondingPxeRequest <String[]>]
 [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>] [-AllowProxyTraffic <Boolean>]
 [-AllowPxeResponse <Boolean>] [-CertificateExpirationTimeUtc <DateTime>] [-CertificatePassword <SecureString>]
 [-CertificatePath <String>] [-ClearMacAddressForRespondingPxeRequest]
 [-ClientCommunicationType <ComputerCommunicationType>] [-ClientConnectionType <ClientConnectionTypes>]
 [-ClientTransferRate <NetworkProfile>] [-ContentMonitoringPriority <Priority>]
 [-ContentValidationSchedule <IResultObject>] [-Description <String>] [-EnableAnonymous <Boolean>]
 [-EnableBranchCache <Boolean>] [-EnableContentValidation <Boolean>] [-EnableLedbat <Boolean>]
 [-EnableMulticast <Boolean>] [-EnableNonWdsPxe <Boolean>] [-EnablePullDP <Boolean>] [-EnablePxe <Boolean>]
 [-EnableScheduledMulticast <Boolean>] [-EnableUnknownComputerSupport <Boolean>] [-EndIPAddress <String>]
 [-EndUdpPort <Int32>] [-Force] [-KeepWds <Boolean>] [-MacAddressForRespondingPxeRequest <String[]>]
 [-MinimumSessionSize <Int32>] [-MulticastMaximumClientCount <Int32>] [-PassThru] [-PxePassword <SecureString>]
 [-PxeServerResponseDelaySec <Int32>] [-ReassignSiteCode <String>] [-RemoveBoundaryGroupName <String[]>]
 [-RemoveMacAddressForRespondingPxeRequest <String[]>] [-RespondToAllNetwork] [-SessionStartDelayMins <Int32>]
 [-SiteCode <String>] [-SiteSystemServerName] <String> [-SourceDistributionPoint <String[]>]
 [-SourceDPRank <Int32[]>] [-StartIPAddress <String>] [-StartUdpPort <Int32>] [-UseAnyRangeIP]
 [-UseComputerAccount] [-UserDeviceAffinity <UserDeviceAffinityType>] [-UserName <String>]
 [-EnableDoinc <Boolean>] [-DiskSpaceUnit <DiskSpaceEnum>] [-DiskSpaceDoinc <Int32>]
 [-LocalDriveDoinc <String>] [-RetainDoincCache <Boolean>] [-AgreeDoincLicense <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDistributionPoint** cmdlet modifies a distribution point on a site system server.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set properties of a distribution point

The first command gets the distribution point object for the site system server named MySiteSys_11310.Contoso.com. It then stores the object in the `$DP` variable. The second command modifies the distribution point object stored in that variable.

```powershell
$DP = Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.Contoso.com"
Set-CMDistributionPoint -InputObject $DP -AllowFallbackForContent $True -AllowPreStaging $True -AllowPxeResponse $False -ClientCommunicationType Http -ClientConnectionType Internet -ContentMonitoringPriority High
```

### Example 2: Set properties of a distribution point by using the pipeline

This command gets the distribution point object for the site system server named MySiteSys_11310.Contoso.com. It then uses the pipeline operator to pass the object to **Set-CMDistributionPoint**, which modifies the distribution point object.

```powershell
Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.Contoso.com" | Set-CMDistributionPoint -AllowFallbackForContent $True -AllowPreStaging $True -AllowPxeResponse $True -ClientCommunicationType Http -ClientConnectionType Internet -ContentMonitoringPriority High
```

### Example 3: Reassign a distribution point to a new site

The following example reassigns the mydp server from site ABC to site XYZ

```PowerShell
Set-CMDistributionPoint -SiteSystemServerName "MyDP.TestDOM.net" -ReassignSiteCode "XYZ" -SiteCode "ABC"
```

## PARAMETERS

### -AddBoundaryGroupName
Adds an array of boundary groups, by name, to a distribution point.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddBoundaryGroupNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddMacAddressForRespondingPxeRequest
Adds an array of media access control (MAC) addresses that respond to Pre-boot eXecution Environment (PXE) requests for a PXE-enabled distribution point.

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

### -AgreeDoincLicense
{{ Fill AgreeDoincLicense Description }}

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

### -AllowFallbackForContent
Indicates whether clients outside of the boundary groups associated with a site system can fall back and use this site system as a source location for content when no other site systems are available.

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

### -AllowPreStaging
Indicates whether the distribution point is enabled for prestaged content.

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

### -AllowProxyTraffic

Enables the site system to use a proxy server when it connects to the internet.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableCloudGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPxeResponse
Indicates whether the distribution point can respond to PXE requests.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: AllowRespondIncomingPxeRequest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpirationTimeUtc
Specifies, in UTC format, the date and time when the certificate expires.

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

### -CertificatePassword
Specifies, as a secure string, the password for a PKI client certificate.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath
Specifies the import path for a PKI client certificate.

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

### -ClearMacAddressForRespondingPxeRequest
Indicates that the cmdlet removes the array of MAC addresses that the distribution point uses to respond to PXE requests.

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

### -ClientCommunicationType

Specifies how clients or devices communicate with the distribution point.

```yaml
Type: ComputerCommunicationType
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientConnectionType

Specifies the client connection type.

```yaml
Type: ClientConnectionTypes
Parameter Sets: (All)
Aliases:
Accepted values: Intranet, Internet, InternetAndIntranet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientTransferRate

Specifies the client transfer rate.

```yaml
Type: NetworkProfile
Parameter Sets: (All)
Aliases:
Accepted values: None, ProfileCustom, Profile10Mbps, Profile100Mbps, Profile1Gbps

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentMonitoringPriority

Specifies the content monitoring priority.

```yaml
Type: Priority
Parameter Sets: (All)
Aliases:
Accepted values: Lowest, Low, Medium, High, Highest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContentValidationSchedule
Specifies a schedule token object that the distribution point uses to validate content on a scheduled basis.
To create a schedule token object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: ValidateContentSchedule

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the distribution point.

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

### -DiskSpaceDoinc
{{ Fill DiskSpaceDoinc Description }}

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

### -DiskSpaceUnit
{{ Fill DiskSpaceUnit Description }}

```yaml
Type: DiskSpaceEnum
Parameter Sets: (All)
Aliases:
Accepted values: GB, Percentage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAnonymous
Indicates that the distribution point permits anonymous connections from Configuration Manager clients to the content library.

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

### -EnableBranchCache
Indicates that clients that use Windows BranchCache are allowed to download content from an on-premises distribution point.
Content downloads from cloud-based distribution points can always be shared by clients that use Windows BranchCache.

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

### -EnableContentValidation
Indicates that content validation is enabled for this distribution point.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableValidateContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDoinc
{{ Fill EnableDoinc Description }}

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

### -EnableLedbat

Enable distribution points to use network congestion control with Windows LEDBAT. This feature can adjust the download speed to use the unused network bandwidth.

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

### -EnableMulticast
Indicates whether multicast is enabled for the distribution point.

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

### -EnableNonWdsPxe
Indicates whether the Configuration Manager PXE responder is enabled on the distribution point. When you enable a PXE responder without Windows Deployment Service (WDS), Configuration Manager installs its PXE responder service on the distribution point.

For more information, see [enable PXE on the distribution point](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points#bkmk_config-pxe).

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

### -EnablePullDP

When set to `$True`, the distribution point is able to pull content from other distribution points.

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

### -EnablePxe
Indicates whether PXE is enabled on the distribution point.

When you enable PXE, Configuration Manager installs Windows Deployment Services (WDS) on the server, if required.
Windows Deployment Services is the service that performs the PXE boot to install operating systems.
After you create the distribution point, Configuration Manager installs a provider in Windows Deployment Services that uses the PXE boot functions.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnablePxeSupport

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableScheduledMulticast
Indicates whether you can schedule when Configuration Manager deploys the operating system image from the distribution point.

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

### -EnableUnknownComputerSupport
Indicates whether support for unknown computers is enabled.
Unknown computers are computers that are not managed by Configuration Manager.

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

### -EndIPAddress
Specifies the ending IP address in a range of multicast addresses that Configuration Manager uses to send data to clients.

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

### -EndUdpPort
Specifies the ending UDP port in a range of multicast UDP ports that Configuration Manager uses to send data to clients.

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

### -Force

Starting in version 1910, use this parameter to add a duplicate certificate without asking for confirmation.

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

### -InputObject
Specifies a distribution point object.
To obtain a distribution point object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: DistributionPoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -KeepWds
Indicates whether the distribution point keeps Windows Deployment Services (WDS) or removes WDS when PXE is disabled.

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

### -LocalDriveDoinc
{{ Fill LocalDriveDoinc Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A:, B:, C:, D:, E:, F:, G:, H:, I:, J:, K:, L:, M:, N:, O:, P:, Q:, R:, S:, T:, U:, V:, W:, X:, Y:, Z:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MacAddressForRespondingPxeRequest
Specifies an array of MAC addresses that the distribution point uses to respond to PXE requests.

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

### -MinimumSessionSize
Specifies how many client requests must be received before a scheduled multicast starts to deploy the operating system.

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

### -MulticastMaximumClientCount
Specifies the maximum number of clients that can download the operating system from this distribution point.

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

### -PxePassword
Specifies, as a secure string, the PXE password.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: ComputersUsePxePassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PxeServerResponseDelaySec
Specifies, in seconds, how long the distribution point delays before it responds to computer requests when you are using multiple PXE-enabled distribution points.
By default, the Configuration Manager PXE service point responds first to network PXE requests.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PxeServerResponseDelaySeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReassignSiteCode
Starting in version 1906, use the following parameter to reassign the distribution point to a new site. Specify the three-letter site code as a string value.

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

### -RemoveBoundaryGroupName
Removes an array of boundary groups, by name, from the distribution point.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveBoundaryGroupNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveMacAddressForRespondingPxeRequest
Removes an array of MAC addresses that the distribution point uses to respond to PXE requests.

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

### -RespondToAllNetwork
Indicates that the distribution point responds to PXE requests that arrive on any of its network interfaces.

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

### -RetainDoincCache
{{ Fill RetainDoincCache Description }}

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

### -SessionStartDelayMins
Specifies the number of minutes that Configuration Manager waits before it responds to the first deployment request.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SessionStartDelayMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for the Configuration Manager site that hosts this site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server that hosts a site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDistributionPoint
Specifies an array of distribution point sources from which this distribution point can pull content.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SourceDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDPRank
Specifies an array that contains the priorities for the distribution point sources from which this distribution point can pull content.
Source distribution points that have the same priority are randomly selected.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: SourceDPRanks

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartIPAddress
Specifies the starting IP address in a range of multicast addresses that Configuration Manager uses to send data to clients.

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

### -StartUdpPort
Specifies the starting UDP port in a range of multicast UDP ports that Configuration Manager uses to send data to clients.

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

### -UseAnyRangeIP

Indicates that multicast uses IP addresses within any range.

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

### -UseComputerAccount

Indicates that the distribution point uses its computer account as the multicast connection account when it connects to the primary site database.

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

### -UserDeviceAffinity

Specifies how you want the distribution point to associate users with their devices for PXE deployments.

```yaml
Type: UserDeviceAffinityType
Parameter Sets: (All)
Aliases:
Accepted values: DoNotUse, AllowWithManualApproval, AllowWithAutomaticApproval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName

Specifies the name of the user that the distribution point uses to connect to the primary site database.
Use the format domain\username.

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

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Add-CMDistributionPoint](Add-CMDistributionPoint.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[New-CMSchedule](New-CMSchedule.md)

[Remove-CMDistributionPoint](Remove-CMDistributionPoint.md)

[Update-CMDistributionPoint](Update-CMDistributionPoint.md)

[Install and configure distribution points in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points)
