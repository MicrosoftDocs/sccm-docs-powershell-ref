---
description: Create a detection method clause for an MSI product code.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMDetectionClauseWindowsInstaller
---

# New-CMDetectionClauseWindowsInstaller

## SYNOPSIS

Create a detection method clause for an MSI product code.

## SYNTAX

### Value
```
New-CMDetectionClauseWindowsInstaller -ExpectedValue <String>
 -ExpressionOperator <WindowsInstallerRuleExpressionOperator> -ProductCode <Guid> [-PropertyType <MSIProperty>]
 [-Value] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseWindowsInstaller -ProductCode <Guid> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a clause in a detection method on an application. This clause is a rule for a Windows Installer (MSI) product code that indicates the presence of an application.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this detection clause object to either the **AddDetectionClause** or **RemoveDetectionClause** parameters.

To group detection clauses, use the **GroupDetectionClauses** parameter on the deployment type cmdlets.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Detect the existence of an MSI product code

This example adds the Configuration Manager console MSI product code to the deployment type.

```powershell
$clause = New-CMDetectionClauseWindowsInstaller -Existence -ProductCode 4F7840A9-9816-45E2-9F6C-F7067A8BC0FD

Set-CMScriptDeploymentType -ApplicationName "Configuration Manager console" -DeploymentTypeName "Install" -AddDetectionClause $clause
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

### -Existence

When you add this parameter, the MSI product code must exist on the target system to indicate presence of this application.

Instead of just existence, to also evaluate a version condition, use the **Value** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: Existence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpectedValue

When you add the **Value** parameter, use **ExpectedValue** with **PropertyType** and **ExpressionOperator**. When you use these parameters, the MSI version must satisfy the rule to indicate the presence of this application. This **ExpectedValue** parameter specifies the value to compare against the device.

<!-- The value to compare depends upon the specified **PropertyType**. -->

```yaml
Type: String
Parameter Sets: Value
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator

When you add the **Value** parameter, use **ExpressionOperator** with **PropertyType** and **ExpectedValue**. When you use these parameters, the MSI version must satisfy the rule to indicate the presence of this application. This **ExpressionOperator** parameter specifies the operator to compare the device's value with the expected value.

Starting in version 2010, the parameter type changed from _RuleExpressionOperator_ to _WindowsInstallerRuleExpressionOperator_.

```yaml
Type: WindowsInstallerRuleExpressionOperator
Parameter Sets: Value
Aliases:
Accepted values: IsEquals, NotEquals, GreaterThan, LessThan, GreaterEquals, LessEquals

Required: True
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

### -ProductCode

Specify the Windows Installer product code that indicates the presence of this application. The format is a GUID, for example `4F7840A9-9816-45E2-9F6C-F7067A8BC0FD`.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyType

When you add the **Value** parameter, use **PropertyType** with **ExpressionOperator** and **ExpectedValue**. When you use these parameters, the MSI version must satisfy the rule to indicate the presence of this application.

This **PropertyType** parameter currently only supports a single value, `ProductVersion`.

```yaml
Type: MSIProperty
Parameter Sets: Value
Aliases:
Accepted values: ProductVersion

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

When you add the **Value** parameter, along with the product code, the MSI version must also satisfy the rule to indicate the presence of this application. Use this parameter with the following parameters: **ExpectedValue**, **ExpressionOperator**, and **PropertyType**.

Instead of evaluating a rule, to just check the MSI product code, use the **Existence** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: Value
Aliases: ValueRule

Required: True
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

### System.Object
## NOTES

## RELATED LINKS

[New-CMDetectionClauseDirectory](New-CMDetectionClauseDirectory.md)

[New-CMDetectionClauseFile](New-CMDetectionClauseFile.md)

[New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)

[New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)
