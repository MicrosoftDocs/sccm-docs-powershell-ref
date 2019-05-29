---
title: Set-CMDistributionPointGroup
titleSuffix: Configuration Manager
description: Changes the configuration settings of distribution point groups.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Set-CMDistributionPointGroup

## SYNOPSIS
Changes the configuration settings of distribution point groups.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDistributionPointGroup -InputObject <IResultObject> [-Description <String>] [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMDistributionPointGroup -Id <String> [-Description <String>] [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMDistributionPointGroup -Name <String> [-Description <String>] [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDistributionPointGroup** cmdlet changes the configuration settings of one or more distribution point groups.

## EXAMPLES

### Example 1: Add a distribution point group to a security scope
```
PS C:\> Set-CMDistributionPointGroup -SecurityScopeAction AddMembership -SecurityScopeName "CScope02" -Name "DpgDept01"
```

This command adds the distribution point group as a member of the security scope named CScope02.

### Example 2: Remove a distribution point group from a security scope
```
PS C:\> Set-CMDistributionPointGroup -SecurityScopeAction RemoveMembership -SecurityScopeName "CScope02" -Name "DpgDept01"
```

This command removes the distribution point group named DpgDept01 as a member of the security scope named CScope02.

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

### -Description
Specifies a description for the distribution point group.

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

### -Id
Specifies an array of IDs for distribution point groups.

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
Specifies a **CMDistributionPointGroup** object.
To obtain a **CMDistributionPointGroup** object, use the [Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md) cmdlet.

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
Specifies a name of a distribution point group.

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
Specifies a new name for the distribution point group.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[New-CMDistributionPointGroup](New-CMDistributionPointGroup.md)

[Remove-CMDistributionPointGroup](Remove-CMDistributionPointGroup.md)
