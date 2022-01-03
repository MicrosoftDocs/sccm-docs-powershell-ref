---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
schema: 2.0.0
title: Set-CMDeploymentTypeSupersedence
---

# Set-CMDeploymentTypeSupersedence

## SYNOPSIS

Configure a supersedence relationship on an application. This cmdlet is deprecated.

## SYNTAX

```
Set-CMDeploymentTypeSupersedence -InputObject <IResultObject> [-IsUninstall <Boolean>] [-PassThru]
 -SupersedingDeploymentType <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!IMPORTANT]
> Starting in version 2111, this cmdlet is deprecated and may be removed in a future release. Use the [Set-CMApplicationSupersedence](Set-CMApplicationSupersedence.md) cmdlet instead.

Use this cmdlet to configure a supersedence relationship on an application.

For more information, see [Supersede applications in Configuration Manager](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

There are two example applications, **LOB app v7** and **LOB app v6**. **V7** supersedes **v6**. The first two commands use the **Get-CMDeploymentType** cmdlet to get deployment type objects. It then uses those objects with to configure the supersedence relationship.

```powershell
$dt7 = Get-CMDeploymentType -ApplicationName "LOB app v7" -DeploymentTypeName "Install"
$dt6 = Get-CMDeploymentType -ApplicationName "LOB app v6" -DeploymentTypeName "Install"

Set-CMDeploymentTypeSupersedence -SupersedingDeploymentType $dt7 -InputObject $dt6 -IsUninstall $true
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

Specify a deployment type object for the application to supersede. In other words, the _old_ deployment type. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) or [Get-CMDeploymentTypeSupersedence](Get-CMDeploymentTypeSupersedence.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: SupersededDeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsUninstall

If `$false`, the new deployment type (superseding) will upgrade the installed deployment type (superseded). If you set this parameter to `$true`, Configuration Manager uninstalls the previous deployment type when it installs the new deployment type.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -SupersedingDeploymentType

Specify a deployment type object for the application to supersede the other. In other words, the _replacement_ deployment type. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Set-CMApplicationSupersedence](Set-CMApplicationSupersedence.md)

[Get-CMDeploymentTypeSupersedence](./Get-CMDeploymentTypeSupersedence.md)

[Supersede applications in Configuration Manager](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence)
