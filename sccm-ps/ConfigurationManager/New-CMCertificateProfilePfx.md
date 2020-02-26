---
description: Creates a PFX certificate profile.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMCertificateProfilePfx
---

# New-CMCertificateProfilePfx

## SYNOPSIS
Creates a PFX certificate profile.

## SYNTAX

```
New-CMCertificateProfilePfx [-Description <String>] [-KeyStorageProvider <KeyStorageProviderSettingType>]
 -Name <String> -SupportedPlatform <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCertificateProfilePfx** cmdlet creates a Personal Information Exchange (PFX) certificate profile.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a PFX certificate profile
```
PS XYZ:\> New-CMCertificateProfilePfx -Name "TestCertificatieProfilePfx1" -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client")
```

This command creates a PFX certificate profile named TestCertificatieProfilePfx1 for all Windows 10 Client platforms.

### Example 2: Create a PFX certificate profile to install to TPM
```
PS XYZ:\> New-CMCertificateProfilePfx -Name "Test2" -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client") -Description "Test cmcertificationprofilepfx description" -KeyStorageProvider InstallToTPM_IfPresent
```

This command creates a PFX certificate profile named Test2 for all Windows 10 Client platforms and sets the key storage provider to install to TPM, if present.

## PARAMETERS

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
Specifies a description for the PFX certificate profile.

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

### -KeyStorageProvider
Specifies the Key Storage Provider.
Valid values are:

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

### -Name
Specifies a name for the PFX certificate profile.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Get-CMCertificateProfilePfx](Get-CMCertificateProfilePfx.md)

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[Set-CMCertificateProfilePfx](Set-CMCertificateProfilePfx.md)
