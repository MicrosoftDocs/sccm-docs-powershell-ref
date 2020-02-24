---
author: mumian
description: Adds a deployment type supersedence in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: jgao
ms.date: 01/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
schema: 2.0.0
title: Add-CMDeploymentTypeSupersedence
titleSuffix: Configuration Manager
---

# Add-CMDeploymentTypeSupersedence

## SYNOPSIS

Adds a deployment type supersedence in Configuration Manager.

## SYNTAX

```
Add-CMDeploymentTypeSupersedence [-SupersedingDeploymentType] <IResultObject>
 [-SupersededDeploymentType] <IResultObject> [-IsUninstall <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Add-CMDeploymentTypeSupersedence** cmdlet sets one deployment type to supersede another. Required input is a superseding type from [Get-CMDeploymentType](./Get-CMDeploymentType.md) and superseded deployment type from [Get-CMDeploymentType](./Get-CMDeploymentType.md).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | Add-CMDeploymentTypeSupersedence -SupersedingDeploymentType (Get-CMDeploymentType -ApplicationName MySupersedingApp)
```

## PARAMETERS

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

### -IsUninstall

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

### -SupersededDeploymentType

Specifies a superseded deployment type object.

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

Specifies a superseding deployment type object.

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

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMDeploymentTypeSupersedence](./Get-CMDeploymentTypeSupersedence.md)

[Set-CMDeploymentTypeSupersedence](./Set-CMDeploymentTypeSupersedence.md)

[Remove-CMDeploymentTypeSupersedence](./Remove-CMDeploymentTypeSupersedence.md)
