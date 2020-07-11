---
description: Gets the status of classic software distribution deployments.
external help file:
Module Name: AdminUI.PS.Deployments
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDeploymentStatus
---

# Get-CMDeploymentStatus

## SYNOPSIS
Gets the status of classic software distribution deployments.

## SYNTAX

## DESCRIPTION
The **Get-CMDeploymentStatus** cmdlet gets the status of one or more classic software distribution deployments.
A classic software distribution is a legacy software distribution program on a client.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get the status of a deployment
```
PS XYZ:\> Get-CMDeploymentStatus -Name "Depack01"
```

This command gets the status of a deployment that is distributed to Configuration Manager clients by using the deployment package named Depack01.

## PARAMETERS

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Get-CMDeploymentPackage](Get-CMDeploymentPackage.md)

[Invoke-CMDeploymentSummarization](Invoke-CMDeploymentSummarization.md)

[Remove-CMDeployment](Remove-CMDeployment.md)


