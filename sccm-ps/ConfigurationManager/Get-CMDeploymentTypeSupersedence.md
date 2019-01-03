---
title: Get-CMDeploymentTypeSupersedence
titleSuffix: Configuration Manager
description: Gets a deployment type supersedence in Configuration Manager.
ms.date: 01/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Get-CMDeploymentTypeSupersedence

## SYNOPSIS

Gets a deployment type supersedence in Configuration Manager.

## SYNTAX

```
Get-CMDeploymentTypeSupersedence -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMDeploymentTypeSupersedence** cmdlet gets supersedence objects for a superseded deployment type. Required input is a superseded deployment type.

## EXAMPLES

### Example 1

```powershell
PS C:\>  Get-CMDeploymentType -ApplicationName MyApp | Get-CMDeploymentTypeSupersedence
```

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

Specifies a superseded deployment type object. 

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

IResultObject#SMS_DeploymentType

## RELATED LINKS

- [Add-CMDeploymentTypeSupersedence](./Add-CMDeploymentTypeSupersedence.md)
- [Set-CMDeploymentTypeSupersedence](./Set-CMDeploymentTypeSupersedence.md)
- [Remove-CMDeploymentTypeSupersedence](./Remove-CMDeploymentTypeSupersedence.md)