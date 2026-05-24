---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
online version:
schema: 2.0.0
---

# New-CMAdministrativeUserPermission

## SYNOPSIS

Create a permissions object to assign to an administrative user.

## SYNTAX

### ByValue (Default)
```
New-CMAdministrativeUserPermission [-Collection <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] -InputObject <IResultObject> [-SecurityScope <IResultObject[]>]
 [-SecurityScopeId <String[]>] [-SecurityScopeName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
New-CMAdministrativeUserPermission [-Collection <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] -RoleId <String> [-SecurityScope <IResultObject[]>] [-SecurityScopeId <String[]>]
 [-SecurityScopeName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
New-CMAdministrativeUserPermission [-Collection <IResultObject[]>] [-CollectionId <String[]>]
 [-CollectionName <String[]>] -RoleName <String> [-SecurityScope <IResultObject[]>]
 [-SecurityScopeId <String[]>] [-SecurityScopeName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a permissions object to assign to an administrative user in Configuration Manager. Permissions can include security roles, security scopes, or collections. An _administrative user_ in Configuration Manager defines a local or domain user or group. For more information about security roles, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

Use this permissions object with the [New-CMAdministrativeUser](New-CMAdministrativeUser.md) cmdlet and its **Permission** parameter.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example creates an object that defines the following permissions:

- Security role: **Read-only Analyst**
- Security scope: **Scope1**
- Collection: **All Systems**

It then creates a new administrative user for **contoso\jqpublic** and assigns these permissions.
The last command displays the new user's permissions.

```powershell
$accountName = "contoso\jqpublic"
$roleName = "Read-only Analyst"
$scopeName = "Scope1"
$collectionName = "All Systems"

$role = Get-CMSecurityRole -Name $roleName
$scope = Get-CMSecurityScope -Name $scopeName
$collection = Get-CMCollection -Name $collectionName

$perms = New-CMAdministrativeUserPermission -RoleName $role.RoleName -SecurityScopeNames $scope.CategoryName -CollectionNames $collection.Name

$User = New-CMAdministrativeUser -Name $accountName -Permission $perms
$User.Permissions
```

## PARAMETERS

### -Collection

Specify an array of collection objects to add to the permissions. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Collections

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specify an array of collection IDs to add to the permissions. This value is the **CollectionID** property, for example, `SMS00001`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CollectionIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify an array of collection names to add to the permissions.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: CollectionNames

Required: False
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

Specify a security role object to add to the permissions. To get this object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Role

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RoleId

Specify the ID of a security role to add to the permissions. This value is the `RoleID` property, for example `SMS000AR` for the **OS Deployment Manager** role.

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName

Specify the name of a security role to add to the permissions.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScope

Specify a security scope object to add to the permissions. To get this object, use the [Get-CMSecurityScope](Get-CMSecurityScope.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: SecurityScopes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeId

Specify the ID of a security scope to add to the permissions. This value is the `CategoryID` property, for example `SMS00UNA` for the **Default** scope.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SecurityScopeIds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeName

Specify the name of a security scope to add to the permissions.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: SecurityScopeNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_APermission

## NOTES

For more information on this return object and its properties, see [SMS_APermission server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_apermission-server-wmi-class).

## RELATED LINKS

[New-CMAdministrativeUser](New-CMAdministrativeUser.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
