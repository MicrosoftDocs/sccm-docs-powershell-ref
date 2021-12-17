---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
online version:
schema: 2.0.0
---

# Get-CMDeploymentTypeRequirement

## SYNOPSIS

Get the requirement rules for a deployment type.

## SYNTAX

```
Get-CMDeploymentTypeRequirement -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the requirement rules for the specified application deployment type. You can use the returned object to add the same rules to another deployment type.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Copy requirement rules between deployment types

The following sample first gets a deployment type object from **AppA**. It passes that object to the **Get-CMDeploymentTypeRequirement** cmdlet to get its requirement rules. It then uses the **Set-CMScriptDeploymentType** cmdlet to add the same requirement rule to another deployment type on a different application.

```powershell
$dt1 = Get-CMDeploymentType -ApplicationName "AppA" -DeploymentTypeName "dt1"

$rule = $dt1 | Get-CMDeploymentTypeRequirement

Set-CMScriptDeploymentType -ApplicationName "AppB" -DeploymentTypeName "dt2" -AddRequirement $rule
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

Specify a deployment type object from which to get the requirement rules. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

### Rule[]

### Rule

## NOTES

## RELATED LINKS

[Get-CMDeploymentType](Get-CMDeploymentType.md)
