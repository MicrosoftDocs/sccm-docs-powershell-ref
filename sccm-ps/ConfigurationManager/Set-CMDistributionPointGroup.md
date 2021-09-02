---
description: Configure distribution point groups
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/26/2020
schema: 2.0.0
title: Set-CMDistributionPointGroup
---

# Set-CMDistributionPointGroup

## SYNOPSIS

Configure distribution point groups.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDistributionPointGroup [-Description <String>] -InputObject <IResultObject> [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMDistributionPointGroup [-Description <String>] -Id <String> [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMDistributionPointGroup [-Description <String>] -Name <String> [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMDistributionPointGroup** cmdlet changes the configuration settings of a distribution point group.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a distribution point group

This command renames the distribution point group **DpgDept01** to **DPG01**.

```powershell
Set-CMDistributionPointGroup -Name "DpgDept01" -NewName "DPG01"
```

### Example 2: Add a description to a distribution point group

This example first gets a distribution point group object with the **Get-CMDistributionPointGroup** cmdlet. It passes that object using the pipeline operator, and adds a description.

```powershell
Get-CMDistributionPointGroup -Name "DPG01" | Set-CMDistributionPointGroup -Description "Core distribution points, contact JQPublic"
```

## PARAMETERS

### -Description

Specify an optional description for the distribution point group.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

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

### -Id

Specify the ID of a distribution point group to configure. This ID is the **GroupID** property of the **SMS_DistributionPointGroup** WMI class. The format is a GUID, for example, `{19797865-d8d9-454b-855f-cb0f099204d0}`.

```yaml
Type: String
Parameter Sets: SetById
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a distribution point group object to configure. To get this object, use the [Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a distribution point group to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename the distribution point group.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
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
Default value: False
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
Default value: False
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

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[New-CMDistributionPointGroup](New-CMDistributionPointGroup.md)

[Remove-CMDistributionPointGroup](Remove-CMDistributionPointGroup.md)

[Manage distribution point groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/install-and-configure-distribution-points#bkmk_manage)
