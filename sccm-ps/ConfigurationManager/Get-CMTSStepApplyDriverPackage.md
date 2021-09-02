---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# Get-CMTSStepApplyDriverPackage

## SYNOPSIS

Get the **Apply Driver Package** step from a specific task sequence.

## SYNTAX

### ByValue (Default)
```
Get-CMTSStepApplyDriverPackage [-InputObject] <IResultObject> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Get-CMTSStepApplyDriverPackage [-TaskSequenceId] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Get-CMTSStepApplyDriverPackage [-TaskSequenceName] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a task sequence step object for one or more instances of the **Apply Driver Package** step. You can use this object to:

- Remove the step from a task sequence with [Remove-CMTSStepApplyDriverPackage](Remove-CMTSStepApplyDriverPackage.md)
- Copy the step to another task sequence with [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md)

For more information on this step, see [About task sequence steps: Apply Driver Package](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyDriverPackage).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets a task sequence object in the **$tsOsd** variable. It then passes that variable as the input object to get the **Apply Driver Package** step.

```powershell
$tsName = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsName -Fast

$tsStepNameApplyDvrPkg = "Apply driver package"
$tsStepApplyDvrPkg = Get-CMTSStepApplyDriverPackage -InputObject $tsOsd -StepName $tsStepNameApplyDvrPkg
```

## PARAMETERS

### -InputObject

Specify a task sequence object from which to get the **Apply Driver Package** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: TaskSequence

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StepName

Specify the name of the **Apply Driver Package** step to get from the task sequence.

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

Specify the **package ID** of the task sequence from which to get the **Apply Driver Package** step. This value is a standard package ID, for example `XYZ00858`.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id, TaskSequencePackageId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify the name of the task sequence from which to get the **Apply Driver Package** step.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[New-CMTSStepApplyDriverPackage](New-CMTSStepApplyDriverPackage.md)
[Remove-CMTSStepApplyDriverPackage](Remove-CMTSStepApplyDriverPackage.md)
[Set-CMTSStepApplyDriverPackage](Set-CMTSStepApplyDriverPackage.md)

[Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md)
[Get-CMTaskSequence](Get-CMTaskSequence.md)

[About task sequence steps: Apply Driver Package](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyDriverPackage)
