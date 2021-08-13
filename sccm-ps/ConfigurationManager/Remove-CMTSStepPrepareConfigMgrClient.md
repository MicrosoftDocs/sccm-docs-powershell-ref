---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2021
online version:
schema: 2.0.0
---

# Remove-CMTSStepPrepareConfigMgrClient

## SYNOPSIS

Remove the **Prepare ConfigMgr Client for Capture** step from a task sequence.

## SYNTAX

### ByValue (Default)
```
Remove-CMTSStepPrepareConfigMgrClient [-InputObject] <IResultObject> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMTSStepPrepareConfigMgrClient [-TaskSequenceId] <String> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMTSStepPrepareConfigMgrClient [-TaskSequenceName] <String> [-StepName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove an instance of the **Prepare ConfigMgr Client for Capture** step from a task sequence.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets a task sequence object in the **$tsOsd** variable. It then passes that variable as the input object to remove the **Prepare ConfigMgr Client for Capture** step.

```powershell
$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsStepNamePrepClient = "Prepare ConfigMgr Client for Capture"
Remove-CMTSStepPrepareConfigMgrClient -InputObject $tsOsd -StepName $tsStepNamePrepClient -Force
```

## PARAMETERS

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

### -Force

Run the command without asking for confirmation.

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

Specify a task sequence object from which to remove the **Prepare ConfigMgr Client for Capture** step. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

Specify the name of the **Prepare ConfigMgr Client for Capture** step to remove from the task sequence.

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

Specify the **package ID** of the task sequence from which to remove the **Prepare ConfigMgr Client for Capture** step. This value is a standard package ID, for example `XYZ00858`.

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

Specify the name of the task sequence from which to remove the **Prepare ConfigMgr Client for Capture** step.

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

[Get-CMTSStepPrepareConfigMgrClient](Get-CMTSStepPrepareConfigMgrClient.md)
[New-CMTSStepPrepareConfigMgrClient](New-CMTSStepPrepareConfigMgrClient.md)
[Set-CMTSStepPrepareConfigMgrClient](Set-CMTSStepPrepareConfigMgrClient.md)

[About task sequence steps: Prepare ConfigMgr Client for Capture](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_PrepareConfigMgrClientforCapture)
