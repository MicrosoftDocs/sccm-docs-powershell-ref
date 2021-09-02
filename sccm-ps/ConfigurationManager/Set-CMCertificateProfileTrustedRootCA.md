---
description: Sets a trusted CA certificate profile.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMCertificateProfileTrustedRootCA
---

# Set-CMCertificateProfileTrustedRootCA

## SYNOPSIS
Sets a trusted CA certificate profile.

## SYNTAX

### ByValue (Default)
```
Set-CMCertificateProfileTrustedRootCA [-Description <String>] [-DestinationStore <CertificateStore>]
 -InputObject <IResultObject> [-NewName <String>] [-PassThru] [-Path <String>]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMCertificateProfileTrustedRootCA [-Description <String>] [-DestinationStore <CertificateStore>]
 -Id <Int32> [-NewName <String>] [-PassThru] [-Path <String>] [-SupportedPlatform <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMCertificateProfileTrustedRootCA [-Description <String>] [-DestinationStore <CertificateStore>]
 -Name <String> [-NewName <String>] [-PassThru] [-Path <String>] [-SupportedPlatform <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCertificateProfileTrustedRootCA** cmdlet changes the settings of a trusted CA certificate profile.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a trusted CA certificate profile by using the pipeline
```
PS XYZ:\> Get-CMCertificateProfileTrustedRootCA -Name "Test123" -Fast | Set-CMCertificateProfileTrustedRootCA -Description "Updated description" -WhatIf
```

This command describes what would happen if the command gets the trusted CA certificate profile object named Test123 and uses the pipeline operator to pass the object to **Set-CMCertificateProfileTrustedRootCA** to update its description.
The command does not actually run.

### Example 2: Set a trusted CA certificate profile by ID
```
PS XYZ:\> Set-CMCertificateProfileTrustedRootCA -Id 16777479 -NewName "Test456" -Description "Update" -DestinationStore UserIntermediate -Confirm
```

This command updates the name of the trusted CA certificate profile with the ID of 16777479 to Test456, updates its description, and changes the destination store to UserIntermediate.
By specifying the *Confirm* parameter, the user is prompted for confirmation before the command runs.

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

### -Id
Specifies the ID of a trusted CA certificate profile.

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
Specifies a trusted CA certificate profile object.
To obtain a trusted CA certificate profile object, use the Get-CMCertificateProfileTrustedRootCA function.

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

### -Name
Specifies the name of a trusted CA certificate profile.

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
Specifies a new name for the trusted CA certificate profile.

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

### -Path
Specifies the path to the trusted CA certificate file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificatePath

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

[Get-CMCertificateProfileTrustedRootCA](Get-CMCertificateProfileTrustedRootCA.md)

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[New-CMCertificateProfileTrustedRootCA](New-CMCertificateProfileTrustedRootCA.md)
