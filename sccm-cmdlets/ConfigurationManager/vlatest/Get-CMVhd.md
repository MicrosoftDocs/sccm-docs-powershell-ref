---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834008
schema: 2.0.0
ms.assetid: 19F2832A-607E-4626-B0BC-A8970D87E46C
---

# Get-CMVhd

## SYNOPSIS
Gets VHD images.

## SYNTAX

### SearchByName (Default)
```
Get-CMVhd [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMVhd -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMVhd** cmdlet gets one or more virtual hard disk (VHD) images that were created by using the operating system deployment feature.

## EXAMPLES

### Example 1: Get a VHD image by using its name
```
PS C:\>Get-CMVhd -Name "VHDAccounting08"
```

This command gets the virtual hard disk (VHD) image named VHDAccounting08.

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
Specifies an array of IDs of VHD images.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a VHD image.

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

[New-CMVhd](./New-CMVhd.md)

[Remove-CMVhd](./Remove-CMVhd.md)

[Set-CMVhd](./Set-CMVhd.md)


