---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Get-CMSecurityRole
---

# Get-CMSecurityRole

## SYNOPSIS

Get security roles.

## SYNTAX

### SearchByName (Default)
```
Get-CMSecurityRole [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSecurityRole -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more security roles from the Configuration Manager site. For more information on security roles and permissions, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

If your account doesn't have permissions to view security roles in the site, this cmdlet returns no results.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all security roles

This example lists all roles and IDs for the site.

```powershell
Get-CMSecurityRole | Select-Object RoleID, RoleName
```

### Example 2: Get a security role by using a wildcard

This command gets all security roles that have a name that starts with App.

```powershell
Get-CMSecurityRole -Name "App*"
```

### Example 3: List all custom security roles

This command returns all security roles that aren't built-in.

```powershell
Get-CMSecurityRole | Where-Object { $_.IsBuiltIn -eq $false }
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

Specify the ID of the security role to get. This value is the `RoleID` property, for example `SMS000AR` for the **OS Deployment Manager** role.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the security role to get.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: RoleName

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

### IResultObject[]#SMS_Role

### IResultObject#SMS_Role

## NOTES

For more information on this return object and its properties, see [SMS_Role server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_role-server-wmi-class).

## RELATED LINKS

[Copy-CMSecurityRole](Copy-CMSecurityRole.md)

[Export-CMSecurityRole](Export-CMSecurityRole.md)

[Import-CMSecurityRole](Import-CMSecurityRole.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)

[Add-CMSecurityRoleToAdministrativeUser](Add-CMSecurityRoleToAdministrativeUser.md)

[Get-CMSecurityRolePermission](Get-CMSecurityRolePermission.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
