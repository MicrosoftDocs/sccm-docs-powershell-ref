---
description: Gets a Configuration Manager task sequence group.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: Get-CMTaskSequenceGroup
---

# Get-CMTaskSequenceGroup

## SYNOPSIS

Gets a Configuration Manager task sequence group.

## SYNTAX

### ByValue (Default)
```
Get-CMTaskSequenceGroup -InputObject <IResultObject> [-StepName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMTaskSequenceGroup -TaskSequenceId <String> [-StepName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMTaskSequenceGroup -TaskSequenceName <String> [-StepName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMTaskSequenceGroup** gets task sequence group(s) in a task sequence. The cmdlet supports pipeline from a task sequence object, and could be filtered by the name of the group.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> $ReferencedTaskSequence | Get-CMTaskSequenceGroup -StepName $gpName
```

The command gets the task sequence groups in a task sequence with name specified.

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

### -InputObject

Specifies a task sequence object.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StepName

Specifies the name of a step.

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

### -TaskSequenceId

Specifies the ID of a task sequence.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specifies the name of a task sequence.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_TaskSequence_Group

### IResultObject#SMS_TaskSequence_Group

## NOTES

## RELATED LINKS

[New-CMTaskSequenceGroup](./New-CMTaskSequenceGroup.md)

[Set-CMTaskSequenceGroup](./Set-CMTaskSequenceGroup.md)

[Remove-CMTaskSequenceGroup](./Remove-CMTaskSequenceGroup.md)
