---
description: Removes the association between a security role and an administrative user.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMSecurityRoleFromAdministrativeUser
---

# Remove-CMSecurityRoleFromAdministrativeUser

## SYNOPSIS
Removes the association between a security role and an administrative user.

## SYNTAX

### RemoveRoleFromAdminByName_Name (Default)
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUserName <String> [-Force] -RoleName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminById_Object
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUser <IResultObject> [-Force] -RoleId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByName_Object
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUser <IResultObject> [-Force] -RoleName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByObject_Object
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUser <IResultObject> [-Force] -Role <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminById_Id
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUserId <Int32> [-Force] -RoleId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByName_Id
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUserId <Int32> [-Force] -RoleName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByObject_Id
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUserId <Int32> [-Force] -Role <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminById_Name
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUserName <String> [-Force] -RoleId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveRoleFromAdminByObject_Name
```
Remove-CMSecurityRoleFromAdministrativeUser -AdministrativeUserName <String> [-Force] -Role <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSecurityRoleFromAdministrativeUser** cmdlet removes the association between one or more security roles and an administrative user.
After you remove the association of a security role with an administrative user, the administrative user cannot view the objects in Configuration Manager that are associated with the security role, and no longer has the permission to perform the tasks that are related to those objects.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

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

### -Role
Specifies a **CMSecurityRole** object.
To obtain a **CMSecurityRole** object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveRoleFromAdminByObject_Object, RemoveRoleFromAdminByObject_Id, RemoveRoleFromAdminByObject_Name
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
Parameter Sets: RemoveRoleFromAdminById_Object, RemoveRoleFromAdminById_Id, RemoveRoleFromAdminById_Name
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
Parameter Sets: RemoveRoleFromAdminByName_Name, RemoveRoleFromAdminByName_Object, RemoveRoleFromAdminByName_Id
Aliases:

Required: True
Position: Named
Default value: None
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

[Add-CMSecurityRoleToAdministrativeUser](Add-CMSecurityRoleToAdministrativeUser.md)

[Copy-CMSecurityRole](Copy-CMSecurityRole.md)

[Export-CMSecurityRole](Export-CMSecurityRole.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Import-CMSecurityRole](Import-CMSecurityRole.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)


