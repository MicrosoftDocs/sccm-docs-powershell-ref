---
title: Get-CMTaskSequence
titleSuffix: Configuration Manager
description: Gets Configuration Manager task sequences.
ms.date: 11/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Get-CMTaskSequence

## SYNOPSIS

Gets Configuration Manager task sequences.

## SYNTAX

### SearchByName (Default)

```powershell
Get-CMTaskSequence [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory

```powershell
Get-CMTaskSequence -TaskSequencePackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMTaskSequence** cmdlet gets Microsoft System Center Configuration Manager task sequences.
A task sequence includes configuration and operating system deployment settings for a System Center Configuration Manager client computer.

You can specify a name or ID to get a specific sequence.
You can also specify a security scope, by itself or with a name or ID, to get sequences with that security scope.

## EXAMPLES

### Example 1: Get a task sequence by name

```powershell
PS C:\> Get-CMTaskSequence -Name "taskSequence"
```

This command gets the task sequence named taskSequence.

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

### -Name

Specifies a name for a task sequence.

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

### -TaskSequencePackageId

Specifies the ID of a task sequence package.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[New-CMTaskSequence](New-CMTaskSequence.md)
[Get-CMTaskSequence](Get-CMTaskSequence.md)
[Set-CMTaskSequence](Set-CMTaskSequence.md)
[Copy-CMTaskSequence](Copy-CMTaskSequence.md)
[Enable-CMTaskSequence](Enable-CMTaskSequence.md)
[Disable-CMTaskSequence](Disable-CMTaskSequence.md)
[Import-CMTaskSequence](Import-CMTaskSequence.md)
[Export-CMTaskSequence](Export-CMTaskSequence.md)
[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
