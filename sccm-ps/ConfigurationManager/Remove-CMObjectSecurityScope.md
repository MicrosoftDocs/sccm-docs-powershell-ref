---
description: Removes a security scope from a Configuration Manager object.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMObjectSecurityScope
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
The **Remove-CMObjectSecurityScope** cmdlet removes a security scope from a Configuration Manager object.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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

### Example 3: Add a new security scope then remove all others from application object

```powershell
#Get Desired Security Scope
$ScopeName = "Team ABC"
$TeamABCScope = Get-CMSecurityScope | Where-Object {$_.CategoryName -eq $ScopeName}

#Get Object to add scope too
$Application = Get-CMApplication -Name "Edge Enterprise Stable"

#Add Scope to object
Add-CMObjectSecurityScope -InputObject $Application -Scope $TeamABCScope

#Get Scopes on Application that're are NOT the one you just added, then cycle through and remove.
foreach ($ExtraScope in (Get-CMObjectSecurityScope -InputObject $Application | Where-Object {$_.CategoryName -ne $ScopeName}))
    {
    Remove-CMObjectSecurityScope -InputObject $Application -Scope $ExtraScope -Force
    }
```

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMObjectSecurityScope](Add-CMObjectSecurityScope.md)

[Get-CMObjectSecurityScope](Get-CMObjectSecurityScope.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[Set-CMObjectSecurityScope](Set-CMObjectSecurityScope.md)


