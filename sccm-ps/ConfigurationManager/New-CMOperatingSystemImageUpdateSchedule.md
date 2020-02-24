---
author: aczechowski
description: Creates an operating system image update schedule.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMOperatingSystemImageUpdateSchedule
titleSuffix: Configuration Manager
---

# New-CMOperatingSystemImageUpdateSchedule

## SYNOPSIS
Creates an operating system image update schedule.

## SYNTAX

### NewScheduleByInputObject (Default)
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-RemoveSupersededUpdates <Boolean>]
 [-CustomSchedule <DateTime>] -InputObject <IResultObject> -SoftwareUpdate <IResultObject[]>
 [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByNameRunNow
```
New-CMOperatingSystemImageUpdateSchedule -Name <String> [-ContinueOnError <Boolean>]
 [-RemoveSupersededUpdates <Boolean>] [-RunNow] -SoftwareUpdate <IResultObject[]>
 [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewScheduleByIdRunNow
```
New-CMOperatingSystemImageUpdateSchedule -Id <String> [-ContinueOnError <Boolean>]
 [-RemoveSupersededUpdates <Boolean>] [-RunNow] -SoftwareUpdate <IResultObject[]>
 [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewScheduleByName
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-RemoveSupersededUpdates <Boolean>]
 [-CustomSchedule <DateTime>] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleById
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-RemoveSupersededUpdates <Boolean>]
 [-CustomSchedule <DateTime>] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByScheduleInputObject
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-RemoveSupersededUpdates <Boolean>]
 [-CustomSchedule <DateTime>] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByInputObjectRunNow
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-RemoveSupersededUpdates <Boolean>]
 -InputObject <IResultObject> [-RunNow] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByScheduleInputObjectRunNow
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-RemoveSupersededUpdates <Boolean>]
 [-RunNow] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMOperatingSystemImageUpdateSchedule** cmdlet creates an operating system image update schedule.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create an operating system image update schedule
```
PS ABC:\> $Win10Image = Get-CMOperatingSystemImage -Name "Windows 10 Enterprise"
PS ABC:\> $Win10SU = Get-CMSoftwareUpdate -UpdateGroupName "Win10SUgroup01"
PS ABC:\> New-CMOperatingSystemImageUpdateSchedule -Name $Win10Image.Name -SoftwareUpdate $Win10SU -RunNow -ContinueOnError $True
```

The first command gets the operating system image object named Windows 10 Enterprise and stores the object in the $Win10Image variable.

The second command gets the software update object for the update group named Win10SUgroup01 and stores the object in the $Win10SU variable.

The last command creates an operating system image update schedule to update the operating system image named Windows 10 Enterprise with the update stored in $Win10SU.
The update will run now, and will continue to apply the updates even if an error is encountered.

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

### -ContinueOnError
Indicates whether software updates should be applied to the image even when there is an error.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomSchedule
Specifies the date and time when the software updates are applied to the operating system image.

```yaml
Type: DateTime
Parameter Sets: NewScheduleByInputObject, NewScheduleByName, NewScheduleById, NewScheduleByScheduleInputObject
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
Specifies the ID of an operating system image.

```yaml
Type: String
Parameter Sets: NewScheduleByIdRunNow
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an operating system image object.
To obtain an operating system image object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: NewScheduleByInputObject, NewScheduleByInputObjectRunNow
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
Parameter Sets: NewScheduleByNameRunNow
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSupersededUpdates
{{ Fill RemoveSupersededUpdates Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CleanUp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunNow
Indicates that the update should run now.

```yaml
Type: SwitchParameter
Parameter Sets: NewScheduleByNameRunNow, NewScheduleByIdRunNow, NewScheduleByInputObjectRunNow, NewScheduleByScheduleInputObjectRunNow
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdate
Specifies an array of software update objects.
To obtain a software update object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateDistributionPoint
Indicates whether the operating system image on distribution points is updated after the software updates are applied.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: UpdateDistributionPointsWithImage, UpdateDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Utc
Indicates whether to use UTC time.

```yaml
Type: Boolean
Parameter Sets: NewScheduleByInputObject, NewScheduleByName, NewScheduleById, NewScheduleByScheduleInputObject
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMOperatingSystemImageUpdateSchedule](Get-CMOperatingSystemImageUpdateSchedule.md)

[Clear-CMOperatingSystemImageUpdateSchedule](Clear-CMOperatingSystemImageUpdateSchedule.md)
