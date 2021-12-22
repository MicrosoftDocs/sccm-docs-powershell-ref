---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
online version:
schema: 2.0.0
---

# Get-CMSecurityRolePermission

## SYNOPSIS

Get the permissions for the specified security role.

## SYNTAX

### SearchByName (Default)
```
Get-CMSecurityRolePermission -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMSecurityRolePermission -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMSecurityRolePermission -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the permissions for the specified security role. For more information on security roles and permissions, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

If your account doesn't have permissions to view security roles in the site, this cmdlet returns no results.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get permissions for a specific role

This example first gets an object for the built-in security role **Application author** in the variable **$role**. It then passes that object to the **Get-CMSecurityRolePermission** cmdlet, and saves the list of permissions in the **$rolePermission** variable.

```powershell
$roleName = "Application author"
$role = Get-CMSecurityRole -Name $roleName
$rolePermission = $role | Get-CMSecurityRolePermission
```

### Example 2: View classes for a specific role

This example is similar to the previous example, but filters and sorts the results differently. It only displays the class names to which the role has permissions, and sorts the list alphabetically.

```powershell
$rolePermission | Select-Object ObjectTypeDisplayName | Sort-Object -Property ObjectTypeDisplayName
```

## PARAMETERS

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

### -Id

Specify the ID of the security role to get its permissions. This value is the `RoleID` property, for example `SMS000AR` for the **OS Deployment Manager** role.

To view all roles and IDs for the site, use the following command:

```powershell
Get-CMSecurityRole | Select-Object RoleID, RoleName
```

```yaml
Type: String
Parameter Sets: SearchById
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a security role object to get its permissions. To get this object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: SecurityRole

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the security role to get its permissions.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#RoleOperation

### IResultObject#RoleOperation

## NOTES

The return object is the `RoleOperation` class, which includes an instance of the `SMS_ARoleOperation` class. For more information, see [SMS_ARoleOperation server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_aroleoperation-server-wmi-class).

## RELATED LINKS

[Set-CMSecurityRolePermission](Set-CMSecurityRolePermission.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
