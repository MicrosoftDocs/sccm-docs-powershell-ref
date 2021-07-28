---
description: Create a detection method clause for a file.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
schema: 2.0.0
title: New-CMDetectionClauseFile
---

# New-CMDetectionClauseFile

## SYNOPSIS

Create a detection method clause for a file.

## SYNTAX

### Value
```
New-CMDetectionClauseFile -FileName <String> -PropertyType <FileFolderProperty> -ExpectedValue <String[]>
 -ExpressionOperator <FileFolderRuleExpressionOperator> [-Is64Bit] -Path <String> [-Value]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### Existence
```
New-CMDetectionClauseFile -FileName <String> [-Is64Bit] -Path <String> [-Existence] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a clause in a detection method on an application. This clause is a rule for a file that indicates the presence of an application.

To detect a folder instead of a file, use the [New-CMDetectionClauseDirectory](New-CMDetectionClauseDirectory.md) cmdlet.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this detection clause object to either the **AddDetectionClause** or **RemoveDetectionClause** parameters.

To group detection clauses, use the **GroupDetectionClauses** parameter on the deployment type cmdlets.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Detect an application by version

This example detects the application **app.exe** in a specific folder where the version is greater than or equal to `1.0.0`.

```powershell
$clause = New-CMDetectionClauseFile -Path "C:\Program Files\Application" -FileName App.exe -Value -PropertyType Version -ExpressionOperator GreaterEquals -ExpectedValue "1.0.0"

Set-CMScriptDeploymentType -ApplicationName "CentralApp" -DeploymentTypeName "Scripted install" -AddDetectionClause $clause
```

### Example 2: Create multiple clauses for an MSI app deployment type

This example creates two file clauses and one registry clause, and then uses them to add an MSI deployment type to an app.

```powershell
$cla1=New-CMDetectionClauseFile -FileName "filetest" -PropertyType Size -ExpectedValue 123 -ExpressionOperator IsEquals -Path "C:\" -Value -Is64Bit
$cla2=New-CMDetectionClauseFile -FileName "foldertest" -PropertyType DateCreated -ExpectedValue (Get-Date) -ExpressionOperator LessThan -Path "C:\" -Value
$cla3=New-CMDetectionClauseRegistryKey -Hive ClassesRoot -KeyName "aaa"
$logic1=$cla1.Setting.LogicalName
$logic2=$cla2.Setting.LogicalName
$logic3=$cla3.Setting.LogicalName

Add-CMMsiDeploymentType -AddDetectionClause $cla1,$cla2,$cla3 -ApplicationName "app" -DeploymentTypeName "dt" -InstallCommand "mycommand" -ContentLocation "\\server\sources\Orca.msi" -GroupDetectionClauses $logic1,$logic2 -DetectionClauseConnector {LogicalName=$logic2;Connector="or"},{LogicalName=$logic3;Connector="or"}
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

When you add this parameter, the file must exist on the target system to indicate presence of this application.

Instead of just existence, to evaluate a rule for properties of this file, use the **Value** parameter.

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

When you add the **Value** parameter, use **ExpectedValue** with **PropertyType** and **ExpressionOperator**. When you use these parameters, the file must satisfy the rule to indicate the presence of this application. This **ExpectedValue** parameter specifies the value to compare against the file system.

The value to compare depends upon the specified **PropertyType**.

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

When you add the **Value** parameter, use **ExpressionOperator** with **PropertyType** and **ExpectedValue**. When you use these parameters, the file must satisfy the rule to indicate the presence of this application. This **ExpressionOperator** parameter specifies the operator to compare the file system value with the expected value.

Starting in version 2010, the parameter type changed from _RuleExpressionOperator_ to _FileFolderRuleExpressionOperator_.

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

### -FileName

Specify the name of the file that indicates the presence of the application. Use the **Path** parameter to specify the path to this file.

For example, the Configuration Manager console installs by default to `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\Microsoft.ConfigurationManagement.exe`. To create a rule for this file, set this parameter to `Microsoft.ConfigurationManagement.exe` and the **Path** parameter to `%ProgramFiles(x86)%\Microsoft Endpoint Manager\AdminConsole\bin`.

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

Add this parameter to indicate that this file is associated with a 32-bit application on 64-bit systems.

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

Specify the path in the file system to the file that indicates the presence of the application. Use the **FileName** parameter to specify the name of the file.

For example, the Configuration Manager console installs by default to `C:\Program Files (x86)\Microsoft Endpoint Manager\AdminConsole\bin\Microsoft.ConfigurationManagement.exe`. To create a rule for this file, set this parameter to `%ProgramFiles(x86)%\Microsoft Endpoint Manager\AdminConsole\bin` and the **FileName** parameter to `Microsoft.ConfigurationManagement.exe`.

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

When you add the **Value** parameter, use **PropertyType** with **ExpressionOperator** and **ExpectedValue**. When you use these parameters, the file must satisfy the rule to indicate the presence of this application. This **PropertyType** parameter specifies the file property to evaluate.

For example, you set this parameter to `Version`, set **ExpressionOperator** to `IsEquals`, and **ExpectedValue** to `1.48.1.0`. The rule then checks the specified file to have that same file version.

```yaml
Type: FileFolderProperty
Parameter Sets: Value
Aliases:
Accepted values: DateCreated, DateModified, Version, Size

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

When you add the **Value** parameter, the file must satisfy the rule to indicate the presence of this application. Use this parameter with the following parameters: **ExpectedValue**, **ExpressionOperator**, and **PropertyType**.

Instead of evaluating a rule, to just check that the file exists, use the **Existence** parameter.

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

[New-CMDetectionClauseRegistryKey](New-CMDetectionClauseRegistryKey.md)

[New-CMDetectionClauseRegistryKeyValue](New-CMDetectionClauseRegistryKeyValue.md)

[New-CMDetectionClauseWindowsInstaller](New-CMDetectionClauseWindowsInstaller.md)
