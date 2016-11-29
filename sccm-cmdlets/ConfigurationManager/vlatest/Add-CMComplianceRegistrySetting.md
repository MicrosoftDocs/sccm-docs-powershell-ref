---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833622
schema: 2.0.0
ms.assetid: 99F92109-CB55-47FD-907E-F8104DBB2B12
---

# Add-CMComplianceRegistrySetting

## SYNOPSIS

## SYNTAX

### Value (Default)
```
Add-CMComplianceRegistrySetting [-DataType <SettingDataType>] [-Description <String>] [-ExpectedValue <Object>]
 [-ExpressionOperator <ExpressionOperator>] -InputObject <IResultObject> [-Is64Bit] -Name <String>
 [-NoncomplianceSeverity <NoncomplianceSeverity>] [-RegistryHive <RegistryRootKey>] [-RegistryKey <String>]
 [-RegistryValue <String>] [-Remediate] [-ReportNoncompliance] [-RuleDescription <String>] -RuleName <String>
 [-ValueRule] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Existential
```
Add-CMComplianceRegistrySetting [-DataType <SettingDataType>] [-Description <String>]
 [-Existence <ExistenceType>] [-ExistentialRule] -InputObject <IResultObject> [-Is64Bit] -Name <String>
 [-NoncomplianceSeverity <NoncomplianceSeverity>] [-RegistryHive <RegistryRootKey>] [-RegistryKey <String>]
 [-RegistryValue <String>] [-RuleDescription <String>] -RuleName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NoRules
```
Add-CMComplianceRegistrySetting [-DataType <SettingDataType>] [-Description <String>]
 -InputObject <IResultObject> [-Is64Bit] -Name <String> [-NoRule] [-RegistryHive <RegistryRootKey>]
 [-RegistryKey <String>] [-RegistryValue <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Rules
```
Add-CMComplianceRegistrySetting [-DataType <SettingDataType>] [-Description <String>]
 -InputObject <IResultObject> [-Is64Bit] -Name <String> [-RegistryHive <RegistryRootKey>]
 [-RegistryKey <String>] [-RegistryValue <String>] [-Rule <Rule[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DataType
```yaml
Type: SettingDataType
Parameter Sets: (All)
Aliases: 
Accepted values: String, Integer, DateTime, FloatingPoint, Version, StringArray

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
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

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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

### -Existence
```yaml
Type: ExistenceType
Parameter Sets: Existential
Aliases: 
Accepted values: MustExist, MustNotExist

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExistentialRule
```yaml
Type: SwitchParameter
Parameter Sets: Existential
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedValue
```yaml
Type: Object
Parameter Sets: Value
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator
```yaml
Type: ExpressionOperator
Parameter Sets: Value
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Is64Bit
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

### -Name
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

### -NoRule
```yaml
Type: SwitchParameter
Parameter Sets: NoRules
Aliases: NoRules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoncomplianceSeverity
```yaml
Type: NoncomplianceSeverity
Parameter Sets: Value, Existential
Aliases: 
Accepted values: None, Informational, Warning, Critical, CriticalWithEvent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryHive
```yaml
Type: RegistryRootKey
Parameter Sets: (All)
Aliases: 
Accepted values: ClassesRoot, CurrentConfig, CurrentUser, LocalMachine, Users

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RegistryKey
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

### -RegistryValue
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

### -Remediate
```yaml
Type: SwitchParameter
Parameter Sets: Value
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportNoncompliance
```yaml
Type: SwitchParameter
Parameter Sets: Value
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Rule
```yaml
Type: Rule[]
Parameter Sets: Rules
Aliases: Rules

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleDescription
```yaml
Type: String
Parameter Sets: Value, Existential
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleName
```yaml
Type: String
Parameter Sets: Value, Existential
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ValueRule
```yaml
Type: SwitchParameter
Parameter Sets: Value
Aliases: 

Required: False
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


