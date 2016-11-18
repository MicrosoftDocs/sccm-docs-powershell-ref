---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 8969DC7F-BF22-4F9C-860F-CFC807D696BE
---

# Set-CMSoftwareMeteringSetting

## SYNOPSIS
Configures Configuration Manager software metering properties.

## SYNTAX

```
Set-CMSoftwareMeteringSetting [-DataRetentionDayCount <Int32>] [-AutoCreateDisabledRule <Boolean>]
 [-AutoCreatePercentage <Int32>] [-AutoCreateThreshold <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareMeteringSetting** cmdlet configures software metering properties for Microsoft System Center Configuration Manager.

Software metering can use software inventory information to create software metering rules.
When you select this feature, System Center Configuration Manager identifies multiple computers that use the same software and creates a rule to track that usage.
You decide how long to keep software metering data that System Center Configuration Manager uses to create rules.

To prevent System Center Configuration Manager from creating too many rules, you can specify what percentage of computers use a piece of software before System Center Configuration Manager creates a rule.

You can also set a rule threshold.
If the number of software metering rules exceeds this threshold, System Center Configuration Manager stops automatically creating rules.

When System Center Configuration Manager creates a rule automatically, it creates that rule as disabled.
A disabled rule does not collect information from clients.
You can use the Enable-CMSoftwareMeteringRule cmdlet to enable a rule.
You can use the Remove-CMSoftwareMeteringRule cmdlet to remove unwanted rules.

## EXAMPLES

### Example 1: Disable automatic rule creation
```
PS C:\>Set-CMSoftwareMeteringSetting -AutoCreateDisabledRule $False
```

This command disables automatic rule creation.
System Center Configuration Manager does not automatically create software metering rules after you run this command.

### Example 2: Configure automatic rule creation
```
PS C:\>Set-CMSoftwareMeteringSetting -AutoCreateDisabledRule $True -AutoCreatePercentage 50 -AutoCreateThreshold 200 -DataRetentionDayCount 30
```

This command enables automatic rule creation and sets properties for it.
This command sets the percentage of computers that use a piece of software to 50 percent, the rule threshold to 200, and the amount of time System Center Configuration Manager keeps software metering data to 30 days.

### Example 3: Change automatic rule creation percentage
```
PS C:\>Set-CMSoftwareMeteringSetting -AutoCreatePercentage 20
```

This command changes the percentage of computers that use a piece of software to 20 percent.

## PARAMETERS

### -AutoCreateDisabledRule
Specifies whether Configuration Manager automatically creates software metering rules.
If this value is $True, Configuration Manager automatically creates software metering rules.
If this value is $False, it does not automatically create rules.

When Configuration Manager creates rules, it creates them as disabled.

You can use the values set by other parameters of this cmdlet to limit creation of rules.

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

### -AutoCreatePercentage
Specifies a percentage of computers that use a piece of software for Configuration Manager to create a rule.
Software metering calculates the number of computers as all the computers monitored for software metering by Configuration Manager, not just for a single site.
Valid values are integers from 1 through 99.

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

### -AutoCreateThreshold
Specifies a number of software metering rules as a threshold.
When Configuration Manager exceeds this threshold, it stops automatically creating rules.
The number of rules counted for this threshold includes all software metering rules, not only those that Configuration Manager creates automatically.
Valid values are integers from 1 through 1000.

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

### -DataRetentionDayCount
Specifies the number of days that Configuration Manager keeps software metering data.

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

[Enable-CMSoftwareMeteringRule](./Enable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringSetting](./Get-CMSoftwareMeteringSetting.md)

[Remove-CMSoftwareMeteringRule](./Remove-CMSoftwareMeteringRule.md)


