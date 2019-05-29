---
title: Add-CMSecurityRoleToAdministrativeUser
titleSuffix: Configuration Manager
description: Adds a security role to an administrative user or group in Configuration Manager.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Add-CMSecurityRoleToAdministrativeUser

## SYNOPSIS
Adds a security role to an administrative user or group in Configuration Manager.

## SYNTAX

### AddRoleToAdminByName_Name (Default)
```
Add-CMSecurityRoleToAdministrativeUser -RoleName <String> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Id
```
Add-CMSecurityRoleToAdministrativeUser -RoleId <String> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Name
```
Add-CMSecurityRoleToAdministrativeUser -RoleId <String> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminById_Object
```
Add-CMSecurityRoleToAdministrativeUser -RoleId <String> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByName_Id
```
Add-CMSecurityRoleToAdministrativeUser -RoleName <String> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByName_Object
```
Add-CMSecurityRoleToAdministrativeUser -RoleName <String> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Id
```
Add-CMSecurityRoleToAdministrativeUser -InputObject <IResultObject> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Name
```
Add-CMSecurityRoleToAdministrativeUser -InputObject <IResultObject> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddRoleToAdminByObject_Object
```
Add-CMSecurityRoleToAdministrativeUser -InputObject <IResultObject> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSecurityRoleToAdministrativeUser** cmdlet adds a security role to an administrative user or administrative group in Microsoft System Center Configuration Manager.

Permissions defined in a role represent object types and actions available for each object type.
System Center Configuration Manager provides some built-in security roles.
You can also create custom security roles.
For more information about security roles, see [Configuring Security for Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=247225) on TechNet.

You can specify an administrative user or group by name or by ID or you can use the use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet to obtain a user or group object.
You can specify a role to add by name or by ID, or you can use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet to obtain a role.

## EXAMPLES

### Example 1: Add a named role to a named user group
```
PS C:\>Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName "Western Administrators " -RoleName "SecurityRole17"
```

This command adds a security role named SecurityRole17 to the administrative group named Western Administrators.

### Example 2: Add a role to a named user group identified by using an ID
```
PS C:\>Add-CMSecurityRoleToAdministrativeUser -AdministrativeUserName "Western Administrators" -RoleId "SMS38973"
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

### -InputObject
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: AddRoleToAdminByObject_Id, AddRoleToAdminByObject_Name, AddRoleToAdminByObject_Object
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
Parameter Sets: AddRoleToAdminById_Id, AddRoleToAdminById_Name, AddRoleToAdminById_Object
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
Parameter Sets: AddRoleToAdminByName_Name, AddRoleToAdminByName_Id, AddRoleToAdminByName_Object
Aliases: 

Required: True
Position: Named
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMSecurityScopeToAdministrativeUser](Add-CMSecurityScopeToAdministrativeUser.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](Remove-CMSecurityRoleFromAdministrativeUser.md)


