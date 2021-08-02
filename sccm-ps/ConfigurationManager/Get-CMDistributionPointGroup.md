---
description: Gets distribution point groups.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDistributionPointGroup
---

# Get-CMDistributionPointGroup

## SYNOPSIS
Gets distribution point groups.

## SYNTAX

### SearchByName (Default)
```
Get-CMDistributionPointGroup [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDistributionPointGroup -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDistributionPointGroup** cmdlet gets one or more distribution point groups.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a distribution point group by using an ID
```
PS XYZ:\> Get-CMDistributionPointGroup -Id "{6617708D-0F98-4898-8D05-9E882C23DCB2}"
```

This command get the distribution point group that has the ID 6617708D-0F98-4898-8D05-9E882C23DCB2.

### Example 2: Get a distribution point group by using a name
```
PS XYZ:\> Get-CMDistributionPointGroup -Name "Dpg01" -Id "{FA921CF2-89C9-407D-A21D-FE6947F2C00A}"
```

This command gets the distribution point group named Dpg01 and that has the ID FA921CF2-89C9-407D-A21D-FE6947F2C00A.

## PARAMETERS

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
Specifies an array of IDs of distribution point groups.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a distribution point group.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_DistributionPointGroup
### IResultObject#SMS_DistributionPointGroup
## NOTES

## RELATED LINKS

[New-CMDistributionPointGroup](New-CMDistributionPointGroup.md)

[Remove-CMDistributionPointGroup](Remove-CMDistributionPointGroup.md)

[Set-CMDistributionPointGroup](Set-CMDistributionPointGroup.md)


