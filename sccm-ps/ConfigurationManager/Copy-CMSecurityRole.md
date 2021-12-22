---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Copy-CMSecurityRole
---

# Copy-CMSecurityRole

## SYNOPSIS

Create a custom security role.

## SYNTAX

### CopyFromId (Default)
```
Copy-CMSecurityRole [-Description <String>] -Name <String> -SourceRoleId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CopyFromName
```
Copy-CMSecurityRole [-Description <String>] -Name <String> -SourceRoleName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### CopyFromValue
```
Copy-CMSecurityRole [-Description <String>] -InputObject <IResultObject> -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a new security role by using an existing security role as a template. Configuration Manager provides several built-in security roles.
If you require additional security roles, you can create a custom security role by creating a copy of an existing security role, and then modifying the copy.

For more information on security roles and permissions, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Copy a security role by using an ID

This command creates a new security role named **SecRole02**. It copies the security role with ID `SMS000CR`, which is the **Software Update Manager** role.

```powershell
Copy-CMSecurityRole -Name "SecRole02" -SourceRoleId "SMS000CR"
```

## PARAMETERS

### -Description

Specify an optional description for the security role.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RoleDescription

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

Specify a security role object to copy. To get this object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: CopyFromValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify a name for the new security role.

```yaml
Type: String
Parameter Sets: (All)
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRoleId

Specify the ID of the security role to copy. This value is the `RoleID` property, for example `SMS000AR` for the **OS Deployment Manager** role.

```yaml
Type: String
Parameter Sets: CopyFromId
Aliases: CopiedFromId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRoleName

Specify the name of the security role to copy.

```yaml
Type: String
Parameter Sets: CopyFromName
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

[Export-CMSecurityRole](Export-CMSecurityRole.md)

[Get-CMSecurityRole](Get-CMSecurityRole.md)

[Import-CMSecurityRole](Import-CMSecurityRole.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)

[Add-CMSecurityRoleToAdministrativeUser](Add-CMSecurityRoleToAdministrativeUser.md)

[Set-CMSecurityRolePermission](Set-CMSecurityRolePermission.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
