---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834298
schema: 2.0.0
ms.assetid: FF85464C-9235-47F3-8981-D97C793053A8
---

# New-CMCertificateProfileScep

## SYNOPSIS
Creates a SCEP certificate profile.

## SYNTAX

```
New-CMCertificateProfileScep [-AllowCertificateOnAnyDevice <Boolean>]
 [-CertificateStore <CertificateStoreType>] -CertificateTemplateName <String> -CertificateValidityDays <Int32>
 [-Description <String>] -Eku <Hashtable> [-EnrollmentRenewThresholdPct <Int32>]
 [-EnrollmentRetryCount <Int32>] [-EnrollmentRetryDelayMins <Int32>] -HashAlgorithm <HashAlgorithmTypes>
 [-KeySize <Int32>] [-KeyStorageProvider <KeyStorageProviderSettingType>] -KeyUsage <X509KeyUsageFlags>
 -Name <String> [-RequireMultifactor] -RootCertificate <IResultObject>
 -SanType <SubjectAlternativeNameFormatTypes> [-ScepServerUrl <String[]>]
 [-SubjectType <SubjectNameFormatTypes>] -SupportedPlatform <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCertificateProfileScep** cmdlet creates a Simple Certificate Enrollment Protocol (SCEP) certificate profile.

Note:  You must create a trusted CA certificate profile before you can create an SCEP certificate profile.
For information about creating a trusted CA certificate profile, see the New-CMCertificateProfileTrustedRootCA cmdlet.

## EXAMPLES

### Example 1: Create a SCEP certificate profile
```
PS C:\> New-CMCertificateProfileScep -CertificateTemplateName "TestTemplate01" -CertificateValidityDays 10 -Eku @{ "name1" ="1.2.3.4"; "name2" = "1.2.3.4.5" } -HashAlgorithm SHA2 -KeyUsage KeyEncipherment -Name "TestSCEPProf01" -RootCertificate (New-CMCertificateProfileTrustedRootCA -Name testing -Path "\\Server\Sharefolder\RootCA.cer" -SupportedPlatform (Get-CMSupportedPlatform  -Fast -Name "All Windows 10*Client")) -SanType SubjectAltReqiureEmail -SupportedPlatform (Get-CMSupportedPlatform  -Fast -Name "All Windows 10*Client")
```

This command creates a trusted root CA certificate, and gets all Windows 10 Client supported platforms.
The command then creates a SEP certificate profile using the newly created trusted root CA certificate.

### Example 2: Create a SCEP certificate profile and set the certificate store to User
```
PS C:\> New-CMCertificateProfileScep -CertificateTemplateName "TestTemplate02" -CertificateValidityDays 10 -Eku @{ "name1" ="1.2.3.4"; "name2" = "1.2.3.4.5" } -HashAlgorithm ShA1 -KeyUsage Digitalsignature -Name "TestSCEPProf02" -RootCertificate (New-CMCertificateProfileTrustedRootCA -Name testingSecond -Path "\\Server\Sharefolder\RootCA.cer" -SupportedPlatform (Get-CMSupportedPlatform  -Fast -Name "All Windows 10*Client")) -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client") -CertificateStore User -Description "Test description" -EnrollmentRenewThresholdPct 2 -EnrollmentRetryCount 5 -EnrollmentRetryDelayMins 7 -KeySize 2048 -KeyStorageProvider InstallToTPM_FailIfNotPresent -RequireMultiFactor -SubjectType SubjectRequireEmail -SanType SubjectAltReqiureEmail
```

This command creates a trusted root CA certificata, and gets all Windows 10 Client supported platforms.
The command then creates a SCEP certificate using the newly created root CA certificate and setting the certificate store to User.

## PARAMETERS

### -AllowCertificateOnAnyDevice
Indicates whether to allow certificate enrollment on any device.

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

### -CertificateStore
Specifies the certificate type.
Valid values are:

- Machine
- User

```yaml
Type: CertificateStoreType
Parameter Sets: (All)
Aliases:
Accepted values: Machine, User

Required: False
Position: Named
Default value: User
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateTemplateName
Specifies the name of a certificate template.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateValidityDays
Specifies, in number of days, the certificate validity period.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
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

### -Description
Specifies a description for the SCEP certificate profile.

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

### -Eku
Specifies the extended key usage.
The values in the hash table define the certificate's intended purpose.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Ekus

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnrollmentRenewThresholdPct
Specifies the percentage of the certificate lifetime that remains before the device requests renewal of the certificate.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnrollmentRetryCount
Specifies the number of times that the device automatically retries the certificate request to the server that is running the Network Device Enrollment Service.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 3
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnrollmentRetryDelayMins
Specifies the interval, in minutes, between each enrollment attempt when you use CA manager approval before the issuing CA processes the certificate request.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
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

### -HashAlgorithm
Specifies the hash algorithm.
Valid values are:

- SHA1
- SHA2
- SHA3

```yaml
Type: HashAlgorithmTypes
Parameter Sets: (All)
Aliases: HashAlgorithms
Accepted values: SHA1, SHA2, SHA3

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeySize
Specifies the size of the key.
Valid values are:

- 1024
- 2048

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:
Accepted values: 1024, 2048

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyStorageProvider
Specifies the Key Storage Provider (KSP) for the SCEP enrollment.
Valid values are:

- None
- InstallToTPM_FailIfNotPresent
- InstallToTPM_IfPresent
- InstallToSoftwareKeyStorageProvider
- InstallToNGC_FailIfNotPresent

```yaml
Type: KeyStorageProviderSettingType
Parameter Sets: (All)
Aliases:
Accepted values: None, InstallToTPM_FailIfNotPresent, InstallToTPM_IfPresent, InstallToSoftwareKeyStorageProvider, InstallToNGC_FailIfNotPresent

Required: False
Position: Named
Default value: InstallToTPM_IfPresent
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyUsage
Specifies the key usage for the certificate.
Valid values are:

- KeyEncipherment
- DigitalSignature

```yaml
Type: X509KeyUsageFlags
Parameter Sets: (All)
Aliases:
Accepted values: KeyEncipherment, DigitalSignature

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the SCEP certificate profile.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RequireMultifactor
Indicates that multi-factor authentication is required during enrollment of devices before issuing certificates to those devices.
This parameter can be used when the InstallToNGC_FailIfNotPresent value is set for the *KeyStorageProvider* parameter.

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

### -RootCertificate
Specifies a trusted root CA certificate object.
To get a trusted root CA certificate, use the Get-CMCertificateProfileTrustedRootCA function.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SanType
Specifies the subject alternative name.
Valid values are:

- SubjectAltRequireSpn
- SubjectAltRequireUpn
- SubjectAltReqiureEmail
- SubjectAltRequireDns

```yaml
Type: SubjectAlternativeNameFormatTypes
Parameter Sets: (All)
Aliases: SanTypes
Accepted values: SubjectAltRequireSpn, SubjectAltRequireUpn, SubjectAltReqiureEmail, SubjectAltRequireDns

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScepServerUrl
Specifies an array of URLs for the Network Device Enrollment Service (NDES) servers that will issue certificates via SCEP.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ScepServerUrls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubjectType
Specifies the subject name format.
Valid values are:

- SubjectRequireCommonNameAsEmail
- SubjectRequireCommonNameAsDeviceName
- SubjectRequireCommonNameAsOSName
- SubjectRequireCommonNameAsIMEI
- SubjectRequireCommonNameAsMEID
- SubjectRequireCommonNameAsSerialNumber
- SubjectRequireCommonNameAsDeviceType
- SubjectRequireCommonNameAsWiFiMAC
- SubjectRequireCommonNameAsEthernetMAC
- SubjectRequireAsCustomString
- SubjectRequireDnsAsCN
- SubjectRequireEmail
- SubjectRequireCommonName
- SubjectRequireDirectoryPath

```yaml
Type: SubjectNameFormatTypes
Parameter Sets: (All)
Aliases: SubjectTypes
Accepted values: SubjectRequireCommonNameAsEmail, SubjectRequireCommonNameAsDeviceName, SubjectRequireCommonNameAsOSName, SubjectRequireCommonNameAsIMEI, SubjectRequireCommonNameAsMEID, SubjectRequireCommonNameAsSerialNumber, SubjectRequireCommonNameAsDeviceType, SubjectRequireCommonNameAsWiFiMAC, SubjectRequireCommonNameAsEthernetMAC, SubjectRequireAsCustomString, SubjectRequireDnsAsCN, SubjectRequireEmail, SubjectRequireCommonName, SubjectRequireDirectoryPath

Required: False
Position: Named
Default value: SubjectRequireCommonName
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupportedPlatform
Specifies a supported platform object.
To obtain a supported platform object, use the Get-CMSupportedPlatform cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SupportedPlatforms

Required: True
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

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Get-CMCertificateProfileScep](./Get-CMCertificateProfileScep.md)

[Get-CMCertificateProfileTrustedRootCA](./Get-CMCertificateProfileTrustedRootCA.md)

[Get-CMSupportedPlatform](./Get-CMSupportedPlatform.md)

[Set-CMCertificateProfileScep](./Set-CMCertificateProfileScep.md)
