---
title: Convert-CMDeploymentType
titleSuffix: Configuration Manager
description: Converts the deployment type of a Configuration Manager deployment application.
ms.date: 01/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Convert-CMDeploymentType

## SYNOPSIS

Converts the deployment type of a Configuration Manager deployment application.

## SYNTAX

```powershell
Convert-CMDeploymentType -InputObject <PSObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

The **Convert-CMDeploymentType** cmdlet converts the deployment type of a Microsoft System Center Configuration Manager application.

A deployment type is contained within an application and contains the information that Microsoft System Center Configuration Manager requires to install software.
A deployment type also contains rules that specify if and how the software is deployed.

This cmdlet allows for getting a native DeploymentType object from an SMS_DeploymentType WMI object instance. Can be combined with [Get-CMDeploymentType](Get-CMDeploymentType.md).

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> $cmdp = Get-CMDeploymentType -ApplicationName "CenterApp"
PS XYZ:\> Convert-CMDeploymentType $cmdp
```

This command gets the deployment type for the application named CenterApp, and then convert the deployment type.

## PARAMETERS

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

Specifies an SMS DeploymentType object. To obtain an SMS DeploymentType object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: IResultObject, DeploymentType, ProviderDeploymentTypeObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

## INPUTS

### System.Management.Automation.PSObject

## OUTPUTS

### System.Object

## RELATED LINKS

[Add-CMDeploymentType](Add-CMDeploymentType.md)

[Get-CMDeploymentType](Add-CMDeploymentType.md)

[Remove-CMDeploymentType](Remove-CMDeploymentType.md)

[Set-CMDeploymentType](Set-CMDeploymentType.md)
