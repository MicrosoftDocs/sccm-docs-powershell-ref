<<<<<<< HEAD
---
title: Get-CMSoftwareMeteringRule
titleSuffix: Configuration Manager
description: Gets Configuration Manager software metering rules.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
ms.assetid: C12620B8-D0BF-464F-BF90-BB1658ABE0B4
online version: https://go.microsoft.com/fwlink/?linkid=833892
schema: 2.0.0
>>>>>>> master
---

# Get-CMSoftwareMeteringRule

## SYNOPSIS
Gets Configuration Manager software metering rules.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareMeteringRule [-ProductName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareMeteringRule -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareMeteringRule** cmdlet gets one or more software metering rules in Microsoft System Center Configuration Manager.
You can use this cmdlet to get rules to pass to other cmdlets, such as the [Enable-CMSoftwareMeteringRule](Enable-CMSoftwareMeteringRule.md) cmdlet or the [Remove-CMSoftwareMeteringRule](Remove-CMSoftwareMeteringRule.md) cmdlet.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

You can specify rules by ID or by product name.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268432) on TechNet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get rules for a product
```
PS XYZ:\> Get-CMSoftwareMeteringRule -ProductName "Accounting Package"
```

This command gets software metering rules for the product named Accounting Package.

## PARAMETERS

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

### -ProductName
Specifies a name for a product that a rule meters.

```yaml
Type: String
Parameter Sets: SearchByName
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

[Disable-CMSoftwareMeteringRule](Disable-CMSoftwareMeteringRule.md)

[Enable-CMSoftwareMeteringRule](Enable-CMSoftwareMeteringRule.md)

[New-CMSoftwareMeteringRule](New-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](Remove-CMSoftwareMeteringRule.md)

[Set-CMSoftwareMeteringRule](Set-CMSoftwareMeteringRule.md)


