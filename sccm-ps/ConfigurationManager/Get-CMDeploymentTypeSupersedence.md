---
description: Get the old deployment types that an application supersedes.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/05/2021
schema: 2.0.0
title: Get-CMDeploymentTypeSupersedence
---

# Get-CMDeploymentTypeSupersedence

## SYNOPSIS

Get the old deployment types that an application supersedes.

## SYNTAX

```
Get-CMDeploymentTypeSupersedence -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the old deployment types that an application supersedes.

For more information, see [Supersede applications in Configuration Manager](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

There are two example applications, **LOB app v7** and **LOB app v6**. **V7** supersedes **v6**. The first command uses the **Get-CMDeploymentType** cmdlet to get a deployment type object for **v7**. It then uses that object with **Get-CMDeploymentTypeSupersedence** to get the superseded deployment type for **v6**.

```powershell
$dt7 = Get-CMDeploymentType -ApplicationName "LOB app v7" -DeploymentTypeName "Install"
$dt6 = Get-CMDeploymentTypeSupersedence -InputObject $dt7
```

The output of this cmdlet is a deployment type object for **LOB app v6**, stored in the **dt6** variable.

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

Specify a deployment type object for an application that supersedes another. In other words, the _replacement_ deployment type. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: SupersedingDeploymentType

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

### IResultObject[]#SMS_DeploymentType

### IResultObject#SMS_DeploymentType

## NOTES

For more information on this return object and its properties, see [SMS_SCI_SysResUse server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymenttype-server-wmi-class).

## RELATED LINKS

[Set-CMApplicationSupersedence](Set-CMApplicationSupersedence.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Supersede applications in Configuration Manager](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence)
