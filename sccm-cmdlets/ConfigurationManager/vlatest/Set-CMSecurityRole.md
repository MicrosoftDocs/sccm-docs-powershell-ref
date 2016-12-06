---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834018
schema: 2.0.0
ms.assetid: 0AE6E561-6C79-48D2-9C0E-EA161C1897C0
---

# Set-CMSecurityRole

## SYNOPSIS
Changes configuration settings of a security role.

## SYNTAX

### SetByValue (Default)
```
Set-CMSecurityRole -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMSecurityRole -Id <String> [-NewName <String>] [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSecurityRole -Name <String> [-NewName <String>] [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSecurityRole** cmdlet changes configuration settings of a security role.
You can use this cmdlet to change the name and description of a security role.

## EXAMPLES

### Example 1: Change the name of a security role by using an ID
```
PS C:\>Set-CMSecurityRole -Id "CM100003" -NewName "RTOperator02"
```

This command renames the security role that has the ID CM100003.
The command changes the name to RTOperator02.

### Example 2: Change the name of a security role by using a name
```
PS C:\>Set-CMSecurityRole -Name "SRole02" -NewName "RTOperator02"
```

This command renames the security role named SRole02.
The command changes the name to RTOperator02.

### Example 3: Change the name of a security role by using an object variable
```
PS C:\>$Srole = Get-CMSecurityRole -Id "CM100003"
PS C:\> Set-CMSecurityRole -Inputobject $Srole -NewName "RTOperator02"
```

The first command gets the security role that has the ID CM100003 and stores it in the $Srole variable.

The second command renames the security role for the object stored in $Srole.
The command changes the name to RTOperator02.

## PARAMETERS

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

### -Id
Specifies an array of IDs of security roles.

```yaml
Type: String
Parameter Sets: SetById
Aliases: RoleId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMSecurityRole** object.
To get a **CMSecurityRole** object, use the Get-CMSecurityRole cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of security roles.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: RoleName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the security role.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: False
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

[Copy-CMSecurityRole](./Copy-CMSecurityRole.md)

[Export-CMSecurityRole](./Export-CMSecurityRole.md)

[Get-CMSecurityRole](./Get-CMSecurityRole.md)

[Import-CMSecurityRole](./Import-CMSecurityRole.md)

[Remove-CMSecurityRole](./Remove-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](./Remove-CMSecurityRoleFromAdministrativeUser.md)


