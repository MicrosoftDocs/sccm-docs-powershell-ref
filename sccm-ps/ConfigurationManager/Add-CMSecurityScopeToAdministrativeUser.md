---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Add-CMSecurityScopeToAdministrativeUser
---

# Add-CMSecurityScopeToAdministrativeUser

## SYNOPSIS

Add a security scope to a user or group.

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

Use this cmdlet to add a security scope to an administrative user or administrative group in Configuration Manager.

For more information about security scopes, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

You can specify an administrative user or group by name or by ID or you can use the use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet to obtain a user or group object. An _administrative user_ in Configuration Manager defines a local or domain user or group.
You can specify a security scope to add by name or by ID or you can use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet to obtain a security scope.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a custom security scope to a domain user group

This command adds a security scope named **Scope22** for a domain group named **Western Administrators**. This command assumes that you already created the custom security scope and the administrative user.

```powershell
Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserName "Contoso\Western Administrators" -SecurityScopeName "Scope22"
```

## PARAMETERS

### -AdministrativeUser

Specify an administrative user object to configure. To get this object, use the [Get-CMAdministrativeUser](Get-CMAdministrativeUser.md) cmdlet.

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

Specify the ID of the administrative user to configure. This value is the `AdminID` property, which is an integer value. For example, `16777234`.

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

Specify the name of the administrative user to configure.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

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

### -SecurityScope

Specify a security scope object to add. To get this object, use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.

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

Specify the ID of the security scope to add. This value is the `CategoryID` property, for example `SMS00UNA` for the **Default** scope.

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

Specify the name of the security scope to add.

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

[Remove-CMSecurityScopeFromAdministrativeUser](Remove-CMSecurityScopeFromAdministrativeUser.md)

[Add-CMSecurityRoleToAdministrativeUser](Add-CMSecurityRoleToAdministrativeUser.md)

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Get-CMSecurityScope](Get-CMSecurityScope.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
