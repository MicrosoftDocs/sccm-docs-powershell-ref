---
description: Sets a SCEP certificate profile.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMCertificateProfileScep
---

# Set-CMCertificateProfileScep

## SYNOPSIS
Sets a SCEP certificate profile.

## SYNTAX

### ByValue (Default)
```
Set-CMCertificateProfileScep [-AllowCertificateOnAnyDevice <Boolean>]
 [-CertificateStore <CertificateStoreType>] [-CertificateTemplateName <String>]
 [-CertificateValidityDays <Int32>] [-Description <String>] [-Eku <Hashtable>]
 [-EnrollmentRenewThresholdPct <Int32>] [-EnrollmentRetryCount <Int32>] [-EnrollmentRetryDelayMins <Int32>]
 [-HashAlgorithm <HashAlgorithmTypes>] -InputObject <IResultObject> [-KeySize <Int32>]
 [-KeyStorageProvider <KeyStorageProviderSettingType>] [-KeyUsage <X509KeyUsageFlags>] [-NewName <String>]
 [-PassThru] [-RequireMultifactor <Boolean>] [-RootCertificate <IResultObject>]
 [-SanType <SubjectAlternativeNameFormatTypes>] [-ScepServerUrl <String[]>]
 [-SubjectType <SubjectNameFormatTypes>] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMCertificateProfileScep [-AllowCertificateOnAnyDevice <Boolean>]
 [-CertificateStore <CertificateStoreType>] [-CertificateTemplateName <String>]
 [-CertificateValidityDays <Int32>] [-Description <String>] [-Eku <Hashtable>]
 [-EnrollmentRenewThresholdPct <Int32>] [-EnrollmentRetryCount <Int32>] [-EnrollmentRetryDelayMins <Int32>]
 [-HashAlgorithm <HashAlgorithmTypes>] -Id <Int32> [-KeySize <Int32>]
 [-KeyStorageProvider <KeyStorageProviderSettingType>] [-KeyUsage <X509KeyUsageFlags>] [-NewName <String>]
 [-PassThru] [-RequireMultifactor <Boolean>] [-RootCertificate <IResultObject>]
 [-SanType <SubjectAlternativeNameFormatTypes>] [-ScepServerUrl <String[]>]
 [-SubjectType <SubjectNameFormatTypes>] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMCertificateProfileScep [-AllowCertificateOnAnyDevice <Boolean>]
 [-CertificateStore <CertificateStoreType>] [-CertificateTemplateName <String>]
 [-CertificateValidityDays <Int32>] [-Description <String>] [-Eku <Hashtable>]
 [-EnrollmentRenewThresholdPct <Int32>] [-EnrollmentRetryCount <Int32>] [-EnrollmentRetryDelayMins <Int32>]
 [-HashAlgorithm <HashAlgorithmTypes>] [-KeySize <Int32>] [-KeyStorageProvider <KeyStorageProviderSettingType>]
 [-KeyUsage <X509KeyUsageFlags>] -Name <String> [-NewName <String>] [-PassThru] [-RequireMultifactor <Boolean>]
 [-RootCertificate <IResultObject>] [-SanType <SubjectAlternativeNameFormatTypes>] [-ScepServerUrl <String[]>]
 [-SubjectType <SubjectNameFormatTypes>] [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCertificateProfileScep** cmdlet updates the settings of a SCEP certificate profile.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a SCEP certificate profile by name
```
PS XYZ:\> Set-CMCertificateProfileScep -Name "TestProfile01" -CertificateStore Machine -Description "Test update" -HashAlgorithm SHA3 -KeySize 1024 -KeyUsage KeyEncipherment -NewName "TestProfile01_updated" -SanType SubjectAltRequireDns
```

This command updates the SEP certificate profile named TestProfile01 and gives it the new name TestProfile01_updated.

### Example 2: Set a SCEP certificate profile by using the pipeline
```
PS XYZ:\> Get-CMCertificateProfileScep -Name "TestProfile02" -Fast | Set-CMCertificateProfileScep -AllowCertificateOnAnyDevice $True -KeyStorageProvider InstallToNGC_FailIfNotPresent
```

This command gets the SEP certificate profile object named TestProfile02 and uses the pipeline operator to pass the object to **Set-CMCertificateProfileScep**, which updates the settings of the profile object.

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateTemplateName
Specifies the name of a certificate template.

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

### -CertificateValidityDays
Specifies, in number of days, the certificate validity period.

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

### -Eku
Specifies the extended key usage.
The values in the hash table define the certificate's intended purpose.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Ekus

Required: False
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
Default value: None
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
Default value: None
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

### -HashAlgorithm
Specifies the hash algorithm.
Valid values are:

- SHA1
- SHA2
- SHA3
- NONE

```yaml
Type: HashAlgorithmTypes
Parameter Sets: (All)
Aliases: HashAlgorithms
Accepted values: NONE, SHA1, SHA2, SHA3

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies the CI_ID of a SCEP certificate profile.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CI_ID, CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a SCEP certificate profile object.
To obtain a SCEP certificate profile object, use the Get-CMCertificateProfileScep function.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Accepted values: 1024, 2048, 4096

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyUsage
Specifies the key usage for the certificate.
Valid values are:

- KeyEncipherment
- DigitalSignature
- None
- EncipherOnly
- CrlSign
- KeyCertSign
- KeyAgreement
- DataEncipherment
- NonRepudiation
- DecipherOnly

```yaml
Type: X509KeyUsageFlags
Parameter Sets: (All)
Aliases: KeyUsages
Accepted values: KeyEncipherment, DigitalSignature

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the SCEP certificate profile.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the SCEP certificate profile.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -RequireMultifactor
Indicates that multi-factor authentication is required during enrollment of devices before issuing certificates to those devices.
This parameter can be used when the InstallToNGC_FailIfNotPresent value is set for the *KeyStorageProvider* parameter.

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

### -RootCertificate
Specifies a trusted root CA certificate object.
To get a trusted root CA certificate, use the Get-CMCertificateProfileTrustedRootCA function.

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
Accepted values: SubjectAltRequireCustom, SubjectAltRequireSpn, SubjectAltRequireAAD, SubjectAltRequireUpn, SubjectAltReqiureEmail, SubjectAltRequireDns

Required: False
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
Default value: None
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

### IResultObject#SMS_ConfigurationPolicy
## NOTES

## RELATED LINKS

[Get-CMCertificateProfileScep](Get-CMCertificateProfileScep.md)

[Get-CMCertificateProfileTrustedRootCA](Get-CMCertificateProfileTrustedRootCA.md)

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[New-CMCertificateProfileScep](New-CMCertificateProfileScep.md)
