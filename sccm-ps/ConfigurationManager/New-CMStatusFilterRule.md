---
description: Creates a rule in Configuration Manager.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: New-CMStatusFilterRule
---

# New-CMStatusFilterRule

## SYNOPSIS
Creates a rule in Configuration Manager.

## SYNTAX

```
New-CMStatusFilterRule [-AllowDeleteAfterDays <Int32>] [-ComponentName <String>]
 [-ForwardToStatusSummarizer <Boolean>] [-MessageId <Int32>] [-MessageType <MessageType>] -Name <String>
 [-ProcessLowerPriorityRule <Boolean>] [-ProgramPath <String>] [-PropertyId <String>] [-PropertyValue <String>]
 [-ReplicateToParentSite <Boolean>] [-ReplicationPriority <ReplicationPriority>] [-ReportToEventLog <Boolean>]
 [-RunProgram <Boolean>] [-SeverityType <SeverityType>] [-SiteCode <String>] [-SiteSystemServerName <String>]
 [-Source <String>] [-StatusFilterRuleSiteCode <String>] [-WriteToDatabase <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMStatusFilterRule** cmdlet creates a rule that triggers one or more actions that alerts an administrator to a specific message in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a status filter rule

This command creates a status filter rule at the **XYZ** site to detect status message **4611** and write an event in the Windows log.

```powershell
New-CMStatusFilterRule -SiteCode "XYZ" -Name "Detect when the component status summarizer resets the status of a component." -Source "Site Server" -ComponentName "SMS_COMPONENT_STATUS_SUMMARIZER" -MessageId "4611" -ReportToEventLog $True -ReplicateToParentSite $False -RunProgram $False -ForwardToStatusSummarizer $True -ProcessLowerPriorityRule $True
```

## PARAMETERS

### -AllowDeleteAfterDays
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: AllowUserDeleteMessagesAfterThresholdDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComponentName
Specifies the Configuration Manager component that corresponds to the status messages.

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

### -ForwardToStatusSummarizer
Indicates whether to forward to the status summarizer.

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

### -MessageId
Specifies a message ID in Configuration Manager.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MessageType
Specifies a status message type in Configuration Manager.

```yaml
Type: MessageType
Parameter Sets: (All)
Aliases:
Accepted values: None, Milestone, Detail, Audit

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the status filter rule.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessLowerPriorityRule
Indicates whether to process a lower priority rule, which prevents further rule processing.

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

### -ProgramPath
Specifies a path to a program that runs when a status message matches the status filter rule.

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

### -PropertyId
Specifies a property ID in Configuration Manager.

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

### -PropertyValue
Specifies a value for the corresponding *PropertyId* parameter.

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

### -ReplicateToParentSite
Indicates whether to pass a message to the parent site.

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

### -ReplicationPriority
Specifies a replication priority for sending status messages to the parent site.
The acceptable values for this parameter are: High, Low, and Medium.

```yaml
Type: ReplicationPriority
Parameter Sets: (All)
Aliases:
Accepted values: Low, Medium, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportToEventLog
Indicates whether to report an event in the Windows event log.

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

### -RunProgram
Indicates whether to run a program when a status message matches a filter rule.

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

### -SeverityType
Specifies the severity of a status message.

```yaml
Type: SeverityType
Parameter Sets: (All)
Aliases:
Accepted values: None, Informational, Warning, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a Configuration Manager site code that defines the status rule.

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

### -SiteSystemServerName
Specifies a name of the site system server.

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

### -Source
Specifies the status message source to match.

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

### -StatusFilterRuleSiteCode
Specifies a site code for the status filter rule.

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

### -WriteToDatabase
Indicates whether to write a message to the database.
Must be set to enable the *AllowUserDeleteMessagesAfterThresholdDays* parameter.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_SCI_SCPropertyList

## NOTES

## RELATED LINKS

[Disable-CMStatusFilterRule](Disable-CMStatusFilterRule.md)

[Enable-CMStatusFilterRule](Enable-CMStatusFilterRule.md)

[Get-CMStatusFilterRule](Get-CMStatusFilterRule.md)

[Remove-CMStatusFilterRule](Remove-CMStatusFilterRule.md)

[Set-CMStatusFilterRule](Set-CMStatusFilterRule.md)
