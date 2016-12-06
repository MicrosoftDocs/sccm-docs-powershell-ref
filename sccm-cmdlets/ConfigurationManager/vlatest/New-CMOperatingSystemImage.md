---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833705
schema: 2.0.0
ms.assetid: E6AB814A-E29E-4DBB-AABF-63DF1F129E80
---

# New-CMOperatingSystemImage

## SYNOPSIS
Creates an operating system image.

## SYNTAX

```
New-CMOperatingSystemImage -Name <String> -Path <String> [-Version <String>] [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMOperatingSystemImage** cmdlet adds an operating system image to a Microsoft System Center Configuration Manager site.
Operating system images are .wim format files and represent a compressed collection of reference files and folders that are System Center Configuration Manager requires to successfully install and configure an operating system on a computer.

## EXAMPLES

### Example 1: Create an operating system image
```
PS C:\>New-CMOperatingSystemImage -Name "STANDARD_WIN7" -Path "\\Contoso01\CM\Images\STANDARD_WIN7.wim"
```

This command creates the operating system image named STANDARD_WIN7 and specifies the network path to the installation source files of the operating system image.

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
Specifies a description for the operating system image.

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

### -Name
Specifies the name of an operating system image.

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
Specifies the network path to the installation source files of an operating system image source .wim file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies a version of the operating system image.

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

[Get-CMOperatingSystemImage](./Get-CMOperatingSystemImage.md)

[Set-CMOperatingSystemImage](./Set-CMOperatingSystemImage.md)

[Remove-CMOperatingSystemImage](./Remove-CMOperatingSystemImage.md)

[Get-CMOperatingSystemImageUpdateSchedule](./Get-CMOperatingSystemImageUpdateSchedule.md)


