---
description: Create a detection method clause for a file system directory.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
schema: 2.0.0
title: New-CMDetectionClauseDirectory
---

# New-CMDetectionClauseDirectory

## SYNOPSIS

Create a detection method clause for a file system directory.

## SYNTAX

### Value
```
New-CMDetectionClauseDirectory -DirectoryName <String> -PropertyType <FileFolderProperty>
 -ExpectedValue <String[]> -ExpressionOperator <FileFolderRuleExpressionOperator> [-Is64Bit] -Path <String>
 [-Value] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseDirectory -DirectoryName <String> [-Is64Bit] -Path <String> [-Existence]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a clause in a detection method on an application. This clause is a rule for a file system folder that indicates the presence of an application.

To detect a file instead of a folder, use the [New-CMDetectionClauseFile](New-CMDetectionClauseFile.md) cmdlet.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this detection clause object to either the **AddDetectionClause** or **RemoveDetectionClause** parameters.

To group detection clauses, use the **GroupDetectionClauses** parameter on the deployment type cmdlets.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add an existence detection method

This example adds a detection clause that requires a specific product ID and directory name to exist.

```powershell
$app = Get-CMApplication -ApplicationName "CentralApp"
$guid = "9900a338-484b-4a18-884e-bce87654ce1b"
$clause1 = New-CMDetectionClauseWindowsInstaller -ProductCode $guid -Value -ExpressionOperator IsEquals -ExpectedValue "1.1.1.1"
$clause2 = New-CMDetectionClauseDirectory -DirectoryName "mymsi" -Path "C:\" -Existence

$app | Add-CMMsiDeploymentType -ContentLocation "\\myserver\mypath\mymsi.msi" -Force -AddDetectionClause ($clause1, $clause2)
```

### Example 2: Add a rule evaluation detection method

This example adds a rule-based detection clause to check that the folder was modified after 12/30/2020.

```powershell
$clause1 = New-CMDetectionClauseDirectory -DirectoryName "AdminConsole" -Path "%ProgramFiles(x86)%\Microsoft Endpoint Manager" -Value -PropertyType DateCreated -ExpressionOperator GreaterThan -ExpectedValue "2020-11-30T08:00:00Z"

Set-CMScriptDeploymentType -ApplicationName "Configuration Manager console" -DeploymentTypeName "Install" -AddDetectionClause $clause1
```

## PARAMETERS

### -DirectoryName

Specify the name of the folder that indicates the presence of the application. Use the **Path** parameter to specify the path to this folder.

For example, the Configuration Manager console installs by default to `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole`. To create a rule for this folder, set this parameter to `AdminConsole` and the **Path** parameter to `%ProgramFiles(x86)%\Microsoft Endpoint Manager`.

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

When you add this parameter, the folder must exist on the target system to indicate presence of this application.

Instead of just existence, to evaluate a rule for properties of this folder, use the **Value** parameter.

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

When you add the **Value** parameter, use **ExpectedValue** with **PropertyType** and **ExpressionOperator**. When you use these parameters, the folder must satisfy the rule to indicate the presence of this application. This **ExpectedValue** parameter specifies the value to compare against the file system.

The **PropertyType** parameter for this clause only accepts the date the folder was created or modified, so this value is a string with a valid datetime. For example, `"2020-11-30T08:00:00Z"`.

```yaml
Type: String[]
Parameter Sets: Value
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpressionOperator

When you add the **Value** parameter, use **ExpressionOperator** with **PropertyType** and **ExpectedValue**. When you use these parameters, the folder must satisfy the rule to indicate the presence of this application. This **ExpressionOperator** parameter specifies the operator to compare the file system value with the expected value.

```yaml
Type: FileFolderRuleExpressionOperator
Parameter Sets: Value
Aliases:
Accepted values: IsEquals, NotEquals, GreaterThan, LessThan, Between, GreaterEquals, LessEquals, OneOf, NoneOf

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

### -Is64Bit

Add this parameter to indicate that this folder is associated with a 32-bit application on 64-bit systems.

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

### -Path

Specify the path in the file system to the folder that indicates the presence of the application. Use the **DirectoryName** parameter to specify the name of the folder.

For example, the Configuration Manager console installs by default to `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole`. To create a rule for this folder, set this parameter to `%ProgramFiles(x86)%\Microsoft Endpoint Manager` and the **DirectoryName** parameter to `AdminConsole`.

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

### -PropertyType

When you add the **Value** parameter, use **PropertyType** with **ExpressionOperator** and **ExpectedValue**. When you use these parameters, the folder must satisfy the rule to indicate the presence of this application. This **PropertyType** parameter specifies the folder property to evaluate.

```yaml
Type: FileFolderProperty
Parameter Sets: Value
Aliases:
Accepted values: DateCreated, DateModified

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

When you add the **Value** parameter, the folder must satisfy the rule to indicate the presence of this application. Use this parameter with the following parameters: **ExpectedValue**, **ExpressionOperator**, and **PropertyType**.

Instead of evaluating a rule, to just check that the folder exists, use the **Existence** parameter.

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

[New-CMDetectionClauseFile](New-CMDetectionClauseFile.md)

[New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)

[New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)

[New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)
