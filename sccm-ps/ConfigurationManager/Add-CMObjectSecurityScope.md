---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Add-CMObjectSecurityScope
---

# Add-CMObjectSecurityScope

## SYNOPSIS

Add a security scope to an object.

## SYNTAX

### ByValue (Default)
```
Add-CMObjectSecurityScope -InputObject <IResultObject[]> [-Scope] <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Add-CMObjectSecurityScope -Id <String> -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMObjectSecurityScope -InputObject <IResultObject[]> [-Name] <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add a security scope to a Configuration Manager object.

For more information on security scopes, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a security scope to application objects

The first command creates a security scope object named **Scope1** and stores it in the **$Scope** variable.

The second command gets all application objects whose name begins with "Central". It then uses the pipeline operator to pass the objects to **Add-CMObjectSecurityScope**. This cmdlet adds the security scope to each application object.

```powershell
$Scope = New-CMSecurityScope -Name "Scope1" -Description "Security scope 1"
Get-CMApplication -Name "Central*" | Add-CMObjectSecurityScope -Scope $Scope
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

Specify the ID of a security scope to add to a Configuration Manager object. This value is the `CategoryID` property, for example `SMS00UNA` for the **Default** scope.

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

Specify an array of Configuration Manager objects to add the security scope. To get this object, use the **Get** cmdlet for the object type. For example, **Get-CMApplication** for app objects.

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

Specify the name of a security scope to add to a Configuration Manager object.

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

Specify an array of security scope objects to add. To get this object use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.

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

[Get-CMObjectSecurityScope](Get-CMObjectSecurityScope.md)

[Remove-CMObjectSecurityScope](Remove-CMObjectSecurityScope.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[Add-CMSecurityScopeToAdministrativeUser](Add-CMSecurityScopeToAdministrativeUser.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
