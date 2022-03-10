---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
online version:
schema: 2.0.0
---

# Set-CMSecurityRolePermission

## SYNOPSIS

Configure a security role with specific permissions.

## SYNTAX

### SearchByValue (Default)
```
Set-CMSecurityRolePermission -InputObject <IResultObject> -RolePermission <Hashtable>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Set-CMSecurityRolePermission -Id <String> -RolePermission <Hashtable> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Set-CMSecurityRolePermission -Name <String> -RolePermission <Hashtable> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure a security role with specific permissions. For more information on security roles and permissions, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets an object for the security role **Contoso custom role** in the variable **$role**. It then creates a hashtable of allowed operations, or permissions, in the **$ops** variable. These permissions include the following operations:

- Create and delete boundaries
- Read applications
- Modify alert subscriptions, including set security scope

The example then uses the **Set-CMSecurityRolePermission** cmdlet to set the specified permissions on the specified security role.

```powershell
$roleName = "Contoso custom role"
$role = Get-CMSecurityRole -Name $roleName

$ops = @{
  Boundaries = "Create,Delete";
  Application="Read";
  "Alert Subscription"="Modify,Set Security Scope"
}

$role | Set-CMSecurityRolePermission -RolePermission $ops
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

Specify the ID of the security role to configure its permissions. This value is the `RoleID` property, for example `SMS000AR` for the **OS Deployment Manager** role.

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

Specify a security role object to configure its permissions. To get this object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

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

Specify the name of the security role to configure its permissions.

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

### -RolePermission

Specify a [hashtable](/powershell/module/microsoft.powershell.core/about/about_hash_tables) of allowed operations, or permissions, for the target role. The first value of the hashtable is the class name, and the second value is an array of permission names.

For an example, see [Example 1](#examples).

```yaml
Type: Hashtable
Parameter Sets: (All)
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
Default value: None
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

[Get-CMSecurityRolePermission](Get-CMSecurityRolePermission.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
