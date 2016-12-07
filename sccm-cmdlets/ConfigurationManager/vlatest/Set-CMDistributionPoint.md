---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833813
schema: 2.0.0
ms.assetid: 568313DB-699D-43DC-AA93-316B5D1142AC
---

# Set-CMDistributionPoint

## SYNOPSIS
Sets a distribution point.

## SYNTAX

### SetByValue (Default)
```
Set-CMDistributionPoint [-InputObject] <IResultObject> [-Description <String>]
 [-ClientCommunicationType <ComputerCommunicationType>] [-ClientConnectionType <ClientConnectionTypes>]
 [-EnableAnonymous <Boolean>] [-CertificateExpirationTimeUtc <DateTime>] [-CertificatePath <String>]
 [-CertificatePassword <SecureString>] [-AllowPreStaging <Boolean>] [-EnablePxe <Boolean>] [-KeepWds <Boolean>]
 [-AllowPxeResponse <Boolean>] [-EnableUnknownComputerSupport <Boolean>] [-PxePassword <SecureString>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-RespondToAllNetwork]
 [-MacAddressForRespondingPxeRequest <String[]>] [-AddMacAddressForRespondingPxeRequest <String[]>]
 [-RemoveMacAddressForRespondingPxeRequest <String[]>] [-ClearMacAddressForRespondingPxeRequest]
 [-PxeServerResponseDelaySec <Int32>] [-EnableMulticast <Boolean>] [-UseComputerAccount] [-UserName <String>]
 [-UseAnyRangeIP] [-StartIPAddress <String>] [-EndIPAddress <String>] [-StartUdpPort <Int32>]
 [-EndUdpPort <Int32>] [-ClientTransferRate <NetworkProfile>] [-MulticastMaximumClientCount <Int32>]
 [-EnableScheduledMulticast <Boolean>] [-SessionStartDelayMins <Int32>] [-MinimumSessionSize <Int32>]
 [-EnableContentValidation <Boolean>] [-ContentValidationSchedule <IResultObject>]
 [-ContentMonitoringPriority <Priority>] [-EnablePullDP <Boolean>] [-SourceDistributionPoint <String[]>]
 [-SourceDPRank <Int32[]>] [-AllowFallbackForContent <Boolean>] [-AddBoundaryGroupName <String[]>]
 [-RemoveBoundaryGroupName <String[]>] [-EnableBranchCache <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMDistributionPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-Description <String>]
 [-ClientCommunicationType <ComputerCommunicationType>] [-ClientConnectionType <ClientConnectionTypes>]
 [-EnableAnonymous <Boolean>] [-CertificateExpirationTimeUtc <DateTime>] [-CertificatePath <String>]
 [-CertificatePassword <SecureString>] [-AllowPreStaging <Boolean>] [-EnablePxe <Boolean>] [-KeepWds <Boolean>]
 [-AllowPxeResponse <Boolean>] [-EnableUnknownComputerSupport <Boolean>] [-PxePassword <SecureString>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-RespondToAllNetwork]
 [-MacAddressForRespondingPxeRequest <String[]>] [-AddMacAddressForRespondingPxeRequest <String[]>]
 [-RemoveMacAddressForRespondingPxeRequest <String[]>] [-ClearMacAddressForRespondingPxeRequest]
 [-PxeServerResponseDelaySec <Int32>] [-EnableMulticast <Boolean>] [-UseComputerAccount] [-UserName <String>]
 [-UseAnyRangeIP] [-StartIPAddress <String>] [-EndIPAddress <String>] [-StartUdpPort <Int32>]
 [-EndUdpPort <Int32>] [-ClientTransferRate <NetworkProfile>] [-MulticastMaximumClientCount <Int32>]
 [-EnableScheduledMulticast <Boolean>] [-SessionStartDelayMins <Int32>] [-MinimumSessionSize <Int32>]
 [-EnableContentValidation <Boolean>] [-ContentValidationSchedule <IResultObject>]
 [-ContentMonitoringPriority <Priority>] [-EnablePullDP <Boolean>] [-SourceDistributionPoint <String[]>]
 [-SourceDPRank <Int32[]>] [-AllowFallbackForContent <Boolean>] [-AddBoundaryGroupName <String[]>]
 [-RemoveBoundaryGroupName <String[]>] [-EnableBranchCache <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDistributionPoint** cmdlet modifies a distribution point on a site system server.

## EXAMPLES

### Example 1: Set properties of a distribution point
```
PS C:\>$DP = Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.Contoso.com"
PS C:\> Set-CMDistributionPoint -InputObject $DP -AllowFallbackForContent $True -AllowPreStaging $True -AllowPxeResponse $False -ClientCommunicationType Http -ClientConnectionType Internet -ContentMonitoringPriority High
```

The first command gets the distribution point object for the site system server named MySiteSys_11310.Contoso.com and stores the object in the $DP variable.

The second command modifies the distribution point object stored in $DP.

### Example 2: Set properties of a distribution point by using the pipeline
```
PS C:\>Get-CMDistributionPoint -SiteSystemServerName "MySiteSys_11310.Contoso.com" | Set-CMDistributionPoint -AllowFallbackForContent $True -AllowPreStaging $True -AllowPxeResponse $True -ClientCommunicationType Http -ClientConnectionType Internet -ContentMonitoringPriority High
```

This command gets the distribution point object for the site system server named MySiteSys_11310.Contoso.com and uses the pipeline operator to pass the object to **Set-CMDistributionPoint**, which modifies the distribution point object.

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
Valid values are: 

- HTTP
- HTTPS

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
Valid values are:

- Internet
- InternetAndIntranet
- Intranet

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
Valid values are:

- None
- Profile100Mbps
- Profile10Mbps
- Profile1Gbps 
- ProfileCustom

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

### -ContentMonitoringPriority
Specifies the content monitoring priority.
Valid values are:

- High
- Highest
- Low
- Lowest
- Medium

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
To create a schedule token object, use the New-CMSchedule cmdlet.

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
Indicates that the cmdlet enables and configures BranchCache for the distribution point.

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

### -EnablePullDP
Enables, when set to $True, the distribution point is able to pull content from other distribution points.

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

When you enable PXE, Configuration Manager installs Windows Deployment Services on the server, if required.
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

### -InputObject
Specifies a distribution point object.
To obtain a distribution point object, use the Get-CMDistributionPoint cmdlet.

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
Returns an object representing the item with which you are working.
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
Valid values are:

- AllowWithAutomaticApproval
- AllowWithManualApproval
- DoNotUse

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMDistributionPoint](./Add-CMDistributionPoint.md)

[Get-CMDistributionPoint](./Get-CMDistributionPoint.md)

[Get-CMSiteSystemServer](./Get-CMSiteSystemServer.md)

[New-CMSchedule](./New-CMSchedule.md)

[Remove-CMDistributionPoint](./Remove-CMDistributionPoint.md)

[Update-CMDistributionPoint](./Update-CMDistributionPoint.md)


