---
description: Modifies the Asset Intelligence hardware inventory reporting classes.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMAssetIntelligenceClass
---

# Set-CMAssetIntelligenceClass

## SYNOPSIS
Modifies the Asset Intelligence hardware inventory reporting classes.

## SYNTAX

### SetByAllReportClass (Default)
```
Set-CMAssetIntelligenceClass [-EnableAllReportingClass] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetBySelectReportClass
```
Set-CMAssetIntelligenceClass [-DisableReportingClass <ClassNameType[]>]
 [-EnableReportingClass <ClassNameType[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAssetIntelligenceClass** cmdlet modifies the Asset Intelligence hardware inventory reporting classes.
The Hardware Inventory Client Agent collects inventory from Configuration Manager clients based on the Asset Intelligence hardware inventory reporting classes that you enable.

You can modify the categorization information, which includes product name, vendor, software category, and software family, for inventoried software only at the top-level site in your hierarchy.
After you modify the categorization information for predefined software, the validation state for the software changes from Validated to User Defined.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the Asset Intelligence hardware inventory reporting classes
```
PS XYZ:\> Set-CMAssetIntelligenceClass -EnableReportingClassName SMS_InstalledExecutable -DisableReportingClassName MS_InstalledSoftware
```

This command enables the reporting class named SMS_InstalledExecutable and disables the reporting class named MS_InstalledSoftware.

### Example 2: Enable all Asset Intelligence hardware inventory reporting classes
```
PS XYZ:\> Set-CMAssetIntelligenceClass -EnableAllReportingClass
```

This command enables all the Asset Intelligence hardware inventory reporting classes.

## PARAMETERS

### -DisableReportingClass
Specifies an array of Asset Intelligence reporting classes to disable.
The acceptable values for this parameter are:

- SMS_AutoStartSoftware
- SMS_BrowserHelperObject
- SMS_InstalledExecutable
- SMS_InstalledSoftware
- SMS_SoftwareShortcut
- SMS_SoftwareTag
- SMS_SystemConsoleUsage
- SMS_SystemConsoleUser
- SoftwareLicensingProduct
- SoftwareLicensingService
- Win32_USBDevice

```yaml
Type: ClassNameType[]
Parameter Sets: SetBySelectReportClass
Aliases:
Accepted values: SMS_AutoStartSoftware, SMS_BrowserHelperObject, SMS_InstalledExecutable, SMS_InstalledSoftware, SMS_SoftwareShortcut, SMS_SystemConsoleUsage, SMS_SystemConsoleUser, SoftwareLicensingProduct, SoftwareLicensingService, Win32_USBDevice, SMS_SoftwareTag

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

### -EnableAllReportingClass
Indicates that all Asset Intelligence reporting classes are enabled.

```yaml
Type: SwitchParameter
Parameter Sets: SetByAllReportClass
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableReportingClass
Specifies an array of Asset Intelligence reporting classes to enable.
The acceptable values for this parameter are:

- SMS_AutoStartSoftware
- SMS_BrowserHelperObject
- SMS_InstalledExecutable
- SMS_InstalledSoftware
- SMS_SoftwareShortcut
- SMS_SoftwareTag
- SMS_SystemConsoleUsage
- SMS_SystemConsoleUser
- SoftwareLicensingProduct
- SoftwareLicensingService
- Win32_USBDevice

```yaml
Type: ClassNameType[]
Parameter Sets: SetBySelectReportClass
Aliases:
Accepted values: SMS_AutoStartSoftware, SMS_BrowserHelperObject, SMS_InstalledExecutable, SMS_InstalledSoftware, SMS_SoftwareShortcut, SMS_SystemConsoleUsage, SMS_SystemConsoleUser, SoftwareLicensingProduct, SoftwareLicensingService, Win32_USBDevice, SMS_SoftwareTag

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

[Send-CMAssetIntelligenceCatalogUpdateRequest](Send-CMAssetIntelligenceCatalogUpdateRequest.md)

[Sync-CMAssetIntelligenceCatalog](Sync-CMAssetIntelligenceCatalog.md)


