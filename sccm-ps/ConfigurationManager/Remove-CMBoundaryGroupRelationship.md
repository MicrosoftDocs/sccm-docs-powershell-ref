---
description: Remove a boundary group relationship.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: Remove-CMBoundaryGroupRelationship
---

# Remove-CMBoundaryGroupRelationship

## SYNOPSIS

Remove a boundary group relationship.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMBoundaryGroupRelationship [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMBoundaryGroupRelationship [-DestinationGroupId <Int32>] [-Force] -SourceGroupId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Remove-CMBoundaryGroupRelationship [-DestinationGroupName <String>] [-Force] [-SourceGroupName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove the relationship between boundary groups. For more information, see [Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Remove-CMBoundaryGroupRelationship -DestinationGroupName "Swindon" -SourceGroupName "London" -Force
```

## PARAMETERS

### -DestinationGroupId

Specify the ID of the neighbor boundary group to remove. This integer value is the **GroupID** property.

The destination boundary group can't be the same as the source boundary group.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationGroupName

Specify the name of the neighbor boundary group to remove.

The destination boundary group can't be the same as the source boundary group.

```yaml
Type: String
Parameter Sets: SearchByName
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

### -Force

Run the command without asking for confirmation.

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

Specify a boundary group relationship object to remove. To get this object, use the [Get-CMBoundaryGroupRelationship](Get-CMBoundaryGroupRelationship.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceGroupId

Specify the ID of the boundary group from which to remove the relationship. This integer value is the **GroupID** property.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceGroupName

Specify the name of the boundary group from which to remove the relationship.

```yaml
Type: String
Parameter Sets: SearchByName
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### 

## NOTES

## RELATED LINKS

[Get-CMBoundaryGroupRelationship](Get-CMBoundaryGroupRelationship.md)

[New-CMBoundaryGroupRelationship](New-CMBoundaryGroupRelationship.md)

[Set-CMBoundaryGroupRelationship](Set-CMBoundaryGroupRelationship.md)

[Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups)
