---
author: aczechowski
description: Removes a security scope from a Configuration Manager object.
external help file: AdminUI.PS.Common.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMObjectSecurityScope
titleSuffix: Configuration Manager
---

# Remove-CMObjectSecurityScope

## SYNOPSIS
Removes a security scope from a Configuration Manager object.

## SYNTAX

### ByValue (Default)
```
Remove-CMObjectSecurityScope [-Force] -InputObject <IResultObject[]> [-Scope] <IResultObject[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMObjectSecurityScope [-Force] -Id <String> -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMObjectSecurityScope [-Force] -InputObject <IResultObject[]> [-Name] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMObjectSecurityScope** cmdlet removes a security scope from a Microsoft System Center Configuration Manager object.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a security scope from application objects by using the pipeline
```
PS XYZ:\> $Scope = Get-CMSecurityScope -Name "Scope1"
PS XYZ:\> Get-CMApplication -Name "Application*" | Remove-CMObjectSecurityScope -Scope $Scope -Force
```

The first command gets the security scope object named Scope1 and stores the object in the $Scope variable.

The second command gets all application objects that have a name that begins with Application and uses the pipeline operator to pass the objects to **Remove-CMObjectSecurityScope**.
**Remove-CMObjectSecurityScope** removes the security scope stored in $Scope from each of the application objects.
The *Force* parameter indicates that the user is not prompted before the security scope is removed.

### Example 2: Remove a security scope from application objects
```
PS XYZ:\> Remove-CMObjectSecurityScope -InputObject (Get-CMApplication -Name "Application*") -Name "Scope1" -Force
```

This command gets all application objects that have a name beginning with Application and removes the security scope named Scope1 from each application object.
The *Force* parameter indicates that the user is not prompted before the security scope is removed.

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
Specifies the ID of a security scope.

```yaml
Type: String
Parameter Sets: ById
Aliases: SecurityScopeId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an array of Configuration Manager objects associated with a security scope.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a security scope.

```yaml
Type: String
Parameter Sets: ByName
Aliases: SecurityScopeName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Specifies an array of security scopes.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: SecurityScope, SecuredCategory, Scopes, SecurityScopes, SecuredCategories

Required: True
Position: 0
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMObjectSecurityScope](Add-CMObjectSecurityScope.md)

[Get-CMObjectSecurityScope](Get-CMObjectSecurityScope.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[Set-CMObjectSecurityScope](Set-CMObjectSecurityScope.md)


