---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/02/2021
online version:
schema: 2.0.0
---

# Get-CMDeploymentTypeDetectionClause

## SYNOPSIS

Get the detection clauses from the specified deployment type.

## SYNTAX

```
Get-CMDeploymentTypeDetectionClause -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to get the detection clauses from the specified deployment type.

You can use this cmdlet to get a detection clause from one app and apply it to another.

## EXAMPLES

### Example 1: Copy a detection clause between apps

This example gets an MSI deployment type from the **CenterApp** application. It then uses **Get-CMDeploymentTypeDetectionClause** to get the detection clause. The third line applies that clause with **Set-CMScriptDeploymentType** to another application.

```powershell
$appMsi = Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows Installer (.msi file)"

$clause1 = Get-CMDeploymentTypeDetectionClause -InputObject $appMsi

Set-CMScriptDeploymentType -ApplicationName "Configuration Manager console" -DeploymentTypeName "Install" -AddDetectionClause $clause1
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

### -InputObject

Specify a deployment type object from which to get the detection clause. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### DetectionClause[]

### DetectionClause

## NOTES

## RELATED LINKS

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Set-CMScriptDeploymentType](Set-CMScriptDeploymentType.md)

[Set-CMMsiDeploymentType](Set-CMMsiDeploymentType.md)

[Set-CMTaskSequenceDeploymentType](Set-CMTaskSequenceDeploymentType.md)
