---
author: aczechowski
description: Gets a security scope.
external help file: AdminUI.PS.Rba.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMSecurityScope
titleSuffix: Configuration Manager
---

# Get-CMSecurityScope

## SYNOPSIS
Gets a security scope.

## SYNTAX

### SearchByName (Default)
```
Get-CMSecurityScope [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSecurityScope -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSecurityScope** cmdlet gets one or more security scopes in Microsoft System Center Configuration Manager.
You can get a security scope by its name or ID.
If you don't provide any parameters, all security scopes are returned.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a security scope by name
```
PS XYZ:\> Get-CMSecurityScope -Name "Scope"
```

This command gets the security scope named Scope.

### Example 2: Get a security scope by using a wildcard
```
PS XYZ:\> Get-CMSecurityScope -Name "S*"
```

This command gets all security scope objects that have a name beginning with "S".

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

### -Id
Specifies the ID of a security scope.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CategoryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a security scope.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMSecurityScope](New-CMSecurityScope.md)

[Remove-CMSecurityScope](Remove-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](Remove-CMSecurityScopeFromAdministrativeUser.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)


