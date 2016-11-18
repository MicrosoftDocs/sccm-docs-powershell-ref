---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 701C2E53-2F36-40F8-929A-9C6B50E2D815
---

# Merge-CMConflictingRecord

## SYNOPSIS
Merges a new Configuration Manager client record with a conflicting client record.

## SYNTAX

### SearchByValue (Default)
```
Merge-CMConflictingRecord -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Merge-CMConflictingRecord -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByName
```
Merge-CMConflictingRecord -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchBySiteCode
```
Merge-CMConflictingRecord -SiteCode <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Merge-CMConflictingRecord** cmdlet merges a new Microsoft System Center Configuration Manager client record with a conflicting client record that has the same hardware information.

When Configuration Manager recognizes a new client, it uses hardware information to check whether it previously created a record for that computer.
For example, you might have reinstalled the operating system.
The previous client record still exists with the same hardware information.
If you manually resolve conflicts, you have the option to merge the new record with the existing record, create a new record, or create a record as a blocked record.
You can also configure Configuration Manager to resolve conflicts automatically.
For more information, see [Configuring Settings for Client Management in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=269847) on TechNet.

You can specify conflicting records by using a name or ID or you can specify a site code to merge each of the unresolved conflicting records for that site.

## EXAMPLES

### Example 1: Merge conflicting records for a site
```
PS C:\>Merge-CMConflictingRecords -SiteCode "CM2"
```

This command merges each of the conflicting records for the specified System Center Configuration Manager site.

### Example 2: Merge records for a named conflict
```
PS C:\>Merge-CMConflictingRecords -Name "CR07"
```

This command merges the conflicting records named CR07.

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
Parameter Sets: SearchById
Aliases: Smsid

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject


```yaml
Type: IResultObject
Parameter Sets: SearchByValue
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
Parameter Sets: SearchByName
Aliases: AgentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.
This cmdlet merges the conflicting records for this site.

```yaml
Type: String
Parameter Sets: SearchBySiteCode
Aliases: 

Required: True
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

[Block-CMConflictingRecord](./Block-CMConflictingRecord.md)

[Get-CMConflictingRecord](./Get-CMConflictingRecord.md)


