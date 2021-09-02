---
description: Removes a schedule for updating an operating system image.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Clear-CMOperatingSystemImageUpdateSchedule
---

# Clear-CMOperatingSystemImageUpdateSchedule

## SYNOPSIS
Removes a schedule for updating an operating system image.

## SYNTAX

### SearchByValueMandatory (Default)
```
Clear-CMOperatingSystemImageUpdateSchedule [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Clear-CMOperatingSystemImageUpdateSchedule [-Force] -Id <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Clear-CMOperatingSystemImageUpdateSchedule [-Force] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Clear-CMOperatingSystemImageUpdateSchedule** cmdlet removes a schedule for updating an operating system image from a Configuration Manager site.

Operating system images are .wim format files, which represent a compressed collection of reference files and folders that Configuration Manager requires to successfully install and configure an operating system on a computer.
You can use Configuration Manager to define a schedule for updating these images by using Component Based Servicing (CBS), then delete unwanted schedules by using this cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a schedule for updating an operating system image by using a name
```
PS XYZ:\>Clear-CMOperatingSystemUpdateSchedule -OperatingSystemImageName "Win8UpdateSchedule"
```

This command removes a schedule named Win8UpdateSchedule that updates an operating system image.

### Example 2: Remove a schedule for updating an operating system image by using an object
```
PS XYZ:\> $Win8UpdateSchedule = Get-CMOperatingSystemUpdateSchedule -Id 1207
PS XYZ:\> Clear-CMOperatingSystemImageUpdateSchedule -OperatingSystemImageName "Win8UpdateSchedule"
```

The first command gets the image update schedule by using the ID 1207.
The command stores this schedule in the $UpdateSchedObject variable.

The second command removes the image update schedule by using $UpdateSchedObject.

## PARAMETERS

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
```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: OperatingSystemImageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: OperatingSystemImage, ServicingSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: OperatingSystemImageName

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMOperatingSystemImageUpdateSchedule](Get-CMOperatingSystemImageUpdateSchedule.md)


