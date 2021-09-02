---
description: Modifies settings of a Configuration Manager status summarizer.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMStatusSummarizer
---

# Set-CMStatusSummarizer

## SYNOPSIS
Modifies settings of a Configuration Manager status summarizer.

## SYNTAX

### SetComponentStatusSummarizer (Default)
```
Set-CMStatusSummarizer [-ComponentStatusSummarizer] [-EnableStatusSummarizer <Boolean>] [-PassThru]
 [-ReplicateToParentSite <Boolean>] [-ReplicationPriority <ReplicationPriorityType>] [-SiteCode <String>]
 [-TimeThreshold <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetAppDeploymentSummarizer
```
Set-CMStatusSummarizer [-ApplicationDeploymentSummarizer] [-Days <Int32>] [-Hours <Int32>] [-Minutes <Int32>]
 [-PassThru] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetAppStatisticsSummarizer
```
Set-CMStatusSummarizer [-ApplicationStatisticSummarizer] [-Days <Int32>] [-Hours <Int32>] [-Minutes <Int32>]
 [-PassThru] [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetSiteSystemStatusSummarizer
```
Set-CMStatusSummarizer [-CriticalSizeKB <Int32>] [-EnableStatusSummarizer <Boolean>] [-PassThru]
 [-ReplicateToParentSite <Boolean>] [-ReplicationPriority <ReplicationPriorityType>]
 [-Schedule <IResultObject>] [-SiteCode <String>] [-SiteSystemStatusSummarizer] [-WarningSizeKB <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStatusSummarizer** cmdlet modifies settings of a status summarizer.
The Configuration Manager status summarizers apply to the areas of application deployment, application statistics, component status, and site system status.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a status summarizer
```
PS XYZ:\> Set-CMStatusSummarizer -ApplicationDeploymentSummarizer -SiteCode "ContosoSite"
```

This command configures the status summarizer for the Contoso site to return application deployment statistics.

## PARAMETERS

### -ApplicationDeploymentSummarizer
Indicates that the summarizer is an application deployment status summarizer.

```yaml
Type: SwitchParameter
Parameter Sets: SetAppDeploymentSummarizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationStatisticSummarizer
Indicates that the summarizer is an application statistic status summarizer.

```yaml
Type: SwitchParameter
Parameter Sets: SetAppStatisticsSummarizer
Aliases: ApplicationStatisticsSummarizer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComponentStatusSummarizer
Indicates that the summarizer is a component status summarizer.

```yaml
Type: SwitchParameter
Parameter Sets: SetComponentStatusSummarizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CriticalSizeKB
Specifies the threshold, in kilobytes, of free space for a Critical message.
This parameter applies to site system status summarizers.

```yaml
Type: Int32
Parameter Sets: SetSiteSystemStatusSummarizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Days
```yaml
Type: Int32
Parameter Sets: SetAppDeploymentSummarizer, SetAppStatisticsSummarizer
Aliases: DayInterval

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

### -EnableStatusSummarizer
Indicates whether to enable Configuration Manager to summarize status messages for the site.
This parameter applies to component status summarizers and site system status summarizers.

```yaml
Type: Boolean
Parameter Sets: SetComponentStatusSummarizer, SetSiteSystemStatusSummarizer
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

### -Hours
```yaml
Type: Int32
Parameter Sets: SetAppDeploymentSummarizer, SetAppStatisticsSummarizer
Aliases: HourInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Minutes
```yaml
Type: Int32
Parameter Sets: SetAppDeploymentSummarizer, SetAppStatisticsSummarizer
Aliases: MinuteInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -ReplicateToParentSite
Indicates whether to pass summarization data from this site to its parent site.
This parameter applies to component status summarizers and site system status summarizers.
If you specify a value of $True for this parameter, specify a priority by using the *ReplicationPriority* parameter and a threshold period by using the *ThresholdPeriod* parameter.

```yaml
Type: Boolean
Parameter Sets: SetComponentStatusSummarizer, SetSiteSystemStatusSummarizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationPriority
Specifies the priority of replication to the parent site.
The acceptable values for this parameter are: Low, Normal, and High.
Specify this parameter if you specify $True for the *ReplicateToParentSite* parameter.

```yaml
Type: ReplicationPriorityType
Parameter Sets: SetComponentStatusSummarizer, SetSiteSystemStatusSummarizer
Aliases:
Accepted values: Low, Normal, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a schedule object that determines how often to summarize site system status.
To obtain a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetSiteSystemStatusSummarizer
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

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

### -SiteSystemStatusSummarizer
Indicates that the summarizer is a site system status summarizer.

```yaml
Type: SwitchParameter
Parameter Sets: SetSiteSystemStatusSummarizer
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeThreshold
```yaml
Type: String
Parameter Sets: SetComponentStatusSummarizer
Aliases: ThresholdPeriod
Accepted values: Since 0:00:00, Since 4:00:00, Since 8:00:00, Since 12:00:00, Since 16:00:00, Since 20:00:00, Since Sunday, Since Monday, Since Tuesday, Since Wednesday, Since Thursday, Since Friday, Since Saturday, Since 15th of the Month, Since 1st of the Month, Since Site Installation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WarningSizeKB
Specifies the threshold, in kilobytes, of free space for a Warning message.
This parameter applies to site system status summarizers.

```yaml
Type: Int32
Parameter Sets: SetSiteSystemStatusSummarizer
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

## NOTES

## RELATED LINKS

[New-CMSchedule](New-CMSchedule.md)

[Get-CMStatusSummarizer](Get-CMStatusSummarizer.md)
