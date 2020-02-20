---
author: aczechowski
description: Disables Configuration Manager software metering rules.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/01/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Disable-CMSoftwareMeteringRule
titleSuffix: Configuration Manager
---

# Disable-CMSoftwareMeteringRule

## SYNOPSIS
Disables Configuration Manager software metering rules.

## SYNTAX

### SearchByIdMandatory (Default)
```
Disable-CMSoftwareMeteringRule -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Disable-CMSoftwareMeteringRule -ProductName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Disable-CMSoftwareMeteringRule -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMSoftwareMeteringRule** cmdlet disables one or more software metering rules in Microsoft System Center Configuration Manager.
If you disable a rule, it does not collect information from clients.
You can use the [Enable-CMSoftwareMeteringRule](Enable-CMSoftwareMeteringRule.md) cmdlet to enable a rule that you previously disabled.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

You can specify rules that disable software metering rules by ID or by product name, or use the [Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md) cmdlet.
You can use the Remove-CMSoftwareMeteringRule to permanently delete a rule.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268432) on TechNet.

## EXAMPLES

### Example 1: Disable rules for a specific product
```
PS XYZ:\>Disable-CMSoftwareMeteringRule -ProductName "Accounting Package"
```

This command disables software metering rules for the product named Accounting Package.
There may be more than one rule.

### Example 2: Disable a specific rule
```
PS XYZ:\>Disable-CMSoftwareMeteringRule -Id "16777229"
```

This command disables a software metering rule that has the specified ID.

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
To obtain a software metering rule object, use the [Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md) cmdlet.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Enable-CMSoftwareMeteringRule](Enable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md)

[New-CMSoftwareMeteringRule](New-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](Remove-CMSoftwareMeteringRule.md)

[Set-CMSoftwareMeteringRule](Set-CMSoftwareMeteringRule.md)


