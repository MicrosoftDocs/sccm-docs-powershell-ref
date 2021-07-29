---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
online version:
schema: 2.0.0
---

# New-CMTSRule

## SYNOPSIS

Create a rule to add to a Set Dynamic Variables task sequence step.

## SYNTAX

### VariableOnly (Default)
```
New-CMTSRule -Variable <Hashtable> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ComputerCondition
```
New-CMTSRule [-AssetTag <String>] [-MacAddress <String>] [-SerialNumber <String>] [-Uuid <String>]
 -Variable <Hashtable> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### LocationCondition
```
New-CMTSRule [-DefaultGateway <String>] -Variable <Hashtable> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MakeModelCondition
```
New-CMTSRule [-Make <String>] [-Model <String>] -Variable <Hashtable> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VariableCondition
```
New-CMTSRule [-ReferencedVariableName <String>] [-ReferencedVariableOperator <VariableOperatorType>]
 [-ReferencedVariableValue <String>] -Variable <Hashtable> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a rule that you can add to a [Set Dynamic Variables](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetDynamicVariables) task sequence step. When the task sequence runs this step, it evaluates the dynamic rules and variables in order. When it evaluates the rules on the specific device, it can then set task sequence variables based on those rules.

There are four types of rules:

- **Computer**: Evaluate values for hardware asset tag, UUID, serial number, or MAC address.
- **Location**: Evaluate values for the default network gateway.
- **Make and Model**: Evaluate values for the make and model of a computer.
- **Task sequence variable**: Add a task sequence variable, condition, and value to evaluate.

For more information, see [Dynamic rules and variables](/mem/configmgr/osd/understand/task-sequence-steps#dynamic-rules-and-variables).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set the download destination if in Windows PE

This example creates the following rule:

`IF _SMSTSInWinPE equals "TRUE" THEN SET OSDDownloadDestinationLocationType = "TSCache"`

It then adds this rule to an existing instance of this step in a task sequence.

```powershell
$tsrule = New-CMTSRule -Variable @{'OSDDownloadDestinationLocationType' = 'TSCache'} -ReferencedVariableName "_SMSTSInWinPE" -ReferencedVariableOperator equals -ReferencedVariableValue TRUE

$tsname = "Default IPU"
$tsstep = "Set Dynamic Variables"

Set-CMTSStepSetDynamicVariable -TaskSequenceName $tsname -StepName $tsstep -AddRule $tsrule
```

## PARAMETERS

### -AssetTag

Specify an **Asset tag** for the **Computer** rule type. The maximum value is 255 characters.

For example, if you set this value to `123456`, it adds the following rule: `IF Asset tag equals "123456" THEN`

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

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

### -DefaultGateway

Specify the **Default gateway** for the **Location** rule type.

For example, if you set this value to `192.168.10.1`, it adds the following rule: `IF Default gateway equals "192.168.10.1" THEN`

```yaml
Type: String
Parameter Sets: LocationCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -MacAddress

Specify the **MAC address** for the **Computer** rule type.

For example, if you set this value to `00:11:22:33:44:55`, it adds the following rule: `IF MAC address equals "00:11:22:33:44:55" THEN`

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Make

Specify the **Make** for the **Make and Model** rule type. To set the other value, use the **Model** parameter. The rule evaluates true when both values are true.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

For example, if you set this value to `Surface` and the **Model** to `*`, it adds the following rule: `IF Make equals "Surface" AND Model equals "*" THEN`

```yaml
Type: String
Parameter Sets: MakeModelCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Model

Specify the **Model** for the **Make and Model** rule type. To set the other value, use the **Make** parameter. The rule evaluates true when both values are true.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

For example, if you set this value to `*` and the **Make** to `Surface`, it adds the following rule: `IF Make equals "Surface" AND Model equals "*" THEN`

```yaml
Type: String
Parameter Sets: MakeModelCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableName

Specify the **Variable** for the **Task Sequence Variable** rule type. It requires that you also set the **ReferencedVariableOperator** and **ReferencedVariableValue** parameters.

This variable name can be a built-in task sequence variable or a custom one that you created. For more information, see [How to use task sequence variables in Configuration Manager](/mem/configmgr/osd/understand/using-task-sequence-variables).

For example, if you set the following values:

- **ReferencedVariableName**: `OSDRegisteredOrgName`
- **ReferencedVariableOperator**: `Equals`
- **ReferencedVariableValue**: `Contoso`

Then it adds the following rule: `IF OSDRegisteredOrgName equals "Contoso" THEN`

```yaml
Type: String
Parameter Sets: VariableCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableOperator

Specify the **Condition** for the **Task Sequence Variable** rule type. It requires that you also set the **ReferencedVariableName** and **ReferencedVariableValue** parameters. For the available operators, see the list of accepted values for this parameter.

For example, if you set the following values:

- **ReferencedVariableName**: `OSDRegisteredOrgName`
- **ReferencedVariableOperator**: `Equals`
- **ReferencedVariableValue**: `Contoso`

Then it adds the following rule: `IF OSDRegisteredOrgName equals "Contoso" THEN`

```yaml
Type: VariableOperatorType
Parameter Sets: VariableCondition
Aliases:
Accepted values: Exists, NotExists, Equals, NotEquals, Greater, GreaterEqual, Less, LessEqual, Like, NotLike

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferencedVariableValue

Specify the **Value** for the **Task Sequence Variable** rule type. It requires that you also set the **ReferencedVariableName** and **ReferencedVariableOperator** parameters.

For example, if you set the following values:

- **ReferencedVariableName**: `OSDRegisteredOrgName`
- **ReferencedVariableOperator**: `Equals`
- **ReferencedVariableValue**: `Contoso`

Then it adds the following rule: `IF OSDRegisteredOrgName equals "Contoso" THEN`

```yaml
Type: String
Parameter Sets: VariableCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SerialNumber

Specify a **Serial number** for the **Computer** rule type.

For example, if you set this value to `123456`, it adds the following rule: `IF Asset tag equals "123456" THEN`

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uuid

Specify a **UUID** for the **Computer** rule type.

For example, if you set this value to `de5ba380-f692-45e0-bbd3-0e40543b549e`, it adds the following rule: `IF UUID equals "de5ba380-f692-45e0-bbd3-0e40543b549e" THEN`

```yaml
Type: String
Parameter Sets: ComputerCondition
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable

Specify the existing or custom task sequence variables and associated values that the step should set when the rule evaluates to true.

For example, if you set this value to  `@{'OSDDownloadDestinationLocationType' = 'TSCache'}`, it adds the following variable after the `THEN` of the rule: `SET OSDDownloadDestinationLocationType = "TSCache"`

To specify more than one variable in the same hashtable, use a semi-colon (`;`) delimiter. For example: `@{'OSDRegisteredUserName' = 'Contoso';'OSDRegisteredOrgName' = 'Contoso'}`

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Variables

Required: True
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

### IResultObject#SMS_TaskSequence_Rule
## NOTES

## RELATED LINKS

[Set-CMTSStepSetDynamicVariable](Set-CMTSStepSetDynamicVariable.md)

[New-CMTSStepSetDynamicVariable](New-CMTSStepSetDynamicVariable.md)

[About task sequence steps - Set Dynamic Variables](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_SetDynamicVariables)

[How to use task sequence variables in Configuration Manager](/mem/configmgr/osd/understand/using-task-sequence-variables)
