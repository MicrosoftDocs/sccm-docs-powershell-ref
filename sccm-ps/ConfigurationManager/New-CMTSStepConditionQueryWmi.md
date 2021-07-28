---
description: Create a WMI query condition for a task sequence step
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 10/28/2020
schema: 2.0.0
title: New-CMTSStepConditionQueryWmi
---

# New-CMTSStepConditionQueryWmi

## SYNOPSIS
Create a WMI query condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionQueryWmi [-Namespace <String[]>] -Query <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Use this cmdlet to create a WMI query condition for a task sequence step.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a query condition based on hardware model

```powershell
$Model = "Latitude E7470"
$ConditionQuery = "Select * From Win32_ComputerSystem Where Model = `"$Model`""
$StepCondition = New-CMTSStepConditionQueryWMI -Namespace "root\cimv2" -Query $ConditionQuery
```

## PARAMETERS

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

### -Namespace
Specify the WMI namespace for the query.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Query
Specify the WMI query.

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### IResultObject#SMS_TaskSequence_WMIConditionExpression
## NOTES

## RELATED LINKS

[Get-CMTSStepConditionQueryWmi](Get-CMTSStepConditionQueryWmi.md)
[New-CMTSStepConditionFile](New-CMTSStepConditionFile.md)
[New-CMTSStepConditionFolder](New-CMTSStepConditionFolder.md)
[New-CMTSStepConditionIfStatement](New-CMTSStepConditionIfStatement.md)
[New-CMTSStepConditionOperatingSystem](New-CMTSStepConditionOperatingSystem.md)
[New-CMTSStepConditionOperatingSystemLanguage](New-CMTSStepConditionOperatingSystemLanguage.md)
[New-CMTSStepConditionRegistry](New-CMTSStepConditionRegistry.md)
[New-CMTSStepConditionSoftware](New-CMTSStepConditionSoftware.md)
[New-CMTSStepConditionVariable](New-CMTSStepConditionVariable.md)
