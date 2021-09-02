---
description: Upgrade a shared distribution point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/24/2020
schema: 2.0.0
title: Start-CMDistributionPointUpgrade
---

# Start-CMDistributionPointUpgrade

## SYNOPSIS
Upgrades a shared distribution point.

## SYNTAX

### UseImportCertificate (Default)
```
Start-CMDistributionPointUpgrade [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-AllowRespondIncomingPxeRequest <Boolean>] [-CertificatePassword <SecureString>] -CertificatePath <String>
 [-ClientCommunicationMode <ComputerCommunicationType>] [-ClientConnectionType <ClientConnectionTypes>]
 [-ContentValidationPriority <Priority>] -DestinationSiteCode <String> [-EnableAnonymous <Boolean>]
 [-EnableNonWdsPxe <Boolean>] [-EnablePxeSupport <Boolean>] [-EnableUnknownComputerSupport <Boolean>]
 [-ForceWhenDuplicateCertificate <Boolean>] [-InitiateConnection <Boolean>] -InputObject <IResultObject>
 [-InstallationAccount <IResultObject>] [-InstallIis <Boolean>] [-MacAddressForRespondingPxeRequest <String[]>]
 [-MinFreeSpaceMB <Int32>] [-PathForSavingMigratedPackage <String>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>] [-PublicFqdn <String>]
 [-PxePassword <SecureString>] [-PxeServerResponseDelaySec <Int32>]
 [-SecondaryContentLibraryLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-ValidateContentSchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UseSelfSignedCertificate
```
Start-CMDistributionPointUpgrade [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-AllowRespondIncomingPxeRequest <Boolean>] -CertificateExpirationTimeUtc <DateTime>
 [-ClientCommunicationMode <ComputerCommunicationType>] [-ClientConnectionType <ClientConnectionTypes>]
 [-ContentValidationPriority <Priority>] -DestinationSiteCode <String> [-EnableAnonymous <Boolean>]
 [-EnableNonWdsPxe <Boolean>] [-EnablePxeSupport <Boolean>] [-EnableUnknownComputerSupport <Boolean>]
 [-InitiateConnection <Boolean>] -InputObject <IResultObject> [-InstallationAccount <IResultObject>]
 [-InstallIis <Boolean>] [-MacAddressForRespondingPxeRequest <String[]>] [-MinFreeSpaceMB <Int32>]
 [-PathForSavingMigratedPackage <String>] [-PrimaryContentLibraryLocation <DriveType>]
 [-PrimaryPackageShareLocation <DriveType>] [-PublicFqdn <String>] [-PxePassword <SecureString>]
 [-PxeServerResponseDelaySec <Int32>] [-SecondaryContentLibraryLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] [-UserDeviceAffinity <UserDeviceAffinityType>]
 [-ValidateContentSchedule <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMDistributionPointUpgrade** cmdlet upgrades a shared distribution point to a Configuration Manager distribution point.

When you migrate from a Configuration Manager 2007 source hierarchy, you can upgrade a shared distribution point to make it a Configuration Manager distribution point.
You can upgrade distribution points at both primary sites and secondary sites.
The upgrade process removes the distribution point from the Configuration Manager 2007 hierarchy and makes it a site system server in the Configuration Manager hierarchy.
This process also copies the existing content that is on the distributing point to a new location on the distribution point computer.
The upgrade process then modifies the copy of the content to create the Configuration Manager single instance store for use with Configuration Manager content deployment.
Therefore, when you upgrade a distribution point, you do not have to redistribute migrated content that was hosted on the Configuration Manager 2007 distribution point.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Upgrade a shared distribution point

The first command gets the distribution point object that has the ID 6617708D-0F98-4898-8D05-9E882C23DCB2, and stores the object in the $CIObj variable.

The second command upgrades the shared distribution point stored in $CIObj to the Configuration Manager site that has the site code CM1.
The command specifies the import path for the PKI issued certificate that the distribution point uses, and specifies that the distribution point can pre-stage contents.

```powershell
$CIObj = Get-CMDistributionPoint -DistributionPointGroupId "{6617708D-0F98-4898-8D05-9E882C23DCB2}"
Start-CMDistributionPointUpgrade -AllowPreStaging $True -CertificatePath "\\Contoso01\CM\Toolbox\BaseCert.txt" -SharedDistributionPoint $CIObj -SiteCode "CM1"
```

## PARAMETERS

### -AllowFallbackForContent
Indicates whether clients can use a fallback source location for content.

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
Indicates whether the distribution point can pre-stage contents.

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

### -AllowRespondIncomingPxeRequest
Indicates whether the distribution point can respond to pre-boot execution environment (PXE) requests.

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

### -CertificateExpirationTimeUtc
Specifies the date and time when the certificate expires.

```yaml
Type: DateTime
Parameter Sets: UseSelfSignedCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Specifies the password, as a secure string, for the public key infrastructure (PKI) client certificate for the distribution point.

```yaml
Type: SecureString
Parameter Sets: UseImportCertificate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath
Specifies the import path for the PKI issued certificate that the distribution point uses.

```yaml
Type: String
Parameter Sets: UseImportCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientCommunicationMode
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

### -ContentValidationPriority
Specifies the content validation priority.
Valid values are:

- High
- Highest
- Low
- Lowest
- Medium

The default value is Lowest.

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

### -DestinationSiteCode
```yaml
Type: String
Parameter Sets: (All)
Aliases: SiteCode

Required: True
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
Indicates whether the distribution point permits anonymous connections from Configuration Manager clients to the content library.

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

### -EnablePxeSupport
Indicates whether to enable PXE on the distribution point.

When you enable PXE, Configuration Manager installs Windows Deployment Services on the server, if required.
Windows Deployment Service is the service that performs the PXE boot to install operating systems.
After you create the distribution point, Configuration Manager installs a provider in Windows Deployment Services that uses the PXE boot functions.

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

### -ForceWhenDuplicateCertificate
Indicates whether Configuration Manager overwrites a duplicate certificate when you import a PKI client certificate for the distribution point.

```yaml
Type: Boolean
Parameter Sets: UseImportCertificate
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

### -InitiateConnection
Indicates whether the distribution point initiates the connection with the clients.

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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: SharedDistributionPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallationAccount
Specifies a Site System Installation Account.
Configuration Manager 2007 Site Component Manager service uses Site System Installation Accounts to install, reinstall, uninstall, and configure site systems.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallIis
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: InstallInternetServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MacAddressForRespondingPxeRequest
Specifies an array of media access controller (MAC) addresses that the distribution point uses to respond to pre-boot execution environment (PXE) requests.

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

### -MinFreeSpaceMB
Specifies the amount of free space on a drive before Configuration Manager chooses a different drive and continues the copy process to that drive.
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

### -PathForSavingMigratedPackage
Specifies the path for a copy of the migrated content.

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

### -PrimaryContentLibraryLocation
Specifies the primary content location.
Configuration Manager copies content to the primary content location until the amount of free space reaches the value that you specified for the *MinFreeSpaceMB* parameter.
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

### -PrimaryPackageShareLocation
Specifies the primary package share location.
Configuration Manager copies content to the primary package share location until the amount of free space reaches the value that you specified for the *MinFreeSpaceMB* parameter.
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

### -PublicFqdn
Specifies the fully qualified domain name (FQDN) of the site system server that hosts the distribution point.

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

### -PxePassword
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

### -UserDeviceAffinity
Specify how the distribution point associates users with the destination computer for PXE deployments.
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

### -ValidateContentSchedule
Specifies a CMSchedule object.
A CMSchedule object defines the schedule for validating the integrity of content files on the distribution point.
To create a CMSchedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
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

## NOTES

## RELATED LINKS

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[New-CMSchedule](New-CMSchedule.md)
