---
description: Removes a boundary group.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMBoundaryGroup
---

# Remove-CMBoundaryGroup

## SYNOPSIS
Removes a boundary group.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMBoundaryGroup -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMBoundaryGroup -Id <String[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMBoundaryGroup -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMBoundaryGroup** cmdlet removes a boundary group from Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a boundary group that is specified by its ID
```
PS XYZ:\> Remove-CMBoundaryGroup -Id "16777219"
```

This command removes a boundary group that is specified by its identifier.
Because the *Force* parameter is not specified, you must confirm the action before it is performed.

### Example 2: Remove multiple boundary groups by using an InputObject
```
PS XYZ:\> $BoundaryObj = Get-CMBoundary -Name "BGroup01", "BGroup02", "BGroup03"
PS XYZ:\> Remove-CMBoundary -InputObject $BoundaryObj
```

The first command uses the **Get-CMBoundaryGroup** to get multiple boundary groups that are specified by their names, and stores this data into the $BoundaryObj variable.

The second command identifies and removes the boundaries that are specified by using the input object $BoundaryObj.
Because the *Force* parameter is not specified, you must confirm the action before it is performed.

## PARAMETERS

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

### -Id
Specifies an array of identifiers (IDs) for one or more boundary groups.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an input object to this cmdlet.
You can get the input object by using the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

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

### -Name
Specifies the name of a boundary group.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
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
Default value: False
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

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[New-CMBoundaryGroup](New-CMBoundaryGroup.md)

[Set-CMBoundaryGroup](Set-CMBoundaryGroup.md)


