---
description: Adds a distribution point.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMDistributionPoint
---

# Add-CMDistributionPoint

## SYNOPSIS
Adds a distribution point.

## SYNTAX

### DistributionPointWithSelfCertByValue (Default)
```
Add-CMDistributionPoint -InputObject <IResultObject> [-InstallInternetServer]
 [-ClientConnectionType <ClientConnectionTypes>] [-AllowProxyTraffic] [-Description <String>]
 [-EnableAnonymous] -CertificateExpirationTimeUtc <DateTime> [-AllowPreStaging] [-MinimumFreeSpaceMB <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-SecondaryContentLibraryLocation <DriveType>]
 [-PrimaryPackageShareLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>] [-EnablePxe]
 [-AllowPxeResponse] [-EnableUnknownComputerSupport] [-EnableNonWdsPxe] [-PxePassword <SecureString>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-MacAddressForRespondingPxeRequest <String[]>]
 [-PxeServerResponseDelaySec <Int32>] [-EnableMulticast] [-UserName <String>] [-StartIPAddress <String>]
 [-EndIPAddress <String>] [-StartUdpPort <Int32>] [-EndUdpPort <Int32>] [-MulticastMaximumClientCount <Int32>]
 [-EnableScheduledMulticast <Boolean>] [-SessionStartDelayMins <Int32>] [-MinimumSessionSize <Int32>]
 [-EnableContentValidation] [-ContentValidationSchedule <IResultObject>]
 [-ContentMonitoringPriority <Priority>] [-EnablePullDP] [-SourceDistributionPoint <String[]>]
 [-SourceDPRank <Int32[]>] [-EnableSsl] [-EnableBranchCache] [-EnableLedbat] [-AllowFallbackForContent]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DistributionPointwithUserSpecifiedCertByValue
```
Add-CMDistributionPoint -InputObject <IResultObject> [-InstallInternetServer]
 [-ClientConnectionType <ClientConnectionTypes>] [-AllowProxyTraffic] [-Description <String>]
 [-EnableAnonymous] -CertificatePath <String> -CertificatePassword <SecureString> [-AllowPreStaging]
 [-MinimumFreeSpaceMB <Int32>] [-PrimaryContentLibraryLocation <DriveType>]
 [-SecondaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] [-EnablePxe] [-AllowPxeResponse] [-EnableUnknownComputerSupport]
 [-EnableNonWdsPxe] [-PxePassword <SecureString>] [-UserDeviceAffinity <UserDeviceAffinityType>]
 [-MacAddressForRespondingPxeRequest <String[]>] [-PxeServerResponseDelaySec <Int32>] [-EnableMulticast]
 [-UserName <String>] [-StartIPAddress <String>] [-EndIPAddress <String>] [-StartUdpPort <Int32>]
 [-EndUdpPort <Int32>] [-MulticastMaximumClientCount <Int32>] [-EnableScheduledMulticast <Boolean>]
 [-SessionStartDelayMins <Int32>] [-MinimumSessionSize <Int32>] [-EnableContentValidation]
 [-ContentValidationSchedule <IResultObject>] [-ContentMonitoringPriority <Priority>] [-EnablePullDP]
 [-SourceDistributionPoint <String[]>] [-SourceDPRank <Int32[]>] [-EnableSsl] [-EnableBranchCache]
 [-EnableLedbat] [-AllowFallbackForContent] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DistributionPointWithSelfCert
```
Add-CMDistributionPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-InstallInternetServer]
 [-ClientConnectionType <ClientConnectionTypes>] [-AllowProxyTraffic] [-Description <String>]
 [-EnableAnonymous] -CertificateExpirationTimeUtc <DateTime> [-AllowPreStaging] [-MinimumFreeSpaceMB <Int32>]
 [-PrimaryContentLibraryLocation <DriveType>] [-SecondaryContentLibraryLocation <DriveType>]
 [-PrimaryPackageShareLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>] [-EnablePxe]
 [-AllowPxeResponse] [-EnableUnknownComputerSupport] [-EnableNonWdsPxe] [-PxePassword <SecureString>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-MacAddressForRespondingPxeRequest <String[]>]
 [-PxeServerResponseDelaySec <Int32>] [-EnableMulticast] [-UserName <String>] [-StartIPAddress <String>]
 [-EndIPAddress <String>] [-StartUdpPort <Int32>] [-EndUdpPort <Int32>] [-MulticastMaximumClientCount <Int32>]
 [-EnableScheduledMulticast <Boolean>] [-SessionStartDelayMins <Int32>] [-MinimumSessionSize <Int32>]
 [-EnableContentValidation] [-ContentValidationSchedule <IResultObject>]
 [-ContentMonitoringPriority <Priority>] [-EnablePullDP] [-SourceDistributionPoint <String[]>]
 [-SourceDPRank <Int32[]>] [-EnableSsl] [-EnableBranchCache] [-EnableLedbat] [-AllowFallbackForContent]
 [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DistributionPointwithUserSpecifiedCert
```
Add-CMDistributionPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-InstallInternetServer]
 [-ClientConnectionType <ClientConnectionTypes>] [-AllowProxyTraffic] [-Description <String>]
 [-EnableAnonymous] -CertificatePath <String> -CertificatePassword <SecureString> [-AllowPreStaging]
 [-MinimumFreeSpaceMB <Int32>] [-PrimaryContentLibraryLocation <DriveType>]
 [-SecondaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] [-EnablePxe] [-AllowPxeResponse] [-EnableUnknownComputerSupport]
 [-EnableNonWdsPxe] [-PxePassword <SecureString>] [-UserDeviceAffinity <UserDeviceAffinityType>]
 [-MacAddressForRespondingPxeRequest <String[]>] [-PxeServerResponseDelaySec <Int32>] [-EnableMulticast]
 [-UserName <String>] [-StartIPAddress <String>] [-EndIPAddress <String>] [-StartUdpPort <Int32>]
 [-EndUdpPort <Int32>] [-MulticastMaximumClientCount <Int32>] [-EnableScheduledMulticast <Boolean>]
 [-SessionStartDelayMins <Int32>] [-MinimumSessionSize <Int32>] [-EnableContentValidation]
 [-ContentValidationSchedule <IResultObject>] [-ContentMonitoringPriority <Priority>] [-EnablePullDP]
 [-SourceDistributionPoint <String[]>] [-SourceDPRank <Int32[]>] [-EnableSsl] [-EnableBranchCache]
 [-EnableLedbat] [-AllowFallbackForContent] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDistributionPoint** cmdlet creates a distribution point on a site system server.
A distribution point is a site system role that Configuration Manager uses to store files for clients to download, such as application content, software packages, software updates, operating system images, and boot images.

You must designate a site system server as a distribution point before you can make content available to client computers.
You can add the distribution point site role to a new site system server or add the site role to an existing site system server.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a site by using a site system server object
```
PS XYZ:\> $Date = [DateTime]::Now.AddYears(30)
PS XYZ:\> $SystemServer = Get-CMSiteSystemServer -SiteSystemServerName "MySiteSys_11310.Contoso.com"
PS XYZ:\> Add-CMDistributionPoint -InputObject $SystemServer -CertificateExpirationTimeUtc $Date
```

The first command creates a date object for thirty years from the current date and stores the object in the $Date variable.

The second command gets the site system server object named MySiteSys_11310.Contoso.com and stores the object in the $SystemServer variable.

The third command adds a distribution point to the site system server stored in $SystemServer, and sets the certificate expiration to the date stored in $Date.

### Example 2: Add a site by using the pipeline
```
PS XYZ:\> $Date = [DateTime]::Now.AddYears(30)
PS XYZ:\> Get-CMSiteSystemServer -SiteSystemServerName "MySiteSys_11310.Contoso.com" | Add-CMDistributionPoint -CertificateExpirationTimeUtc $Date
```

The first command creates a date object for thirty years from the current date and stores the object in the $Date variable.

The second command gets the site system server object named MySiteSys_11310.Contoso.com and uses the pipeline operator to pass the object to **Add-DistributionPoint**, which adds a distribution point to the site system server object and sets the certificate expiration to the date stored in $Date.

## PARAMETERS

### -AllowFallbackForContent
Indicates that clients outside of the boundary groups associated with a site system can fall back and use this site system as a source location for content when no other site systems are available.

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
Indicates that the distribution point can pre-stage contents.

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
Parameter Sets: DistributionPointwithUserSpecifiedCertByValue, DistributionPointwithUserSpecifiedCert
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
Parameter Sets: DistributionPointwithUserSpecifiedCertByValue, DistributionPointwithUserSpecifiedCert
Aliases:

Required: True
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

### -ContentMonitoringPriority
Specifies the content monitoring priority.
Valid values are:

- Highest
- High
- Medium
- Low
- Lowest

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
Indicates that the cmdlet enables and configures BranchCache for the distribution point.

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
Enables the distribution point to pull content from other distribution points.

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

When you enable PXE, Configuration Manager installs Windows Deployment Services on the server, if required.
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
Unknown computers are computers that are not managed by Configuration Manager.

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
Starting in version 1910, use the `-Force` switch to add a duplicated certificate.

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

### -InputObject
Specifies a site system server object.
To obtain a site system server object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

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

### -InstallInternetServer
Indicates that Configuration Manager installs and configures Internet Information Services (IIS) on the server if it is not already installed.
IIS must be installed on all distribution points.

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

### -PrimaryContentLibraryLocation
Specifies the primary content location.
Configuration Manager copies content to the primary content location until the amount of free space reaches the value that you specified for the *MinimumFreeSpaceMB* parameter.
Valid values are:

- Automatic.
- Drive letter from A: through Z:

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
Configuration Manager copies content to the primary package share location until the amount of free space reaches the value that you specified for the *MinimumFreeSpaceMB* parameter.
Valid values are:

- Automatic.
- Drive letter from A: through Z:.

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

### -SecondaryContentLibraryLocation
Specifies the secondary content location.
Valid values are:

- Automatic.
- Drive letter from A: through Z:.

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
Valid values are:

- Automatic.
- Drive letter from A: through Z:.

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
Specifies the site code for the Configuration Manager site that hosts this site system role.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMSiteSystemServer](Get-CMSiteSystemServer.md)

[New-CMSchedule](New-CMSchedule.md)

[Set-CMDistributionPoint](Set-CMDistributionPoint.md)

[Update-CMDistributionPoint](Update-CMDistributionPoint.md)

[Remove-CMDistributionPoint](Remove-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)


