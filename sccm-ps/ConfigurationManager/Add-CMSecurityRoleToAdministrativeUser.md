---
description: Adds a security role to an administrative user or group in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMSecurityRoleToAdministrativeUser
---

# Add-CMSecurityRoleToAdministrativeUser

## SYNOPSIS
Adds a security role to an administrative user or group in Configuration Manager.

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
The **Add-CMSecurityRoleToAdministrativeUser** cmdlet adds a security role to an administrative user or administrative group in Configuration Manager.

Permissions defined in a role represent object types and actions available for each object type.
Configuration Manager provides some built-in security roles.
You can also create custom security roles.
For more information about security roles, see [Configuring Security for Configuration Manager](/mem/configmgr/core/plan-design/security/configure-security).

You can specify an administrative user or group by name or by ID or you can use the use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet to obtain a user or group object.
You can specify a role to add by name or by ID, or you can use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet to obtain a role.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a named role to a named user group
```
PS XYZ:\>Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName "Western Administrators " -RoleName "SecurityRole17"
```

This command adds a security role named SecurityRole17 to the administrative group named Western Administrators.

### Example 2: Add a role to a named user group identified by using an ID
```
PS XYZ:\>Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName "Western Administrators" -RoleId "SMS38973"
```

This command adds a security role that has the specified ID to the administrative group named Western Administrators.

## PARAMETERS

### -AdministrativeUser
Specifies an administrative user or administrative group object.
To obtain an administrative user or administrative group object, use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet.

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
Specifies an ID of an administrative user or administrative group.

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
Specifies a name of an administrative user or administrative group.

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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

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
Specifies an ID of a role.
A role represents Configuration Manager permissions granted to a user.

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
Specifies a name of a role.
A role represents Configuration Manager permissions granted to a user.

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

[Add-CMSecurityScopeToAdministrativeUser](Add-CMSecurityScopeToAdministrativeUser.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](Remove-CMSecurityRoleFromAdministrativeUser.md)


