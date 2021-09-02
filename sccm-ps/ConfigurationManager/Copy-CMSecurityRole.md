---
description: Creates a custom security role.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Copy-CMSecurityRole
---

# Copy-CMSecurityRole

## SYNOPSIS
Creates a custom security role.

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
The **Copy-CMSecurityRole** cmdlet creates a new security role by using an existing security role as a template.
Configuration Manager provides several built-in security roles.
If you require additional security roles, you can create a custom security role by creating a copy of an existing security role, and then modifying the copy.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Copy a security role by using an ID
```
PS XYZ:\>Copy-CMSecurityRole -Name "SecRole02" -SourceRoleId "SMS000CR"
```

This command creates a new security role named SecRole02 by copying the security role that has the ID SMS000CR.

### Example 2: Copy a security role by using a name
```
PS XYZ:\>Copy-CMSecurityRole -Name "SecRole02" -SourceRoleName "Software Update Manager"
```

This command creates a new security role named SecRole02 by copying the security role named Software Update Manager.

### Example 3: Copy a security role
```
PS XYZ:\> $Srole = Get-CMSecurityRole -Name "Software Update Manager"
PS XYZ:\> Copy-CMSecurityRole -InputObject $Srole -Name "SecRole02"
```

The first command gets the security role named Software Update Manager and stores it in the $Srole variable.

The second command creates a new security role named SecRole02 by copying the object stored in $Srole.

## PARAMETERS

### -Description
Specifies the description of a security role.

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
Specifies a **CMSecurityRole** object.
To obtain a **CMSecurityRole** object, use the [Get-CMSecurityRole](Get-CMSecurityRole.md) cmdlet.

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
Specifies a name for the new security scope.

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
Specifies the ID of a security role.

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
Specifies the name of a security role.

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

[Remove-CMSecurityRoleFromAdministrativeUser](Remove-CMSecurityRoleFromAdministrativeUser.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)


