---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: E30DA485-2D19-497F-92BA-8BD7F7804602
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

### Example 1: Upgrade a shared distribution point
```
PS C:\>$CIObj = Get-CMDistributionPoint -DistributionPointGroupId "{6617708D-0F98-4898-8D05-9E882C23DCB2}"
PS C:\> Start-CMDistributionPointUpgrade -AllowPreStaging $True -CertificatePath "\\Contoso01\CM\Toolbox\BaseCert.txt" -SharedDistributionPoint $CIObj -SiteCode "CM1"
```

The first command gets the distribution point object that has the ID 6617708D-0F98-4898-8D05-9E882C23DCB2, and stores the object in the $CIObj variable.

The second command upgrades the shared distribution point stored in $CIObj to the Configuration Manager site that has the site code CM1.
The command specifies the import path for the PKI issued certificate that the distribution point uses, and specifies that the distribution point can pre-stage contents.

## PARAMETERS

### -AllowFallbackForContent


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

### -InitiateConnection


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

[Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md)

[Get-CMBoundaryGroup](./Get-CMBoundaryGroup.md)

[Get-CMDistributionPoint](./Get-CMDistributionPoint.md)

[New-CMSchedule](./New-CMSchedule.md)


