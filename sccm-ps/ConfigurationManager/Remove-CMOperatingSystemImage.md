---
description: Removes operating system images.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMOperatingSystemImage
---

# Remove-CMOperatingSystemImage

## SYNOPSIS
Removes operating system images.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMOperatingSystemImage [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMOperatingSystemImage [-Force] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMOperatingSystemImage [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMOperatingSystemImage** cmdlet removes one or more operating system images from a Configuration Manager site.
Operating system images are .wim format files and represent a compressed collection of reference files and folders that Configuration Manager requires to successfully install and configure an operating system on a computer.

After you remove an operating system image, you cannot distribute the operating system image to distribution points.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove an operating system image
```
PS XYZ:\> Remove-CMOperatingSystemImage -Name "STANDARD_WIN7"
```

This command removes the operating system image named STANDARD_WIN7.

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

### -Force
Forces the command to run without asking for user confirmation.

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

### -InputObject
Specifies a **CMOperatingSystemImage** object.
To obtain a **CMOperatingSystemImage** object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of an operating system image.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
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

### System.Object
## NOTES

## RELATED LINKS

[Set-CMOperatingSystemImage](Set-CMOperatingSystemImage.md)

[New-CMOperatingSystemImage](New-CMOperatingSystemImage.md)

[Get-CMOperatingSystemImageUpdateSchedule](Get-CMOperatingSystemImageUpdateSchedule.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)


