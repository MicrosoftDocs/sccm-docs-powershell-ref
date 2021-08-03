---
description: Get the status of a software update deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/07/2020
schema: 2.0.0
title: Get-CMSoftwareUpdateDeploymentStatus
---

# Get-CMSoftwareUpdateDeploymentStatus

## SYNOPSIS

Get the status of a software update deployment.

## SYNTAX

```
Get-CMSoftwareUpdateDeploymentStatus -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMSoftwareUpdateDeploymentStatus** cmdlet gets the status of a software update deployment. Use the **Get-CMSoftwareUpdateDeployment** cmdlet to get a software update deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Display deployment status for a Patch Tuesday deployment

This example uses the **Get-CMSoftwareUpdateDeployment** cmdlet to get a software update deployment object. That object is then used as the input to show the status.

```powershell
$sudeploy = Get-CMSoftwareUpdateDeployment -Name "Patch Tuesday - Office and Edge 2020-07-15 00:11:11"

Get-CMSoftwareUpdateDeploymentStatus -InputObject $sudeploy
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

Specify a software update deployment object for which to get status. Use the **Get-CMSoftwareUpdateDeployment** cmdlet to get this object.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: SoftwareUpdate, Assignment, Deployment

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

[Get-CMSoftwareUpdateDeployment](Get-CMSoftwareUpdateDeployment.md)
