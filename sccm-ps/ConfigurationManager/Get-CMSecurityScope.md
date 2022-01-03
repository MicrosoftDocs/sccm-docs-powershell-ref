---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Get-CMSecurityScope
---

# Get-CMSecurityScope

## SYNOPSIS

Get a security scope.

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

Use this cmdlet to get one or more security scopes in Configuration Manager.
You can get a security scope by its name or ID.
If you don't provide any parameters, all security scopes are returned.

For more information on security scopes, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a security scope by name

This command gets the security scope named **Scope1**.

```powershell
Get-CMSecurityScope -Name "Scope1"
```

### Example 2: Get a security scope by using a wildcard

This command gets all security scope objects that have a name beginning with "Contoso".

```powershell
Get-CMSecurityScope -Name "Contoso*"
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

Specify the ID of a security scope to get. This value is the `CategoryID` property, for example `SMS00UNA` for the **Default** scope.

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

Specify the name of a security scope to get.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CategoryName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_SecuredCategory

### IResultObject#SMS_SecuredCategory

## NOTES

For more information on this return object and its properties, see [SMS_SecuredCategory server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_securedcategory-server-wmi-class).

## RELATED LINKS

[New-CMSecurityScope](New-CMSecurityScope.md)

[Remove-CMSecurityScope](Remove-CMSecurityScope.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)

[Get-CMObjectSecurityScope](Get-CMObjectSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](Remove-CMSecurityScopeFromAdministrativeUser.md)

[New-CMAdministrativeUserPermission](New-CMAdministrativeUserPermission.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
