---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionSoftware

## SYNOPSIS

Create an _installed software_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionSoftware [-IsAnyVersion <Boolean>] -MsiFilePath <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an _installed software_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates a condition object for the Configuration Manager console MSI.

It then uses the **Set-CMTSStepRunPowerShellScript** cmdlet to add this condition object to the **Run PowerShell Script** step of the **Default OS deployment** task sequence.

```powershell
$msi = "\\cm01.contoso.com\SMS_XYZ\bin\i386\adminconsole.msi"

$condition = New-CMTSStepConditionSoftware -MsiFilePath $msi -IsAnyVersion $true

$tsNameOsd = "Default OS deployment"
$tsStepNameRunPwsh = "Run PowerShell Script"

Set-CMTSStepRunPowerShellScript -TaskSequenceName $tsNameOsd -StepName $tsStepNameRunPwsh -AddCondition $condition

```

This sample script creates the following condition on the step:

`Software  An version of "Microsoft Endpoint Configuration Manager Console" installed`

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

### -IsAnyVersion

Use this parameter to determine how the condition matches the MSI codes:

- `$true`: Match any version of this product, MSI _upgrade code_ only
- `$false`: Match this specific product, MSI _product code_ and _upgrade code_

If you don't specify this parameter, by default it matches the specific product.

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

### -MsiFilePath

Specify the path to the MSI file to evaluate. The cmdlet reads the product details from this MSI. The path to the MSI isn't saved, just the product details.

For example, it saves the following details for the Configuration Manager version 2107 **AdminConsole.msi**:

- `ProductCode`: **{B3842C82-95EB-472C-940A-D82C4A10857D}**
- `ProductName`: **Microsoft Endpoint Configuration Manager Console**
- `UpgradeCode`: **{B038D5E8-6C93-4A05-9E21-240324CFDF0E}**
- `Version`: **5.2107.1059.1000**

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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_SoftwareConditionExpression

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_SoftwareConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_softwareconditionexpression-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepConditionSoftware](Get-CMTSStepConditionSoftware.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
