---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833747
schema: 2.0.0
ms.assetid: CAC293F8-F168-4D53-8C74-E33A077BE0D1
---

# Add-CMSecurityScopeToAdministrativeUser

## SYNOPSIS
Adds a security scope to an administrative user or group in Configuration Manager.

## SYNTAX

### AddScopeToAdminByName_Name (Default)
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScopeName <String> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminById_Id
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScopeId <String> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminById_Name
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScopeId <String> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminById_Object
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScopeId <String> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByName_Object
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScopeName <String> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByName_Id
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScopeName <String> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByObject_Object
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScope <IResultObject> -AdministrativeUser <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByObject_Id
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScope <IResultObject> -AdministrativeUserId <Int32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddScopeToAdminByObject_Name
```
Add-CMSecurityScopeToAdministrativeUser -SecurityScope <IResultObject> -AdministrativeUserName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSecurityScopeToAdministrativeUser** cmdlet adds a security scope to an administrative user or administrative group in Microsoft System Center Configuration Manager.

For more information about security scopes, see [Configuring Security for Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=247225) on TechNet.

You can specify an administrative user or group by name or by ID or you can use the use the Get-CMAdministrativeUser cmdlet to obtain a user or group object.
You can specify a security scope to add by name or by ID or you can use the Get-CMSecurityScope cmdlet to obtain a security scope.

## EXAMPLES

### Example 1: Add a named security scope to a named administrative group
```
PS C:\>Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserName "Western Administrators" -SecurityScopeName "Scope22"
```

This command adds a security scope named Scope22 to an administrative group named Western Administrators.

### Example 2: Add a security scope to an administrative group by using an ID
```
PS C:\>Add-CMSecurityScopeToAdministrativeUser -AdministrativeUserId 345 -SecurityScopeId "SMS00067"
```

This command adds the security scope that has the ID SMS00067 to the administrative user that has the ID 345.

## PARAMETERS

### -AdministrativeUser
Specifies an administrative user or administrative group object.
To get an administrative user or administrative group object, use the Get-CMAdministrativeUser cmdlet.

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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
To obtain a security scope object, use the Get-CMSecurityScope cmdlet.

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
Parameter Sets: AddScopeToAdminById_Id, AddScopeToAdminById_Name, AddScopeToAdminById_Object
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

[Add-CMSecurityRoleToAdministrativeUser](./Add-CMSecurityRoleToAdministrativeUser.md)

[Get-CMAdministrativeUser](./Get-CMAdministrativeUser.md)

[Get-CMSecurityScope](./Get-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](./Remove-CMSecurityScopeFromAdministrativeUser.md)


