---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Remove-CMSecurityScope
---

# Remove-CMSecurityScope

## SYNOPSIS

Remove a security scope.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSecurityScope [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMSecurityScope [-Force] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSecurityScope [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a security scope from Configuration Manager. You can only remove custom scopes.

For more information on security scopes, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a security scope in a variable

The first command gets the security scope object named **Scope1** and stores the object in the **$Scope** variable.

The second command removes the security scope stored in the variable.
With the **Force** parameter, you're not prompted for confirmation before the cmdlet runs.

```powershell
$Scope = Get-CMSecurityScope -Name "Scope1"

Remove-CMSecurityScope -InputObject $Scope -Force
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

Specify the ID of a security scope to remove. This value is the `CategoryID` property. Since this cmdlet only works with custom scopes, this value should always start with the site code. (IDs for built-in scopes start with `SMS`.)

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

### -InputObject

Specify a security scope object to remove. To get this object, use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.

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

Specify the name of a security scope to remove.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: CategoryName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[New-CMSecurityScope](New-CMSecurityScope.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](Remove-CMSecurityScopeFromAdministrativeUser.md)

[Remove-CMObjectSecurityScope](Remove-CMObjectSecurityScope.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
