---
description: Adds a security scope to an administrative user or group in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMSecurityScopeToAdministrativeUser
---

# Add-CMSecurityScopeToAdministrativeUser

## SYNOPSIS
Adds a security scope to an administrative user or group in Configuration Manager.

## SYNTAX

### AddScopeToAdminByName_Name (Default)
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserName <String> -SecurityScopeName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminById_Object
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUser <IResultObject> -SecurityScopeId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByName_Object
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUser <IResultObject> -SecurityScopeName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByObject_Object
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUser <IResultObject> -SecurityScope <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminById_Id
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserId <Int32> -SecurityScopeId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByName_Id
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserId <Int32> -SecurityScopeName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByObject_Id
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserId <Int32> -SecurityScope <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminById_Name
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserName <String> -SecurityScopeId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByObject_Name
```
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserName <String> -SecurityScope <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSecurityScopeToAdministrativeUser** cmdlet adds a security scope to an administrative user or administrative group in Configuration Manager.

For more information about security scopes, see [Configuring Security for Configuration Manager](/mem/configmgr/core/plan-design/security/configure-security).

You can specify an administrative user or group by name or by ID or you can use the use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet to obtain a user or group object.
You can specify a security scope to add by name or by ID or you can use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet to obtain a security scope.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a named security scope to a named administrative group
```
PS XYZ:\>Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserName "Western Administrators" -SecurityScopeName "Scope22"
```

This command adds a security scope named Scope22 to an administrative group named Western Administrators.

### Example 2: Add a security scope to an administrative group by using an ID
```
PS XYZ:\>Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserId 345 -SecurityScopeId "SMS00067"
```

This command adds the security scope that has the ID SMS00067 to the administrative user that has the ID 345.

## PARAMETERS

### -AdministrativeUser
Specifies an administrative user or administrative group object.
To get an administrative user or administrative group object, use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddScopeToAdminById_Object, AddScopeToAdminByName_Object, AddScopeToAdminByObject_Object
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
Parameter Sets: AddScopeToAdminById_Id, AddScopeToAdminByName_Id, AddScopeToAdminByObject_Id
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
Parameter Sets: AddScopeToAdminByName_Name, AddScopeToAdminById_Name, AddScopeToAdminByObject_Name
Aliases:

Required: True
Position: Named
Default value: None
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

### -SecurityScope
Specifies a security scope object.
To obtain a security scope object, use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: AddScopeToAdminByObject_Object, AddScopeToAdminByObject_Id, AddScopeToAdminByObject_Name
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
Parameter Sets: AddScopeToAdminById_Object, AddScopeToAdminById_Id, AddScopeToAdminById_Name
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
Parameter Sets: AddScopeToAdminByName_Name, AddScopeToAdminByName_Object, AddScopeToAdminByName_Id
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Add-CMSecurityRoleToAdministrativeUser](Add-CMSecurityRoleToAdministrativeUser.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](Remove-CMSecurityScopeFromAdministrativeUser.md)


