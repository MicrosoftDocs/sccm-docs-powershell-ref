---
author: aczechowski
description: Removes a Configuration Manager boundary.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMBoundary
titleSuffix: Configuration Manager
---

# Remove-CMBoundary

## SYNOPSIS
Removes a Configuration Manager boundary.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMBoundary -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMBoundary -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMBoundary -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMBoundary** cmdlet removes a boundary from Microsoft System Center Configuration Manager.

In System Center Configuration Manager, a boundary is an intranet location that contains one or more devices that you can manage.
A boundary can be an IP subnet, Active Directory site name, IPv6 prefix, or an IP address range.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a boundary that is specified by its ID
```
PS XYZ:\> Remove-CMBoundary -Id "16777223"
```

This command removes the boundary that has an identifier of 16777223.
Because the *Force* parameter is not specified, you must confirm the action before it is performed.

### Example 2: Remove a boundary by using an InputObject
```
PS XYZ:\> $BoundaryObj = Get-CMBoundary -Id "16777223"
PS XYZ:\>
Remove-Boundary -InputObject $BoundaryObj
```

In this example, the first command uses the **Get-CMBoundary** cmdlet to get a boundary that has the ID of 16777223, and inserts it into the input object $BoundaryObj.

The second command identifies the boundary by using the input object $BoundaryObj and then removes the boundary.
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
Specifies an array of boundary identifiers (IDs).

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: BoundaryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an input object to this cmdlet.
You can get the input object by using the Get-CMBoundary cmdlet.

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
Specifies an array of boundary names.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: DisplayName

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMBoundary](Get-CMBoundary.md)

[New-CMBoundary](New-CMBoundary.md)

[Set-CMBoundary](Set-CMBoundary.md)

[Remove-CMBoundaryFromGroup](Remove-CMBoundaryFromGroup.md)

[Remove-CMBoundaryGroup](Remove-CMBoundaryGroup.md)


