---
author: aczechowski
description: Removes the association between a security role and an administrative user.
external help file: AdminUI.PS.Rba.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMSecurityRoleFromAdministrativeUser
titleSuffix: Configuration Manager
---

# Remove-CMSecurityRoleFromAdministrativeUser

## SYNOPSIS
Removes the association between a security role and an administrative user.

## SYNTAX

### RemoveRoleFromAdminByName_Name (Default)
```
Remove-CMSecurityRoleFromAdministrativeUser -RoleName <String> -AdministrativeUserName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminById_Id
```
Remove-CMSecurityRoleFromAdministrativeUser -RoleId <String> -AdministrativeUserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminById_Name
```
Remove-CMSecurityRoleFromAdministrativeUser -RoleId <String> -AdministrativeUserName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminById_Object
```
Remove-CMSecurityRoleFromAdministrativeUser -RoleId <String> -AdministrativeUser <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByName_Id
```
Remove-CMSecurityRoleFromAdministrativeUser -RoleName <String> -AdministrativeUserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByName_Object
```
Remove-CMSecurityRoleFromAdministrativeUser -RoleName <String> -AdministrativeUser <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByObject_Id
```
Remove-CMSecurityRoleFromAdministrativeUser -Role <IResultObject> -AdministrativeUserId <Int32> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByObject_Name
```
Remove-CMSecurityRoleFromAdministrativeUser -Role <IResultObject> -AdministrativeUserName <String> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByObject_Object
```
Remove-CMSecurityRoleFromAdministrativeUser -Role <IResultObject> -AdministrativeUser <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSecurityRoleFromAdministrativeUser** cmdlet removes the association between one or more security roles and an administrative user.
After you remove the association of a security role with an administrative user, the administrative user cannot view the objects in Microsoft System Center Configuration Manager that are associated with the security role, and no longer has the permission to perform the tasks that are related to those objects.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove a security role from an administrative user
```
PS XYZ:\> Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUserName "Contoso\PattiFuller" -RoleName "Security Update Manager"
```

This command removes the association between the security role named Security Update Manager and the administrative user named Contoso\PattiFuller.

## PARAMETERS

### -AdministrativeUser
Specifies a **CMAdministrativeUser** object.
To obtain a **CMAdministrativeUser** object, use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveRoleFromAdminById_Object, RemoveRoleFromAdminByName_Object, RemoveRoleFromAdminByObject_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AdministrativeUserId
Specifies the ID of an administrative user.

```yaml
Type: Int32
Parameter Sets: RemoveRoleFromAdminById_Id, RemoveRoleFromAdminByName_Id, RemoveRoleFromAdminByObject_Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AdministrativeUserName
Specifies the name of an administrative user.

```yaml
Type: String
Parameter Sets: RemoveRoleFromAdminByName_Name, RemoveRoleFromAdminById_Name, RemoveRoleFromAdminByObject_Name
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

### -Role
Specifies a **CMSecurityRole** object.
To obtain a **CMSecurityRole** object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveRoleFromAdminByObject_Id, RemoveRoleFromAdminByObject_Name, RemoveRoleFromAdminByObject_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleId
Specifies the ID of a role.

```yaml
Type: String
Parameter Sets: RemoveRoleFromAdminById_Id, RemoveRoleFromAdminById_Name, RemoveRoleFromAdminById_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Specifies the name of a role.

```yaml
Type: String
Parameter Sets: RemoveRoleFromAdminByName_Name, RemoveRoleFromAdminByName_Id, RemoveRoleFromAdminByName_Object
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMSecurityRoleToAdministrativeUser](Add-CMSecurityRoleToAdministrativeUser.md)

[Copy-CMSecurityRole](Copy-CMSecurityRole.md)

[Export-CMSecurityRole](Export-CMSecurityRole.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Import-CMSecurityRole](Import-CMSecurityRole.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)


