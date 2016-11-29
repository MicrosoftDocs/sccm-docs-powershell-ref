---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833709
schema: 2.0.0
ms.assetid: DB311582-AD04-42ED-8330-6693CF3AADDB
---

# New-CMOperatingSystemImageUpdateSchedule

## SYNOPSIS

## SYNTAX

### NewScheduleByInputObject (Default)
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -InputObject <IResultObject> -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>]
 [-Utc <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByNameRunNow
```
New-CMOperatingSystemImageUpdateSchedule -Name <String> [-ContinueOnError <Boolean>] [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByIdRunNow
```
New-CMOperatingSystemImageUpdateSchedule -Id <String> [-ContinueOnError <Boolean>] [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleById
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByScheduleInputObject
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByName
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-CustomSchedule <DateTime>]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-Utc <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByInputObjectRunNow
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] -InputObject <IResultObject> [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewScheduleByScheduleInputObjectRunNow
```
New-CMOperatingSystemImageUpdateSchedule [-ContinueOnError <Boolean>] [-RunNow]
 -SoftwareUpdate <IResultObject[]> [-UpdateDistributionPoint <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
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
Default value: False
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
Parameter Sets: NewScheduleByInputObject, NewScheduleById, NewScheduleByScheduleInputObject, NewScheduleByName
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
Parameter Sets: NewScheduleByInputObject, NewScheduleById, NewScheduleByScheduleInputObject, NewScheduleByName
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


