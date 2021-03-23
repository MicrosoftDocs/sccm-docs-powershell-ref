---
description: Remove a deployment type supersedence relationship.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/05/2021
schema: 2.0.0
title: Remove-CMDeploymentTypeSupersedence
---

# Remove-CMDeploymentTypeSupersedence

## SYNOPSIS

Remove a deployment type supersedence relationship.

## SYNTAX

```
Remove-CMDeploymentTypeSupersedence [-Force] [-SupersededDeploymentType] <IResultObject>
 [-SupersedingDeploymentType] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a superseding deployment type from a superseded deployment type. In other words, remove the _replacement_ deployment type from the _old_ deployment type.

For more information, see [Supersede applications in Configuration Manager](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

There are two example applications, **LOB app v7** and **LOB app v6**. **V7** supersedes **v6**. The first command uses the **Get-CMDeploymentType** cmdlet to get a deployment type object for **v7**. It then uses that object with **Get-CMDeploymentTypeSupersedence** to get the superseded deployment type for **v6**. Finally it removes the supersedence relationship between the two objects.

```powershell
$dt7 = Get-CMDeploymentType -ApplicationName "LOB app v7" -DeploymentTypeName "Install"
$dt6 = Get-CMDeploymentTypeSupersedence -InputObject $dt7

Remove-CMDeploymentTypeSupersedence -SupersedingDeploymentType $dt7 -SupersededDeploymentType $dt6
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

### -Force

Forces the command to run without asking for user confirmation.

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

### -SupersededDeploymentType

Specify a deployment type object for an application that's superseded. In other words, the _old_ deployment type. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) or [Get-CMDeploymentTypeSupersedence](Get-CMDeploymentTypeSupersedence.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupersedingDeploymentType

Specify a deployment type object for an application that supersedes another. In other words, the _replacement_ deployment type. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
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

### System.Object
## NOTES

## RELATED LINKS

[Add-CMDeploymentTypeSupersedence](./Add-CMDeploymentTypeSupersedence.md)

[Get-CMDeploymentTypeSupersedence](./Get-CMDeploymentTypeSupersedence.md)

[Set-CMDeploymentTypeSupersedence](./Set-CMDeploymentTypeSupersedence.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Supersede applications in Configuration Manager](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence)
