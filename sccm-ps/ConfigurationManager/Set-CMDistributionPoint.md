---
description: Configuring distribution points.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
schema: 2.0.0
title: Set-CMDistributionPoint
---

# Set-CMDistributionPoint

## SYNOPSIS

Configure a distribution point.

## SYNTAX

### SetByValue (Default)
```
Set-CMDistributionPoint [-EnableMaintenanceMode <Boolean>] [-AddBoundaryGroupName <String[]>]
 [-AddMacAddressForRespondingPxeRequest <String[]>] [-AllowFallbackForContent <Boolean>]
 [-AllowPreStaging <Boolean>] [-AllowProxyTraffic <Boolean>] [-AllowPxeResponse <Boolean>]
 [-CertificateExpirationTimeUtc <DateTime>] [-CertificatePassword <SecureString>] [-CertificatePath <String>]
 [-ClearMacAddressForRespondingPxeRequest] [-ClientCommunicationType <ComputerCommunicationType>]
 [-ClientConnectionType <ClientConnectionTypes>] [-ClientTransferRate <NetworkProfile>]
 [-ContentMonitoringPriority <Priority>] [-ContentValidationSchedule <IResultObject>] [-Description <String>]
 [-EnableAnonymous <Boolean>] [-EnableBranchCache <Boolean>] [-EnableContentValidation <Boolean>]
 [-EnableLedbat <Boolean>] [-EnableMulticast <Boolean>] [-EnableNonWdsPxe <Boolean>] [-EnablePullDP <Boolean>]
 [-EnablePxe <Boolean>] [-EnableScheduledMulticast <Boolean>] [-EnableUnknownComputerSupport <Boolean>]
 [-EndIPAddress <String>] [-EndUdpPort <Int32>] [-Force] [-InputObject] <IResultObject> [-KeepWds <Boolean>]
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
Set-CMDistributionPoint [-EnableMaintenanceMode <Boolean>] [-AddBoundaryGroupName <String[]>]
 [-AddMacAddressForRespondingPxeRequest <String[]>] [-AllowFallbackForContent <Boolean>]
 [-AllowPreStaging <Boolean>] [-AllowProxyTraffic <Boolean>] [-AllowPxeResponse <Boolean>]
 [-CertificateExpirationTimeUtc <DateTime>] [-CertificatePassword <SecureString>] [-CertificatePath <String>]
 [-ClearMacAddressForRespondingPxeRequest] [-ClientCommunicationType <ComputerCommunicationType>]
 [-ClientConnectionType <ClientConnectionTypes>] [-ClientTransferRate <NetworkProfile>]
 [-ContentMonitoringPriority <Priority>] [-ContentValidationSchedule <IResultObject>] [-Description <String>]
 [-EnableAnonymous <Boolean>] [-EnableBranchCache <Boolean>] [-EnableContentValidation <Boolean>]
 [-EnableLedbat <Boolean>] [-EnableMulticast <Boolean>] [-EnableNonWdsPxe <Boolean>] [-EnablePullDP <Boolean>]
 [-EnablePxe <Boolean>] [-EnableScheduledMulticast <Boolean>] [-EnableUnknownComputerSupport <Boolean>]
 [-EndIPAddress <String>] [-EndUdpPort <Int32>] [-Force] [-KeepWds <Boolean>]
 [-MacAddressForRespondingPxeRequest <String[]>] [-MinimumSessionSize <Int32>]
 [-MulticastMaximumClientCount <Int32>] [-PassThru] [-PxePassword <SecureString>]
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

The first command gets the distribution point object for the site system server named **MySiteSys_11310.Contoso.com**. It then stores the object in the **$DP** variable. The second command modifies the distribution point object stored in that variable.

```powershell
$DP = Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.Contoso.com"
Set-CMDistributionPoint -InputObject $DP -AllowFallbackForContent $True -AllowPreStaging $True -AllowPxeResponse $False -ClientCommunicationType Http -ClientConnectionType Internet -ContentMonitoringPriority High
```

### Example 2: Reassign a distribution point to a new site

The following example reassigns the **mydp** server from site **ABC** to site **XYZ**.

```PowerShell
Set-CMDistributionPoint -SiteSystemServerName "MyDP.TestDOM.net" -SiteCode "ABC" -ReassignSiteCode "XYZ"
```

### Example 3: Enable Microsoft Connected Cache

The first command gets the distribution point object, and stores it in a variable. It passes that object through the pipeline to enable Connected Cache and configure other related settings.

```powershell
$dp = Get-CMDistributionPoint -SiteSystemServerName "dp01.contoso.com"

$dp | Set-CMDistributionPoint -RetainDoincCache $true -EnableDoinc $true -AgreeDoincLicense $true

$dp | Set-CMDistributionPoint -LocalDriveDoinc "Z:" -DiskSpaceDoinc 9000 -DiskSpaceUnit GB
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

Adds an array of MAC addresses that respond to PXE requests for a PXE-enabled distribution point.

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

When you use the **EnableDoinc** parameter, set this parameter to `$true` to accept the Microsoft Connected Cache server license terms. For more information, see [Microsoft Connected Cache in Configuration Manager](/mem/configmgr/core/plan-design/hierarchy/microsoft-connected-cache#licensing).

If you've already agreed to the licensing terms, you don't have to include this parameter. You see this warning when you unnecessarily include it:<!-- 12502130 -->
`The parameter 'AgreeDoincLicense' has been ignored. Reason: Once the license terms agreement is selected, it will be grayed out and never uncheck it.`

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

Specify a date and time when the self-signed certificate expires.

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

Specify a secure string password for a PKI client certificate specified in **CertificatePath**.

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

Specify the path for a PKI client certificate to import for HTTPS communication. Use the **CertificatePassword** parameter for the certificate's password.

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

Add this parameter to remove the array of MAC addresses that the distribution point uses to respond to PXE requests.

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

Specifies how clients or devices communicate with the distribution point. If you specify `Https`, use the **CertificatePath** and **CertificatePassword** parameters to specify the PKI certificate to use.

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

Specify the client transfer rate.

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

Specify the content monitoring priority.

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

If you use the **EnableContentValidation** parameter, use this parameter to specify the schedule when the distribution point validates content. To create a schedule token object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

Specify an optional description for the distribution point.

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

When you use the **EnableDoinc** parameter, use this parameter to specify the amount of disk space to be used for Microsoft Connected Cache. Use the **DiskSpaceUnit** parameter to determine if this value is disk space in GB or a percentage value.

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

Use this parameter with **DiskSpaceDoinc** to determine if that value is disk space in GB or a percentage value.

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

Indicates that clients that use Windows BranchCache are allowed to download content from this on-premises distribution point.

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

Indicates that content validation is enabled for this distribution point. Use the **ContentValidationSchedule** parameter to specify the schedule.

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

Set this parameter to `$true` to enable this distribution point to be used as a Microsoft Connected Cache server. For more information, see [Microsoft Connected Cache in Configuration Manager](/mem/configmgr/core/plan-design/hierarchy/microsoft-connected-cache).

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

### -EnableMaintenanceMode

Set this parameter to `$true` to enable [maintenance mode](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points#bkmk_maint).

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

Enable multicast for the distribution point.

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

Enable the Configuration Manager PXE responder on the distribution point. When you enable a PXE responder without Windows Deployment Service (WDS), Configuration Manager installs its PXE responder service on the distribution point.

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

When set to `$True`, the distribution point can pull content from other distribution points. Use this parameter with the **SourceDPRank** and **SourceDistributionPoint** parameters.

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

Enable PXE on the distribution point. When you enable PXE, Configuration Manager installs Windows Deployment Services (WDS) on the server, if it's not already installed. WDS is the service that supports PXE boot to install Windows images over the network.

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

Indicates whether you can schedule when Configuration Manager deploys the OS image from the distribution point.

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

Enable support for unknown computers. Unknown computers are devices that Configuration Manager hasn't yet discovered.

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

Use this parameter to add a duplicate certificate without asking for confirmation.

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
### -InitialMPForLookup

This parameter expects a string that represents the different lookup MPs separated by the symbol *. MPs are filtered out based on the Site code of the DP, if the MP' site code is different, an error is thrown.
  - If the DP has Preferred MP already enabled, -InitialMPForLookup accepts the string of MPs.
  - If we're setting the PreferredMPEnabled as disabled, -InitialMPForLookup isn't required to be passed in.

```yaml
Type: String
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a distribution point object to configure. To get this object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

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

Indicates whether the distribution point keeps Windows Deployment Services (WDS) or removes it if you disable PXE.

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

When you use the **EnableDoinc** parameter, use this parameter to select the drive to be used for the Microsoft Connected Cache. If you specify `Automatic`, Configuration Manager selects the drive with the most free space.

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

Specify an array of MAC addresses that the distribution point uses to respond to PXE requests.

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

Specifies how many client requests must be received before a scheduled multicast starts to deploy an OS.

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

Specifies the maximum number of clients that can download the OS from this distribution point.

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

### -PreferredMPEnabled

This parameter is boolean where the $true value for the parameter indicates that the dynamic MP usage is enabled. PXE has to be enabled on the Distribution Point before using this parameter.

```yaml
Type: SwitchParameter
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -PxePassword

Specify the PXE password as a secure string.

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

Specifies how long the distribution point delays before it responds to computer requests when you use multiple PXE-enabled distribution points. By default, the Configuration Manager PXE service point responds first to network PXE requests. This integer value is in seconds.

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

Use this parameter to reassign the distribution point to a new site. Specify the three-letter site code as a string value.

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

Removes an array of boundary groups by name from the distribution point.

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

When you use the **EnableDoinc** parameter, use this parameter to keep the content on the server when you disable the Microsoft Connected Cache.

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

Specifies the number of minutes that Configuration Manager waits before it responds to the first multicast deployment request.

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

Specify the three-character code for the Configuration Manager site that hosts this site system role.

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

Specify the FQDN of the server that hosts this site system role.

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

When you use the **EnablePullDP** parameter, use this parameter to specify an array of distribution point sources. This distribution point pulls content from the specified sources. Use the **SourceDPRank** parameter to prioritize these sources.

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

Specify an array that contains the priorities for the distribution point sources from which this distribution point can pull content. When source distribution points have the same priority, the pull distribution point randomly selects a source. Use this parameter with the **EnablePullDP** and **SourceDistributionPoint** parameters.

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

Specify the name of the user that the distribution point uses to connect to the primary site database. Use the format `domain\username`.

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
