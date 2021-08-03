---
description: Removes the association between security scopes and an administrative user.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMSecurityScopeFromAdministrativeUser
---

# Remove-CMSecurityScopeFromAdministrativeUser

## SYNOPSIS
Removes the association between security scopes and an administrative user.

## SYNTAX

### RemoveScopeFromAdminByName_Name (Default)
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserName <String> [-Force]
 -SecurityScopeName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveScopeFromAdminById_Object
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUser <IResultObject> [-Force]
 -SecurityScopeId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveScopeFromAdminByName_Object
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUser <IResultObject> [-Force]
 -SecurityScopeName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveScopeFromAdminByObject_Object
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUser <IResultObject> [-Force]
 -SecurityScope <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveScopeFromAdminById_Id
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserId <Int32> [-Force] -SecurityScopeId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminByName_Id
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserId <Int32> [-Force] -SecurityScopeName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveScopeFromAdminByObject_Id
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserId <Int32> [-Force]
 -SecurityScope <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveScopeFromAdminById_Name
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserName <String> [-Force]
 -SecurityScopeId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveScopeFromAdminByObject_Name
```
Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserName <String> [-Force]
 -SecurityScope <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSecurityScopeFromAdministrativeUser** cmdlet removes the association between one or more security scopes and an administrative user.

After you remove the association between a security scope and an administrative user, the administrative user cannot view the objects in Configuration Manager that are associated with the security scope, and no longer has the permission to perform the tasks that are related to those objects.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a security scope from an administrative user
```
PS XYZ:\> Remove-CMSecurityScopeFromAdministrativeUser -AdministrativeUserName "Contoso\PattiFuller" -SecurityScopeName "SecScope02"
```

This command removes the association between the security scope named SecScope02 and the administrative user named Contoso\PattiFuller.

## PARAMETERS

### -AdministrativeUser
Specifies a **CMAdministrativeUser** object.
To obtain a **CMAdministrativeUser** object, use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveScopeFromAdminById_Object, RemoveScopeFromAdminByName_Object, RemoveScopeFromAdminByObject_Object
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
Parameter Sets: RemoveScopeFromAdminById_Id, RemoveScopeFromAdminByName_Id, RemoveScopeFromAdminByObject_Id
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
Parameter Sets: RemoveScopeFromAdminByName_Name, RemoveScopeFromAdminById_Name, RemoveScopeFromAdminByObject_Name
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

### -SecurityScope
Specifies a security scope object.
To obtain a security scope object, use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveScopeFromAdminByObject_Object, RemoveScopeFromAdminByObject_Id, RemoveScopeFromAdminByObject_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SecurityScopeId
Specifies the ID of a security scope.

```yaml
Type: String
Parameter Sets: RemoveScopeFromAdminById_Object, RemoveScopeFromAdminById_Id, RemoveScopeFromAdminById_Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeName
Specifies the name of a security scope.
A security scope name can be Default or the name of a custom security scope.

```yaml
Type: String
Parameter Sets: RemoveScopeFromAdminByName_Name, RemoveScopeFromAdminByName_Object, RemoveScopeFromAdminByName_Id
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

[Add-CMSecurityScopeToAdministrativeUser](Add-CMSecurityScopeToAdministrativeUser.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[New-CMSecurityScope](New-CMSecurityScope.md)

[Remove-CMSecurityScope](Remove-CMSecurityScope.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)


