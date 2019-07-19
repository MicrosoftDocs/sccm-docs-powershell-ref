<<<<<<< HEAD
---
title: Start-CMDistributionPointUpgrade
titleSuffix: Configuration Manager
description: Upgrades a shared distribution point.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: E30DA485-2D19-497F-92BA-8BD7F7804602
online version: https://go.microsoft.com/fwlink/?linkid=834218
schema: 2.0.0
>>>>>>> master
---

# Start-CMDistributionPointUpgrade

## SYNOPSIS
Upgrades a shared distribution point.

## SYNTAX

### UseImportCertificate (Default)
```
Start-CMDistributionPointUpgrade [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-AllowRespondIncomingPxeRequest <Boolean>] [-ClientConnectionType <ClientConnectionTypes>]
 [-ClientCommunicationMode <ComputerCommunicationType>] [-PxePassword <SecureString>]
 [-ContentValidationPriority <Priority>] [-EnableAnonymous <Boolean>] [-EnablePxeSupport <Boolean>]
 [-EnableUnknownComputerSupport <Boolean>] [-InitiateConnection <Boolean>] [-InstallIis <Boolean>]
 [-MacAddressForRespondingPxeRequest <String[]>] [-PublicFqdn <String>] [-PxeServerResponseDelaySec <Int32>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-ValidateContentSchedule <IResultObject>]
 [-CertificatePassword <SecureString>] -CertificatePath <String> -DestinationSiteCode <String>
 [-ForceWhenDuplicateCertificate <Boolean>] [-InstallationAccount <IResultObject>] [-MinFreeSpaceMB <Int32>]
 [-PathForSavingMigratedPackage <String>] [-PrimaryContentLibraryLocation <DriveType>]
 [-PrimaryPackageShareLocation <DriveType>] [-SecondaryContentLibraryLocation <DriveType>]
 [-SecondaryPackageShareLocation <DriveType>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UseSelfSignedCertificate
```
Start-CMDistributionPointUpgrade [-AllowFallbackForContent <Boolean>] [-AllowPreStaging <Boolean>]
 [-AllowRespondIncomingPxeRequest <Boolean>] [-ClientConnectionType <ClientConnectionTypes>]
 [-ClientCommunicationMode <ComputerCommunicationType>] [-PxePassword <SecureString>]
 [-ContentValidationPriority <Priority>] [-EnableAnonymous <Boolean>] [-EnablePxeSupport <Boolean>]
 [-EnableUnknownComputerSupport <Boolean>] [-InitiateConnection <Boolean>] [-InstallIis <Boolean>]
 [-MacAddressForRespondingPxeRequest <String[]>] [-PublicFqdn <String>] [-PxeServerResponseDelaySec <Int32>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-ValidateContentSchedule <IResultObject>]
 -CertificateExpirationTimeUtc <DateTime> -DestinationSiteCode <String> [-InstallationAccount <IResultObject>]
 [-MinFreeSpaceMB <Int32>] [-PathForSavingMigratedPackage <String>]
 [-PrimaryContentLibraryLocation <DriveType>] [-PrimaryPackageShareLocation <DriveType>]
 [-SecondaryContentLibraryLocation <DriveType>] [-SecondaryPackageShareLocation <DriveType>]
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMDistributionPointUpgrade** cmdlet upgrades a shared distribution point to a Microsoft System Center Configuration Manager distribution point.

When you migrate from a Microsoft System Center Configuration Manager 2007 source hierarchy, you can upgrade a shared distribution point to make it a System Center Configuration Manager distribution point.
You can upgrade distribution points at both primary sites and secondary sites.
The upgrade process removes the distribution point from the Configuration Manager 2007 hierarchy and makes it a site system server in the System Center Configuration Manager hierarchy.
This process also copies the existing content that is on the distributing point to a new location on the distribution point computer.
The upgrade process then modifies the copy of the content to create the System Center Configuration Manager single instance store for use with System Center Configuration Manager content deployment.
Therefore, when you upgrade a distribution point, you do not have to redistribute migrated content that was hosted on the Configuration Manager 2007 distribution point.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Upgrade a shared distribution point
```
PS XYZ:\> $CIObj = Get-CMDistributionPoint -DistributionPointGroupId "{6617708D-0F98-4898-8D05-9E882C23DCB2}"
PS XYZ:\> Start-CMDistributionPointUpgrade -AllowPreStaging $True -CertificatePath "\\Contoso01\CM\Toolbox\BaseCert.txt" -SharedDistributionPoint $CIObj -SiteCode "CM1"
```

The first command gets the distribution point object that has the ID 6617708D-0F98-4898-8D05-9E882C23DCB2, and stores the object in the $CIObj variable.

The second command upgrades the shared distribution point stored in $CIObj to the Configuration Manager site that has the site code CM1.
The command specifies the import path for the PKI issued certificate that the distribution point uses, and specifies that the distribution point can pre-stage contents.

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

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[New-CMSchedule](New-CMSchedule.md)
