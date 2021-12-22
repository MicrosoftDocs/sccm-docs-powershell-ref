---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: New-CMAdministrativeUser
---

# New-CMAdministrativeUser

## SYNOPSIS

Create an administrative user.

## SYNTAX

### New
```
New-CMAdministrativeUser [-CollectionName <String[]>] -Name <String> -RoleName <String[]>
 [-SecurityScopeName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### Advanced
```
New-CMAdministrativeUser -Name <String> -Permission <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an administrative user for Configuration Manager. An _administrative user_ in Configuration Manager defines a local or domain user or group. When you create the administrative user in Configuration Manager, you can give it access to security roles, security scopes, and collections. For more information about security roles, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add an administrative user

This command adds the Contoso domain user named **AdminUser1** as an administrative user.
It adds this user to the **Application Administrator** and **Software Update Manager** built-in security roles.
The command also adds the user to the **scope1** and **scope2** security scopes, and to the **userCollection1** and **deviceCollection1** collections.

```powershell
$name = "Contoso\AdminUser1"
$roles = "Application Administrator","Software Update Manager"
$scopes = "scope1","scope2"
$colls = "userCollection1","deviceCollection1"

New-CMAdministrativeUser -Name $name -RoleName $roles -SecurityScopeName $scopes -CollectionName $colls
```

### Example 2: Add a domain group

This example adds the Contoso domain group **Security Analysts** to the built-in **Read-only Analyst** security role.

```powershell
New-CMAdministrativeUser -Name "Contoso\Security Analysts" -RoleName "Read-only Analyst"
```

## PARAMETERS

### -CollectionName

Specify an array of collection names. The cmdlet assigns the new administrative user to each of these collections.

```yaml
Type: String[]
Parameter Sets: New
Aliases:

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

Specify the name of the administrative user to add. Use the format `domain\name`, where `name` is either the user or the group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogonName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Permission

Specify an array of permissions objects to assign to this new user. To get these objects, use the [New-CMAdministrativeUserPermission](New-CMAdministrativeUserPermission.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: Advanced
Aliases: Permissions

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName

Specify an array of security role names. This name can be for a built-in or custom role. To see the list of built-in security roles, see [Security roles](/mem/configmgr/core/understand/fundamentals-of-role-based-administration#security-roles).

```yaml
Type: String[]
Parameter Sets: New
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeName

Specify an array of security scope names.
A security scope name can be "Default" or the name of a custom security scope.
The cmdlet assigns the security scopes that you specify to the administrative user.

```yaml
Type: String[]
Parameter Sets: New
Aliases:

Required: False
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

### IResultObject#SMS_Admin

## NOTES

For more information on this return object and its properties, see [SMS_Admin server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_admin-server-wmi-class).

## RELATED LINKS

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Remove-CMAdministrativeUser](Remove-CMAdministrativeUser.md)

[New-CMAdministrativeUserPermission](New-CMAdministrativeUserPermission.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
