---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 09/02/2021
online version:
schema: 2.0.0
---

# New-CMTSStepConditionRegistry

## SYNOPSIS

Create a _registry setting_ condition for a task sequence step.

## SYNTAX

```
New-CMTSStepConditionRegistry -RegistryKey <String> -RegistryOperator <VariableOperatorType>
 [-RegistryValueData <String>] [-RegistryValueName <String>] -RootKey <RegistryRootKeyType>
 [-ValueType <RegistryValueType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a _registry setting_ condition object for a task sequence step. Then use one of the **New-CMTSStep\*** or **Set-CMTSStep\*** cmdlets with the **Condition** or **AddCondition** parameters. For example, [Set-CMTSStepApplyDataImage](Set-CMTSStepApplyDataImage.md).

For more information, see [Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first creates the condition object for the registry setting that checks the Configuration Manager client log level.

It then uses the **Set-CMTSStepSetDynamicVariable** cmdlet to add this condition object to the **Set Dynamic Variables** step of the **Default OS deployment** task sequence.

```powershell
$root = "HKeyLocalMachine"
$key = "SOFTWARE\Microsoft\CCM\Logging\@Global"
$name = "LogLevel"
$type = "RegistryDWord"
$value = 1

$condition = New-CMTSStepConditionRegistry -RootKey $root -RegistryKey $key -RegistryOperator Equals -RegistryValueName $name -ValueType $type -RegistryValueData $value

$tsNameOsd = "Default OS deployment"
$tsStepNameDynVar = "Set Dynamic Variables"

Set-CMTSStepSetDynamicVariable -TaskSequenceName $tsNameOsd -StepName $tsStepNameDynVar -AddCondition $condition
```

This sample script creates the following condition on the step:

`Registry  "HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\CCM\Logging\@Global\LogLevel" (REG_DWORD) equals "1"`

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

### -RegistryKey

Specify the registry key path to check. For example, with the `HKeyLocalMachine` **RootKey**, you can specify the registry key `SOFTWARE\Microsoft\CCM`.

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

### -RegistryOperator

Use this parameter to specify the operator for the task sequence to evaluate the registry value. If you use the `Exists` or `NotExists` values, then you don't need to use the **RegistryValueData** parameter.

```yaml
Type: VariableOperatorType
Parameter Sets: (All)
Aliases:
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryValueData

If you use a comparative **RegistryOperator** like `Equals`, use this parameter to specify the value data to evaluate. Use **ValueType** to specify the registry type.

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

### -RegistryValueName

Specify the name of the registry value to check. If you don't specify this parameter, the condition checks the **(Default)** value of the specified **RegistryKey**.

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

### -RootKey

Specify the registry root key to check.

```yaml
Type: RegistryRootKeyType
Parameter Sets: (All)
Aliases:
Accepted values: HKeyCurrentUser, HKeyLocalMachine, HKeyUsers, HKeyCurrentConfig

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueType

Specify the type of registry value to check. Use this parameter with the **RegistryValueData** to specify the value data.

```yaml
Type: RegistryValueType
Parameter Sets: (All)
Aliases:
Accepted values: RegistrySZ, RegistryExpandSZ, RegistryDWord

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

### IResultObject#SMS_TaskSequence_RegistryConditionExpression

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_RegistryConditionExpression server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_registryconditionexpression-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepConditionRegistry](Get-CMTSStepConditionRegistry.md)

[Use the task sequence editor: Conditions](/mem/configmgr/osd/understand/task-sequence-editor#bkmk_conditions)
