---
description: Creates an operating system upgrade update schedule.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMOperatingSystemUpgradeUpdateSchedule
---

# New-CMOperatingSystemUpgradeUpdateSchedule

## SYNOPSIS
Creates an operating system upgrade update schedule.

## SYNTAX

### NewScheduleByInputObject (Default)
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -InputObject <IResultObject> [-RemoveSupersededUpdates <Boolean>] -SoftwareUpdate <IResultObject[]>
 [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByName
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 [-RemoveSupersededUpdates <Boolean>] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleById
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 [-RemoveSupersededUpdates <Boolean>] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByScheduleInputObject
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 [-RemoveSupersededUpdates <Boolean>] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByIdRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] -Id <String>
 [-RemoveSupersededUpdates <Boolean>] [-RunNow] -SoftwareUpdate <IResultObject[]>
 [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewScheduleByInputObjectRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] -InputObject <IResultObject>
 [-RemoveSupersededUpdates <Boolean>] [-RunNow] -SoftwareUpdate <IResultObject[]>
 [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewScheduleByNameRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] -Name <String>
 [-RemoveSupersededUpdates <Boolean>] [-RunNow] -SoftwareUpdate <IResultObject[]>
 [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewScheduleByScheduleInputObjectRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-RemoveSupersededUpdates <Boolean>]
 [-RunNow] -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -ContinueOnError
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
```yaml
Type: SwitchParameter
Parameter Sets: NewScheduleByIdRunNow, NewScheduleByInputObjectRunNow, NewScheduleByNameRunNow, NewScheduleByScheduleInputObjectRunNow
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdate
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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_ImageServicingSchedule
## NOTES

## RELATED LINKS
