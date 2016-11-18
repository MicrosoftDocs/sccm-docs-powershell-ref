---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 3911D73C-E269-4160-8667-732DAFD7AB48
---

# Set-CMStatusFilterRule

## SYNOPSIS
Modifies settings for a Configuration Manager filter rule for status messages.

## SYNTAX

```
Set-CMStatusFilterRule [-SiteCode <String>] -Name <String> [-Priority <PriorityChangeType>] [-Source <String>]
 [-StatusFilterRuleSiteCode <String>] [-SiteSystemServerName <String>] [-ComponentName <String>]
 [-MessageType <MessageType>] [-SeverityType <SeverityType>] [-MessageId <Int32>] [-PropertyId <String>]
 [-PropertyValue <String>] [-WriteToDatabase <Boolean>] [-AllowDeleteAfterDays <Int32>]
 [-ReportToEventLog <Boolean>] [-ReplicateToParentSite <Boolean>] [-ReplicationPriority <ReplicationPriority>]
 [-RunProgram <Boolean>] [-ProgramPath <String>] [-ForwardToStatusSummarizer <Boolean>]
 [-ProcessLowerPriorityRule <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStatusFilterRule** cmdlet modifies settings for a Microsoft System Center Configuration Manager filter rule for status messages.
System Center Configuration Manager checks a status message against rules in order of priority.
A rule can specify that rules with lower priority do not apply to a message after that rule applied.

Status filter rules specify how System Center Configuration Manager responds to status messages.
Each filter rule contains criteria and actions for status messages.
You configure status filter rules for each site, not across all sites.

To change the priority of a rule, use the rule name to specify the rule.

## EXAMPLES

### Example 1: Increase the priority of a rule
```
PS C:\>Set-CMStatusFilterRule -Name "Status change to critical" -SiteCode "CM1" -Priority Increase
```

This command increases the priority of a filter rule that has the specified name in a site that has the site code CM1.

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

### -ForwardToStatusSummarizer


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

### -Priority


```yaml
Type: PriorityChangeType
Parameter Sets: (All)
Aliases: 
Accepted values: Increase, Decrease

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProcessLowerPriorityRule


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


```yaml
Type: ReplicationPriority
Parameter Sets: (All)
Aliases: 
Accepted values: High, Medium, Low

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportToEventLog


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

### -WriteToDatabase


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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMStatusFilterRule](./Disable-CMStatusFilterRule.md)

[Enable-CMStatusFilterRule](./Enable-CMStatusFilterRule.md)

[Get-CMStatusFilterRule](./Get-CMStatusFilterRule.md)

[New-CMStatusFilterRule](./New-CMStatusFilterRule.md)

[Remove-CMStatusFilterRule](./Remove-CMStatusFilterRule.md)


