---
description: Sets a deployment type supersedence in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/02/2019
schema: 2.0.0
title: Set-CMDeploymentTypeSupersedence
---

# Set-CMDeploymentTypeSupersedence

## SYNOPSIS

Sets a deployment type supersedence in Configuration Manager.

## SYNTAX

```
Set-CMDeploymentTypeSupersedence -InputObject <IResultObject> [-IsUninstall <Boolean>]
 -SupersedingDeploymentType <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMDeploymentTypeSupersedence** cmdlet configures settings for a deployment type supersedence. Required input is a superseding type from [Get-CMDeploymentType](./Get-CMDeploymentType.md) or [Get-CMDeploymentTypeSupersedence](./Get-CMDeploymentTypeSupersedence.md) and superseded deployment type from [Get-CMDeploymentType](./Get-CMDeploymentType.md).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```
PS XYZ:\>  Get-CMDeploymentType -ApplicationName MyApp | Set-CMDeploymentTypeSupersedence -SupersedingDeploymentType (Get-CMDeploymentType -ApplicationName MySupersedingApp) -IsUninstall $true
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
Aliases: SupersededDeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -PassThru

Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

Specifies a superseding deployment type object.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMDeploymentTypeSupersedence](./Add-CMDeploymentTypeSupersedence.md)

[Get-CMDeploymentTypeSupersedence](./Get-CMDeploymentTypeSupersedence.md)

[Remove-CMDeploymentTypeSupersedence](./Remove-CMDeploymentTypeSupersedence.md)
