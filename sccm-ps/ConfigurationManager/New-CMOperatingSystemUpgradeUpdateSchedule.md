---
title: New-CMOperatingSystemUpgradeUpdateSchedule
titleSuffix: Configuration Manager
description: Creates an operating system upgrade update schedule.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMOperatingSystemUpgradeUpdateSchedule

## SYNOPSIS
Creates an operating system upgrade update schedule.

## SYNTAX

### NewScheduleByInputObject (Default)
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -InputObject <IResultObject> -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByNameRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule -Name <String> [-ContinueOnError <Boolean>] [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByIdRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule -Id <String> [-ContinueOnError <Boolean>] [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByName
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleById
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByScheduleInputObject
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByInputObjectRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] -InputObject <IResultObject> [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByScheduleInputObjectRunNow
```
New-CMOperatingSystemUpgradeUpdateSchedule [-ContinueOnError <Boolean>] [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
```

 

## PARAMETERS

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

### -RunNow
 

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_ImageServicingSchedule

## NOTES

## RELATED LINKS

