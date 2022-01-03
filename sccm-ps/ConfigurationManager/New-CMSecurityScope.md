---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: New-CMSecurityScope
---

# New-CMSecurityScope

## SYNOPSIS

Create a security scope.

## SYNTAX

```
New-CMSecurityScope [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a security scope. Security scopes provide administrative users with access to securable objects.

For more information on security scopes, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a security scope

This command creates a security scope named **Scope1** with a description.

```powershell
New-CMSecurityScope -Name "Scope1" -Description "Custom scope"
```

## PARAMETERS

### -Description

Specify an optional description for the security scope.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CategoryDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Name

Specify a name for the security scope to create.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CategoryName

Required: True
Position: Named
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

### None

## OUTPUTS

### IResultObject#SMS_SecuredCategory

## NOTES

For more information on this return object and its properties, see [SMS_SecuredCategory server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_securedcategory-server-wmi-class).

## RELATED LINKS

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)

[Remove-CMSecurityScope](Remove-CMSecurityScope.md)

[Add-CMSecurityScopeToAdministrativeUser](Add-CMSecurityScopeToAdministrativeUser.md)

[Add-CMObjectSecurityScope](Add-CMObjectSecurityScope.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
