---
description: Get the status details of a Configuration Manager deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/06/2020
schema: 2.0.0
title: Get-CMDeploymentStatusDetails
---

# Get-CMDeploymentStatusDetails

## SYNOPSIS

Get the status details of a Configuration Manager deployment.

## SYNTAX

```
Get-CMDeploymentStatusDetails -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMDeploymentStatusDetails** cmdlet gets the status details of a Configuration Manager deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example gets the status of a task sequence deployment using the **Get-CMPackageDeploymentStatus** cmdlet. It then displays the status details using a variable object.

```powershell
$status = Get-CMPackageDeploymentStatus -Name "TS Name"
Get-CMDeploymentStatusDetails -InputObject $status[1]
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

Specify an deployment status object to get details. Use the [Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md) cmdlet to get the object. If that cmdlet returns more than one status, it stores them in an array.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMApplicationDeploymentStatus](Get-CMApplicationDeploymentStatus.md)

[Get-CMBaselineDeploymentStatus](Get-CMBaselineDeploymentStatus.md)

[Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)

[Get-CMSoftwareUpdateDeploymentStatus](Get-CMSoftwareUpdateDeploymentStatus.md)
