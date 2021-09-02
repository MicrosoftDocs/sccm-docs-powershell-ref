---
description: Sets an object representing a status reporting component.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: Set-CMStatusReportingComponent
---

# Set-CMStatusReportingComponent

## SYNOPSIS
Sets an object representing a status reporting component.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMStatusReportingComponent [-ClientLogChecked <Boolean>] [-ClientLogFailureChecked <Boolean>]
 [-ClientLogType <StatusReportOrLogType>] [-ClientReportChecked <Boolean>]
 [-ClientReportFailureChecked <Boolean>] [-ClientReportType <StatusReportOrLogType>]
 -InputObject <IResultObject> [-ServerLogChecked <Boolean>] [-ServerLogFailureChecked <Boolean>]
 [-ServerLogType <StatusReportOrLogType>] [-ServerReportChecked <Boolean>]
 [-ServerReportFailureChecked <Boolean>] [-ServerReportType <StatusReportOrLogType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMStatusReportingComponent [-ClientLogChecked <Boolean>] [-ClientLogFailureChecked <Boolean>]
 [-ClientLogType <StatusReportOrLogType>] [-ClientReportChecked <Boolean>]
 [-ClientReportFailureChecked <Boolean>] [-ClientReportType <StatusReportOrLogType>] -Name <String>
 [-ServerLogChecked <Boolean>] [-ServerLogFailureChecked <Boolean>] [-ServerLogType <StatusReportOrLogType>]
 [-ServerReportChecked <Boolean>] [-ServerReportFailureChecked <Boolean>]
 [-ServerReportType <StatusReportOrLogType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchBySiteCodeMandatory
```
Set-CMStatusReportingComponent [-ClientLogChecked <Boolean>] [-ClientLogFailureChecked <Boolean>]
 [-ClientLogType <StatusReportOrLogType>] [-ClientReportChecked <Boolean>]
 [-ClientReportFailureChecked <Boolean>] [-ClientReportType <StatusReportOrLogType>]
 [-ServerLogChecked <Boolean>] [-ServerLogFailureChecked <Boolean>] [-ServerLogType <StatusReportOrLogType>]
 [-ServerReportChecked <Boolean>] [-ServerReportFailureChecked <Boolean>]
 [-ServerReportType <StatusReportOrLogType>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStatusReportingComponent** cmdlet sets an object that represents a status reporting component.
A status reporting component object specifies information about the client configuration and server configuration components.

You can configure the reporting component to check log files and monitor the severity of entries in the log files.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set status reporting component

This command sets a client report type and a server report type.

```powershell
Set-CMStatusReportingComponent -SiteCode "CM1" -ClientReportType AllMilestones -ServerReportType AllMilestones
```

## PARAMETERS

### -ClientLogChecked
Indicates whether a client log is checked.

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

### -ClientLogFailureChecked
Indicates whether a client log failure is checked.

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

### -ClientLogType
Specifies a type of client log.

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases:
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientReportChecked
Indicates whether a client report is checked.

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

### -ClientReportFailureChecked
Indicates whether a client failure is checked.

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

### -ClientReportType
Specifies a type of report.

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases:
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

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

### -InputObject
Specifies an object output from another cmdlet.

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
Specifies a name for a status reporting component in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerLogChecked
Indicates whether a server log is checked.

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

### -ServerLogFailureChecked
Indicates whether a server log failure is checked.

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

### -ServerLogType
Specifies a server log type.

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases:
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerReportChecked
Indicates whether a server report is checked.

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

### -ServerReportFailureChecked
Indicates whether a server report failure is checked.

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

### -ServerReportType
Specifies a report type.

```yaml
Type: StatusReportOrLogType
Parameter Sets: (All)
Aliases:
Accepted values: AllMilestonesAndAllDetails, AllMilestones, ErrorAndWarningMilestones, ErrorMilestones

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMStatusReportingComponent](Get-CMStatusReportingComponent.md)
