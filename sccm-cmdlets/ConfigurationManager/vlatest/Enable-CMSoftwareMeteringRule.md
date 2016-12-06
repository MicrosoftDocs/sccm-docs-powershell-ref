---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833991
schema: 2.0.0
ms.assetid: BE43AAAD-ABF9-42DD-886C-D3224AAAB175
---

# Enable-CMSoftwareMeteringRule

## SYNOPSIS
Enables Configuration Manager software metering rules.

## SYNTAX

### SearchByIdMandatory (Default)
```
Enable-CMSoftwareMeteringRule -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Enable-CMSoftwareMeteringRule -ProductName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Enable-CMSoftwareMeteringRule -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Enable-CMSoftwareMeteringRule** cmdlet enables one or more software metering rules in Microsoft System Center Configuration Manager.
You can enable a rule that you previously disabled by using the Disable-CMSoftwareMeteringRule cmdlet.
When System Center Configuration Manager automatically creates software metering rules, it creates them as disabled.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

You can specify rules that enable software metering rules by ID or by product name, or by using the Get-CMSoftwareMeteringRule cmdlet.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268432) on TechNet.

## EXAMPLES

### Example 1: Enable rules for a specific product
```
PS C:\>Enable-CMSoftwareMeteringRule -ProductName "Accounting Package"
```

This command enables software metering rules for a product named Accounting Package.
There may be more than one rule.
If you previously disabled some rules for this product, but not all, the cmdlet does not inform you that some rules were already enabled.

### Example 2: Enable a specific rule
```
PS C:\>Enable-CMSoftwareMeteringRule -Id "16777229"
```

This command enables a software metering rule that has the specified ID.

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
Specifies an array of IDs for software metering rules.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: RuleId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software metering rule object.
To obtain a software metering rule object, use the Get-CMSoftwareMeteringRule cmdlet.

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

### -ProductName
Specifies a name for a product that a rule meters.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

[Disable-CMSoftwareMeteringRule](./Disable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringRule](./Get-CMSoftwareMeteringRule.md)

[New-CMSoftwareMeteringRule](./New-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](./Remove-CMSoftwareMeteringRule.md)

[Set-CMSoftwareMeteringRule](./Set-CMSoftwareMeteringRule.md)


