---
description: Removes a deployment type supersedence in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/02/2019
schema: 2.0.0
title: Remove-CMDeploymentTypeSupersedence
---

# Remove-CMDeploymentTypeSupersedence

## SYNOPSIS

Removes a deployment type supersedence in Configuration Manager.

## SYNTAX

```
Remove-CMDeploymentTypeSupersedence [-Force] [-SupersededDeploymentType] <IResultObject>
 [-SupersedingDeploymentType] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-CMDeploymentTypeSupersedence** cmdlet removes a superseding deployment type from a superseded deployment type. Required input is a superseding type from [Get-CMDeploymentType](./Get-CMDeploymentType.md) or [Get-CMDeploymentTypeSupersedence](./Get-CMDeploymentTypeSupersedence.md) and superseded deployment type from [Get-CMDeploymentType](./Get-CMDeploymentType.md).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | Remove-CMDeploymentTypeSupersedence -SupersedingDeploymentType (Get-CMDeploymentType -ApplicationName MySupersedingApp)
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

### -SupersededDeploymentType

Specifies a superseded deployment type.

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

Specifies a superseding deployment type.

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
