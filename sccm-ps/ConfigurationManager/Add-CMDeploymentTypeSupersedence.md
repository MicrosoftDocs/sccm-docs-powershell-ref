---
description: Add a deployment type supersedence in Configuration Manager.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/06/2020
schema: 2.0.0
title: Add-CMDeploymentTypeSupersedence
---

# Add-CMDeploymentTypeSupersedence

## SYNOPSIS

Add a deployment type supersedence in Configuration Manager.

## SYNTAX

```
Add-CMDeploymentTypeSupersedence [-SupersedingDeploymentType] <IResultObject>
 [-SupersededDeploymentType] <IResultObject> [-IsUninstall <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Add-CMDeploymentTypeSupersedence** cmdlet sets one deployment type to supersede another. Required inputs are the superseding deployment type and the superseded deployment type. You can get both objects from the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example gets the deployment type from **MyApp** and stores it as a variable **$oldAppVer**. It then supersedes this app deployment type with a newer version, using a deployment type from **MySupersedingApp**.

```powershell
$oldAppVer = Get-CMDeploymentType -ApplicationName "MyApp"

Add-CMDeploymentTypeSupersedence -SupersededDeploymentType $oldAppVer -SupersedingDeploymentType (Get-CMDeploymentType -ApplicationName "MySupersedingApp")
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

### -SupersededDeploymentType

Specifies a superseded (old) deployment type object. Get this object with the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

Specifies a superseding (new) deployment type object. Get this object with the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMDeploymentTypeSupersedence](./Get-CMDeploymentTypeSupersedence.md)

[Set-CMDeploymentTypeSupersedence](./Set-CMDeploymentTypeSupersedence.md)

[Remove-CMDeploymentTypeSupersedence](./Remove-CMDeploymentTypeSupersedence.md)
