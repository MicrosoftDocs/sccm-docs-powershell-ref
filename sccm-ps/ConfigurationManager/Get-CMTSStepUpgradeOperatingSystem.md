---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# Get-CMTSStepUpgradeOperatingSystem

## SYNOPSIS

Get the **Upgrade OS** step from a specific task sequence.

## SYNTAX

### ByValue (Default)
```
Get-CMTSStepUpgradeOperatingSystem [-InputObject] <IResultObject> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
Get-CMTSStepUpgradeOperatingSystem [-TaskSequenceId] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Get-CMTSStepUpgradeOperatingSystem [-TaskSequenceName] <String> [-StepName <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a task sequence step object for one or more instances of the **Upgrade OS** step. You can use this object to:

- Remove the step from a task sequence with [Remove-CMTSStepUpgradeOperatingSystem](Remove-CMTSStepUpgradeOperatingSystem.md)
- Copy the step to another task sequence with [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md)

For more information on this step, see [About task sequence steps: Upgrade OS](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_UpgradeOS).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets a task sequence object in the **$tsUpg** variable. It then passes that variable as the input object to get the **Upgrade OS** step.

```powershell
$tsName = "Default OS upgrade"
$tsUpg = Get-CMTaskSequence -Name $tsName -Fast

$tsStepNameUpgradeOs = "Upgrade Operating System"
$tsStepUpgradeOs = Get-CMTSStepUpgradeOperatingSystem -InputObject $tsUpg -StepName $tsStepNameUpgradeOs
```

## PARAMETERS

### -InputObject

Specify a task sequence object from which to get the **Upgrade OS** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

Specify the name of the **Upgrade OS** step to get from the task sequence.

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

Specify the **package ID** of the task sequence from which to get the **Upgrade OS** step. This value is a standard package ID, for example `XYZ00858`.

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

Specify the name of the task sequence from which to get the **Upgrade OS** step.

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

[New-CMTSStepUpgradeOperatingSystem](New-CMTSStepUpgradeOperatingSystem.md)
[Remove-CMTSStepUpgradeOperatingSystem](Remove-CMTSStepUpgradeOperatingSystem.md)
[Set-CMTSStepUpgradeOperatingSystem](Set-CMTSStepUpgradeOperatingSystem.md)

[Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md)
[Get-CMTaskSequence](Get-CMTaskSequence.md)

[About task sequence steps: Apply OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyOperatingSystemImage)
