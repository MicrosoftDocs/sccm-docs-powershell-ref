---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Add-CMSecurityRoleToAdministrativeUser
---

# Add-CMSecurityRoleToAdministrativeUser

## SYNOPSIS

Add a security role to a user or group.

## SYNTAX

### AddRoleToAdminByName_Name (Default)
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName <String> -RoleName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Object
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUser <IResultObject> -RoleId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByName_Object
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUser <IResultObject> -RoleName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Object
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUser <IResultObject> -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Id
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserId <Int32> -RoleId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByName_Id
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserId <Int32> -RoleName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Id
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserId <Int32> -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Name
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName <String> -RoleId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Name
```
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName <String> -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add a security role to an administrative user or administrative group in Configuration Manager.

Permissions defined in a role represent object types and actions available for each object type.
Configuration Manager provides some built-in security roles.
You can also create custom security roles.
For more information about security roles, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

You can specify an administrative user or group by name or by ID or you can use the use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet to get a user or group object. An _administrative user_ in Configuration Manager defines a local or domain user or group.
You can specify a role to add by name or by ID, or you can use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet to get a role.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add custom security role to a domain user group

This command adds the custom security role **SecurityRole17** for the domain group **Western Administrators**. This command assumes that you already created the custom security role and the administrative user.

```powershell
Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName "Contoso\Western Administrators " -RoleName "SecurityRole17"
```

## PARAMETERS

### -AdministrativeUser

Specify an administrative user object to configure. To get this object, use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddRoleToAdminById_Object, AddRoleToAdminByName_Object, AddRoleToAdminByObject_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AdministrativeUserId

Specify the ID of the administrative user to configure. This value is the `AdminID` property, which is an integer value. For example, `16777234`.

```yaml
Type: Int32
Parameter Sets: AddRoleToAdminById_Id, AddRoleToAdminByName_Id, AddRoleToAdminByObject_Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeUserName

Specify the name of the administrative user to configure.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: AddRoleToAdminByName_Name, AddRoleToAdminById_Name, AddRoleToAdminByObject_Name
Aliases:

Required: True
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

### -InputObject

Specify a security role object to add. To get this object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddRoleToAdminByObject_Object, AddRoleToAdminByObject_Id, AddRoleToAdminByObject_Name
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleId

Specify the ID of the security role to add. This value is the `RoleID` property, for example `SMS000AR` for the **OS Deployment Manager** role.

```yaml
Type: String
Parameter Sets: AddRoleToAdminById_Object, AddRoleToAdminById_Id, AddRoleToAdminById_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName

Specify the name of the security role to add.

```yaml
Type: String
Parameter Sets: AddRoleToAdminByName_Name, AddRoleToAdminByName_Object, AddRoleToAdminByName_Id
Aliases:

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Remove-CMSecurityRoleFromAdministrativeUser](Remove-CMSecurityRoleFromAdministrativeUser.md)

[Add-CMSecurityScopeToAdministrativeUser](Add-CMSecurityScopeToAdministrativeUser.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
