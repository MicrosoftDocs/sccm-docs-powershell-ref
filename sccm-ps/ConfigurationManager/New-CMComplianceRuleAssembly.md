---
author: aczechowski
description: Creates a compliance rule assembly.
external help file: AdminUI.PS.Dcm.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMComplianceRuleAssembly
titleSuffix: Configuration Manager
---

# New-CMComplianceRuleAssembly

## SYNOPSIS
Creates a compliance rule assembly.

## SYNTAX

### AssemblyToken (Default)
```
New-CMComplianceRuleAssembly [-PublicKeyToken] -ExpressionOperator <RuleExpressionOperator>
 [-ReportNoncompliance] -RuleName <String> -InputObject <ConfigurationItemSetting> [-ExpectedValue <String[]>]
 [-NoncomplianceSeverity <NoncomplianceSeverity>] [-RuleDescription <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AssemblyCulture
```
New-CMComplianceRuleAssembly [-Culture] -ExpressionOperator <RuleExpressionOperator> [-ReportNoncompliance]
 -RuleName <String> -InputObject <ConfigurationItemSetting> [-ExpectedValue <String[]>]
 [-NoncomplianceSeverity <NoncomplianceSeverity>] [-RuleDescription <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
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

### -Culture
```yaml
Type: SwitchParameter
Parameter Sets: AssemblyCulture
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -ExpectedValue
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: ExpectedValues

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator
```yaml
Type: RuleExpressionOperator
Parameter Sets: (All)
Aliases:
Accepted values: And, Or, Other, IsEquals, NotEquals, GreaterThan, LessThan, Between, NotBetween, GreaterEquals, LessEquals, BeginsWith, NotBeginsWith, EndsWith, NotEndsWith, Contains, NotContains, AllOf, OneOf, NoneOf, SetEquals, SubsetOf, ExcludesAll

Required: True
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
```yaml
Type: ConfigurationItemSetting
Parameter Sets: (All)
Aliases: Setting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoncomplianceSeverity
```yaml
Type: NoncomplianceSeverity
Parameter Sets: (All)
Aliases:
Accepted values: None, Informational, Warning, Critical, CriticalWithEvent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicKeyToken
```yaml
Type: SwitchParameter
Parameter Sets: AssemblyToken
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportNoncompliance
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

### -RuleDescription
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

### -RuleName
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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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

### Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItemSetting

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
