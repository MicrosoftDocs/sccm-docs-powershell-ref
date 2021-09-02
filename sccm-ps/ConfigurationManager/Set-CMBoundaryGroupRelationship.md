---
description: Configure a boundary group relationship.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2020
schema: 2.0.0
title: Set-CMBoundaryGroupRelationship
---

# Set-CMBoundaryGroupRelationship

## SYNOPSIS

Configure a boundary group relationship.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMBoundaryGroupRelationship [-FallbackDPMinutes <Int32>] [-FallbackMPMinutes <Int32>]
 [-FallbackSmpMinutes <Int32>] [-FallbackSupMinutes <Int32>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByIdMandatory
```
Set-CMBoundaryGroupRelationship -DestinationGroupId <Int32> [-FallbackDPMinutes <Int32>]
 [-FallbackMPMinutes <Int32>] [-FallbackSmpMinutes <Int32>] [-FallbackSupMinutes <Int32>] [-PassThru]
 -SourceGroupId <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMBoundaryGroupRelationship -DestinationGroupName <String> [-FallbackDPMinutes <Int32>]
 [-FallbackMPMinutes <Int32>] [-FallbackSmpMinutes <Int32>] [-FallbackSupMinutes <Int32>] [-PassThru]
 -SourceGroupName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the relationship between boundary groups. For more information, see [Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMBoundaryGroupRelationship** cmdlet to get a boundary group relationship object. It then passes that object to the **Set-CMBoundaryGroupRelationship** cmdlet to change the fallback times. It changes the fallback for software update points to 120 minutes and for management points to immediate (0 minutes).

```powershell
Get-CMBoundaryGroupRelationship -DestinationGroupName "Swindon" -SourceGroupName "London" | Set-CMBoundaryGroupRelationship -FallbackSupMinutes 120 -FallbackMPMinutes 0
```

## PARAMETERS

### -DestinationGroupId

Specify the ID of the neighbor boundary group. This integer value is the **GroupID** property.

The destination boundary group can't be the same as the source boundary group.

```yaml
Type: Int32
Parameter Sets: SetByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationGroupName

Specify the name of the neighbor boundary group.

The destination boundary group can't be the same as the source boundary group.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
Aliases:

Required: True
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

### -FallbackDPMinutes

Specify an integer value for the fallback time in minutes for distribution points (DP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FallbackMPMinutes

Specify an integer value for the fallback time in minutes for management points (MP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FallbackSmpMinutes

Specify an integer value for the fallback time in minutes for state migration points (SMP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FallbackSupMinutes

Specify an integer value for the fallback time in minutes for software update points (SUP) from the source to the destination boundary group. To set the option to **Never fallback**, specify the value `-1`.

```yaml
Type: Int32
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

Specify a boundary group relationship object to configure. To get this object, use the [Get-CMBoundaryGroupRelationship](Get-CMBoundaryGroupRelationship.md) cmdlet.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -SourceGroupId

Specify the ID of the boundary group from which to configure the relationship. This integer value is the **GroupID** property.

```yaml
Type: Int32
Parameter Sets: SetByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceGroupName

Specify the name of the boundary group from which to configure the relationship.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
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

### IResultObject#SMS_BoundaryGroupRelationships
## NOTES

## RELATED LINKS

[Get-CMBoundaryGroupRelationship](Get-CMBoundaryGroupRelationship.md)

[New-CMBoundaryGroupRelationship](New-CMBoundaryGroupRelationship.md)

[Remove-CMBoundaryGroupRelationship](Remove-CMBoundaryGroupRelationship.md)

[Configure boundary groups for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups)
