---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: 5B61CB9F-A632-4D14-B6EA-F6BA25BDD0A1
online version: https://go.microsoft.com/fwlink/?linkid=833693
schema: 2.0.0
---

# Set-CMCertificateProfilePfx

## SYNOPSIS
Sets a PFX certificate profile.

## SYNTAX

### ByValue (Default)
```
Set-CMCertificateProfilePfx [-Description <String>] -InputObject <IResultObject>
 [-KeyStorageProvider <KeyStorageProviderSettingType>] [-NewName <String>] [-PassThru]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMCertificateProfilePfx [-Description <String>] -Id <Int32>
 [-KeyStorageProvider <KeyStorageProviderSettingType>] [-NewName <String>] [-PassThru]
 [-SupportedPlatform <IResultObject[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMCertificateProfilePfx [-Description <String>] [-KeyStorageProvider <KeyStorageProviderSettingType>]
 -Name <String> [-NewName <String>] [-PassThru] [-SupportedPlatform <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCertificateProfilePfx** cmdlet changes the settings of a PFX certificate profile.

## EXAMPLES

### Example 1: Set a PFX certificate profile by name
```
PS C:\> Set-CMCertificateProfilePfx -Name "TestUpdate1" -Description "Update name to Test" -NewName "Test" -SupportedPlatform (Get-CMSupportedPlatform -Fast -Name "All Windows 10*Client")
```

This command updates the name of the PFX certificate profile named TestUpdate1 to Test for all Windows 10 Client platforms.

### Example 2: Set a PFX certificate profile by ID
```
PS C:\> Set-CMCertificateProfilePfx -Id 16777453 -Description "Updated" -KeyStorageProvider InstallToSoftwareKeyStorageProvider -NewName "Test2"
```

This command updates the name of the PFX certificate profile with the ID 16777453 to Test2 and sets the key storage provider to install to Software Key Storage Provider.

### Example 3: Set a PFX certificate profile by using the pipeline
```
PS C:\> Get-CMCertificateprofilePfx -Name "Test3" | Set-CMCertificateprofilePfx -Description "Updated"
```

This command gets the PFX certificate profile object named Test3 and uses the pipeline operator to pass the object to **Set-CMCertificateProfilePfx**, which updates the description of the object.

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

### -Id
Specifies the ID of a PFX certificate profile.

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
Specifies a PFX certificate profile object.
To obtain a PFX certificate profile object, use the Get-CMCertificateProfilePfx function.

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a PFX certificate profile.

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
Specifies a new name for the PFX certificate profile.

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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

[Get-CMCertificateProfilePfx](Get-CMCertificateProfilePfx.md)

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[New-CMCertificateProfilePfx](New-CMCertificateProfilePfx.md)


