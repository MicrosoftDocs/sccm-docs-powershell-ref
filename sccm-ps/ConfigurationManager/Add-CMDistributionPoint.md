---
description: Adding distribution points.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/06/2023
schema: 2.0.0
title: Add-CMDistributionPoint
---

# Add-CMDistributionPoint

## SYNOPSIS

Add a distribution point role.

## SYNTAX

### DistributionPointWithSelfCertByValue (Default)
```
Add-CMDistributionPoint [-AllowFallbackForContent] [-AllowPreStaging] [-AllowProxyTraffic] [-AllowPxeResponse]
 -CertificateExpirationTimeUtc <DateTime> [-ClientConnectionType <ClientConnectionTypes>]
 [-ContentMonitoringPriority <Priority>] [-ContentValidationSchedule <IResultObject>] [-Description <String>]
 [-EnableAnonymous] [-EnableBranchCache] [-EnableContentValidation] [-EnableLedbat] [-EnableMulticast]
 [-EnableNonWdsPxe] [-EnablePullDP] [-EnablePxe] [-EnableScheduledMulticast <Boolean>] [-EnableSsl]
 [-EnableUnknownComputerSupport] [-EndIPAddress <String>] [-EndUdpPort <Int32>] [-Force]
 -InputObject <IResultObject> [-InstallInternetServer] [-MacAddressForRespondingPxeRequest <String[]>]
 [-MinimumFreeSpaceMB <Int32>] [-MinimumSessionSize <Int32>] [-MulticastMaximumClientCount <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-PxePassword <SecureString>] [-PxeServerResponseDelaySec <Int32>]
 [-SecondaryContentLibraryLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 [-SessionStartDelayMins <Int32>] [-SourceDistributionPoint <String[]>] [-SourceDPRank <Int32[]>]
 [-StartIPAddress <String>] [-StartUdpPort <Int32>] [-UserDeviceAffinity <UserDeviceAffinityType>]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### DistributionPointWithSelfCert
```
Add-CMDistributionPoint [-AllowFallbackForContent] [-AllowPreStaging] [-AllowProxyTraffic] [-AllowPxeResponse]
 -CertificateExpirationTimeUtc <DateTime> [-ClientConnectionType <ClientConnectionTypes>]
 [-ContentMonitoringPriority <Priority>] [-ContentValidationSchedule <IResultObject>] [-Description <String>]
 [-EnableAnonymous] [-EnableBranchCache] [-EnableContentValidation] [-EnableLedbat] [-EnableMulticast]
 [-EnableNonWdsPxe] [-EnablePullDP] [-EnablePxe] [-EnableScheduledMulticast <Boolean>] [-EnableSsl]
 [-EnableUnknownComputerSupport] [-EndIPAddress <String>] [-EndUdpPort <Int32>] [-Force]
 [-InstallInternetServer] [-MacAddressForRespondingPxeRequest <String[]>] [-MinimumFreeSpaceMB <Int32>]
 [-MinimumSessionSize <Int32>] [-MulticastMaximumClientCount <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-PxePassword <SecureString>] [-PxeServerResponseDelaySec <Int32>]
 [-SecondaryContentLibraryLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 [-SessionStartDelayMins <Int32>] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-SourceDistributionPoint <String[]>] [-SourceDPRank <Int32[]>] [-StartIPAddress <String>]
 [-StartUdpPort <Int32>] [-UserDeviceAffinity <UserDeviceAffinityType>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DistributionPointwithUserSpecifiedCert
```
Add-CMDistributionPoint [-AllowFallbackForContent] [-AllowPreStaging] [-AllowProxyTraffic] [-AllowPxeResponse]
 -CertificatePassword <SecureString> -CertificatePath <String> [-ClientConnectionType <ClientConnectionTypes>]
 [-ContentMonitoringPriority <Priority>] [-ContentValidationSchedule <IResultObject>] [-Description <String>]
 [-EnableAnonymous] [-EnableBranchCache] [-EnableContentValidation] [-EnableLedbat] [-EnableMulticast]
 [-EnableNonWdsPxe] [-EnablePullDP] [-EnablePxe] [-EnableScheduledMulticast <Boolean>] [-EnableSsl]
 [-EnableUnknownComputerSupport] [-EndIPAddress <String>] [-EndUdpPort <Int32>] [-Force]
 [-InstallInternetServer] [-MacAddressForRespondingPxeRequest <String[]>] [-MinimumFreeSpaceMB <Int32>]
 [-MinimumSessionSize <Int32>] [-MulticastMaximumClientCount <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-PxePassword <SecureString>] [-PxeServerResponseDelaySec <Int32>]
 [-SecondaryContentLibraryLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 [-SessionStartDelayMins <Int32>] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-SourceDistributionPoint <String[]>] [-SourceDPRank <Int32[]>] [-StartIPAddress <String>]
 [-StartUdpPort <Int32>] [-UserDeviceAffinity <UserDeviceAffinityType>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DistributionPointwithUserSpecifiedCertByValue
```
Add-CMDistributionPoint [-AllowFallbackForContent] [-AllowPreStaging] [-AllowProxyTraffic] [-AllowPxeResponse]
 -CertificatePassword <SecureString> -CertificatePath <String> [-ClientConnectionType <ClientConnectionTypes>]
 [-ContentMonitoringPriority <Priority>] [-ContentValidationSchedule <IResultObject>] [-Description <String>]
 [-EnableAnonymous] [-EnableBranchCache] [-EnableContentValidation] [-EnableLedbat] [-EnableMulticast]
 [-EnableNonWdsPxe] [-EnablePullDP] [-EnablePxe] [-EnableScheduledMulticast <Boolean>] [-EnableSsl]
 [-EnableUnknownComputerSupport] [-EndIPAddress <String>] [-EndUdpPort <Int32>] [-Force]
 -InputObject <IResultObject> [-InstallInternetServer] [-MacAddressForRespondingPxeRequest <String[]>]
 [-MinimumFreeSpaceMB <Int32>] [-MinimumSessionSize <Int32>] [-MulticastMaximumClientCount <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-PxePassword <SecureString>] [-PxeServerResponseDelaySec <Int32>]
 [-SecondaryContentLibraryLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 [-SessionStartDelayMins <Int32>] [-SourceDistributionPoint <String[]>] [-SourceDPRank <Int32[]>]
 [-StartIPAddress <String>] [-StartUdpPort <Int32>] [-UserDeviceAffinity <UserDeviceAffinityType>]
 [-UserName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **Add-CMDistributionPoint** cmdlet creates a distribution point on a site system server.
A distribution point is a site system role that Configuration Manager uses to store files for clients to download. Files such as application content, software packages, software updates, operating system images, and boot images are stored.

Before you can make content available to client computers, assign a site system server as a distribution point.
You can add the distribution point site role to a new site system server or add the site role to an existing site system server.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a site by using a site system server object

The first command creates a date object for 30 years from the current date and stores the object in the **$Date** variable.

The second command gets the site system server object named **MySiteSys_11310.Contoso.com** and stores the object in the **$SystemServer** variable.

The third command adds a distribution point to the site system server stored in **$SystemServer**, and sets the certificate expiration to the date stored in **$Date**.

```powershell
$Date = [DateTime]::Now.AddYears(30)
$SystemServer = Get-CMSiteSystemServer -SiteSystemServerName "MySiteSys_11310.Contoso.com"
Add-CMDistributionPoint -InputObject $SystemServer -CertificateExpirationTimeUtc $Date
```

### Example 2: Add a site by using the pipeline

The first command creates a date object for 30 years from the current date and stores the object in the **$Date** variable.

The second command gets the site system server object named **MySiteSys_11310.Contoso.com**. It then uses the pipeline operator to pass the object to **Add-DistributionPoint**, which adds a distribution point to the site system server object. It then sets the certificate expiration to the date stored in **$Date**.

```powershell
$Date = [DateTime]::Now.AddYears(30)
Get-CMSiteSystemServer -SiteSystemServerName "MySiteSys_11310.Contoso.com" | Add-CMDistributionPoint -CertificateExpirationTimeUtc $Date
```

## PARAMETERS

### -AllowFallbackForContent
Indicates that clients outside of the boundary groups associated with a site system can fall back. Those clients can use this site system as a source location for content when no other site systems are available.

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

### -AllowPreStaging
Indicates that the distribution point can prestage contents.

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

### -AllowProxyTraffic

Enables the site system to use a proxy server when it connects to the internet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableCloudGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPxeResponse
Indicates that the distribution point can respond to PXE requests.

```yaml
Type: SwitchParameter
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
Parameter Sets: DistributionPointWithSelfCertByValue, DistributionPointWithSelfCert
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Specifies, as a secure string, the password for a PKI client certificate.

```yaml
Type: SecureString
Parameter Sets: DistributionPointwithUserSpecifiedCert, DistributionPointwithUserSpecifiedCertByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath
Specifies the import path for a PKI client certificate.

```yaml
Type: String
Parameter Sets: DistributionPointwithUserSpecifiedCert, DistributionPointwithUserSpecifiedCertByValue
Aliases:

Required: True
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

### -EnableAnonymous
Indicates that the distribution point permits anonymous connections from Configuration Manager clients to the content library.

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

### -EnableBranchCache
Indicates that clients that use Windows BranchCache are allowed to download content from an on-premises distribution point.
Content downloads from cloud-based distribution points can always be shared by clients that use Windows BranchCache.

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

### -EnableContentValidation
Indicates that content validation is enabled for this distribution point.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableValidateContent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableLedbat

Enable distribution points to use network congestion control with Windows LEDBAT. This feature can adjust the download speed to use the unused network bandwidth.

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

### -EnableMulticast
Indicates that multicast is enabled for this distribution point.

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

### -EnableNonWdsPxe

Indicates whether the Configuration Manager PXE responder is enabled on the distribution point. When you enable a PXE responder without Windows Deployment Service (WDS), Configuration Manager installs its PXE responder service on the distribution point.

For more information, see [enable PXE on the distribution point](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points#bkmk_config-pxe).

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

### -EnablePullDP

When set to `$True`, the distribution point is able to pull content from other distribution points.

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

### -EnablePxe
Indicates that PXE is enabled on the distribution point.

When you enable PXE, Configuration Manager installs Windows Deployment Services on the server, if necessary.
Windows Deployment Service is the service that performs the PXE boot to install operating systems.
After you create the distribution point, Configuration Manager installs a provider in Windows Deployment Services that uses the PXE boot functions.

```yaml
Type: SwitchParameter
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

### -EnableSsl
Indicates that SSL is enabled on this distribution point.

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

### -EnableUnknownComputerSupport
Indicates that support for unknown computers is enabled.
Unknown computers are computers that aren't managed by Configuration Manager.

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

### -InputObject

Specify a site system server object to add the distribution point role. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: DistributionPointWithSelfCertByValue, DistributionPointwithUserSpecifiedCertByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```
### -InitialMPForLookup
It's required (and requires) when providing -PreferredMPEnabled parameter. It expects a string input that represents different lookup MPs separated by the * symbol. MPs are filtered based on the Site code of the DP, if the MP's site code is different, an error is thrown.

```yaml
Type: String
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallInternetServer
Indicates that Configuration Manager installs and configures Internet Information Services (IIS) on the server if it isn't already installed. The distribution point role requires IIS.

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

### -MinimumFreeSpaceMB
Specifies the amount of free space to reserve on each drive used by this distribution point.
When this limit is reached, Configuration Manager chooses a different drive and continues the copy process to that drive.
Content files can span multiple drives.

Starting in version 2107, the default minimum free space changed from 50 MB to **500 MB**.

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
### -PreferredMPEnabled

It's a switch parameter. The presence of the parameter indicates that the dynamic MP usage is enabled. PXE has to be enabled on the Distribution Point before using this parameter.

```yaml
Type: SwitchParameter
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### -PrimaryContentLibraryLocation

Specifies the primary content location.
Configuration Manager copies content to the primary content location until the amount of free space reaches the value that you specified for the **MinimumFreeSpaceMB** parameter.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryPackageShareLocation

Specifies the primary package share location.
Configuration Manager copies content to the primary package share location until the amount of free space reaches the value that you specified for the **MinimumFreeSpaceMB** parameter.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

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
Specifies, in seconds, how long the distribution point delays before it responds to computer requests when you're using multiple PXE-enabled distribution points.
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

### -SecondaryContentLibraryLocation
Specifies the secondary content location.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondaryPackageShareLocation
Specifies the secondary package share location.

```yaml
Type: DriveType
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z

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

Specify the three-character code for the site that hosts this site system role.

Starting in version 2111, you can't specify the central administration site (CAS) for this parameter, which doesn't support any client-facing site system roles.

```yaml
Type: String
Parameter Sets: DistributionPointWithSelfCert, DistributionPointwithUserSpecifiedCert
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server to host a site system role.

```yaml
Type: String
Parameter Sets: DistributionPointWithSelfCert, DistributionPointwithUserSpecifiedCert
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
Specifies an array containing the priorities for the distribution point sources from which this distribution point can pull content.
Source distribution points with the same priority are randomly selected.

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

For more information on this return object and its properties, see [SMS_SCI_SysResUse server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_sci_sysresuse-server-wmi-class).

## RELATED LINKS

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[New-CMSchedule](New-CMSchedule.md)

[Set-CMDistributionPoint](Set-CMDistributionPoint.md)

[Update-CMDistributionPoint](Update-CMDistributionPoint.md)

[Remove-CMDistributionPoint](Remove-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Install and configure distribution points in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points)
