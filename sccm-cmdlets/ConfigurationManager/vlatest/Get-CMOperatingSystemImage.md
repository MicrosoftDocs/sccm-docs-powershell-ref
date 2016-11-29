---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833789
schema: 2.0.0
ms.assetid: B1F3E321-B9DE-4E3D-8EC7-1E023B36998F
---

# Get-CMOperatingSystemImage

## SYNOPSIS
Gets operating system images.

## SYNTAX

### SearchByName (Default)
```
Get-CMOperatingSystemImage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMOperatingSystemImage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOperatingSystemImage** cmdlet gets one or more operating system images on a Microsoft System Center Configuration Manager site.
Operating system images are .wim format files and represent a compressed collection of reference files and folders that System Center Configuration Manager requires to successfully install and configure an operating system on a computer.

## EXAMPLES

### Example 1: Get an operating system image
```
PS C:\>Get-CMOperatingSystemImage -Name "OSImagePkg01" -SecuredScopeNames "SecScope02"
```

This command gets the operating system image named OSImagePkg01 for the security scope named SecScope02.

## PARAMETERS

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

### -Id
Specifies an array of IDs of operating system images.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of an operating system image.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMOperatingSystemImage](./New-CMOperatingSystemImage.md)

[Set-CMOperatingSystemImage](./Set-CMOperatingSystemImage.md)

[Remove-CMOperatingSystemImage](./Remove-CMOperatingSystemImage.md)

[Get-CMOperatingSystemImageUpdateSchedule](./Get-CMOperatingSystemImageUpdateSchedule.md)


