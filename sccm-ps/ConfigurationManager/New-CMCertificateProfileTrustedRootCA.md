---
description: Creates a trusted CA certificate profile.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMCertificateProfileTrustedRootCA
---

# New-CMCertificateProfileTrustedRootCA

## SYNOPSIS
Creates a trusted CA certificate profile.

## SYNTAX

```
New-CMCertificateProfileTrustedRootCA [-Description <String>] [-DestinationStore <CertificateStore>]
 -Name <String> -Path <String> -SupportedPlatform <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCertificateProfileTrustedRootCA** cmdlet creates a trusted certification authority (CA) certificate profile.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a trusted CA certificate profile
```
PS XYZ:\> New-CMCertificateProfileTrustedRootCA -Name "Test01" -Path "\\Server01\ShareFolder\RootCA.cer" -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client")
```

This command creates a trusted CA certificate profile named Test01 from the RootCA.cer certificate for all Windows 10 Client platforms.

### Example 2: Create a trusted CA certificate profile and set the destination store
```
PS XYZ:\> New-CMCertificateProfileTrustedRootCA -Name "Test02" -Path \\Server01\ShareFolder\RootCA.cer -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client") -Description "TestRootCertificate" -DestinationStore SystemIntermediate
```

This command creates a trusted CA certificate profile named Test02 from the RootCA.cer certificate for all Windows 10 Client platforms.
Additionally, the command sets the destination store to Computer certificate store - Intermediate.

## PARAMETERS

### -Description
Specifies a description for the trusted CA certificate profile.

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

### -DestinationStore
Specifies the destination store for the trusted CA certificate.
Valid values are:

- SystemRoot
- SystemIntermediate
- UserIntermediate

```yaml
Type: CertificateStore
Parameter Sets: (All)
Aliases: Store
Accepted values: SystemRoot, SystemIntermediate, UserIntermediate

Required: False
Position: Named
Default value: SystemRoot
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

### -Name
Specifies a name for the trusted CA certificate profile.

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

### -Path
Specifies the path to the trusted CA certificate file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificatePath

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

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMCertificateProfileTrustedRootCA](Get-CMCertificateProfileTrustedRootCA.md)

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[Set-CMCertificateProfileTrustedRootCA](Set-CMCertificateProfileTrustedRootCA.md)
