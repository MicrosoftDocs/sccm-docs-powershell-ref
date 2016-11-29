---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833873
schema: 2.0.0
ms.assetid: FE92047B-B040-478C-B886-6C67FAD3A4E4
---

# Remove-CMAdministrativeUser

## SYNOPSIS
Removes an administrative user.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAdministrativeUser -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Remove-CMAdministrativeUser -Name <String> [-Force] [-RoleName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMAdministrativeUser [-Force] -Id <String> [-RoleName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAdministrativeUser** cmdlet removes one or more Microsoft System Center Configuration Manager administrative users.
When you remove an administrative user, Configuration Manager revokes the access of the administrative user to manage Configuration Manager.

## EXAMPLES

### Example 1: SearchByValueMandatory, pipeline
```
PS C:\>Get-CMAdministrativeUser -Name contoso\admin1 -RoleName "Application Administrator" | Remove-CMAdministrativeUser -Force
```

This command gets the administrative user object named AdminUser1 who is a member of the Application Administrator role and uses the pipeline operator to pass the object to **Remove-CMAdministrativeUser**, which removes the adminsitrative user.
Specifying the *Force* parameter indicates that the user is not prompted for confirmation prior to the user being removed.

### Example 2: SearchByName
```
PS C:\>Remove-CMAdministrativeUser -Name contoso\admin1 -RoleName "Application Administrator" -Force
```

This command removes the administrative user named AdminUser1 who is a member of the Application Administrator role.
Specifying the *Force* parameter indicates that the user is not prompted for confirmation prior to the user being removed.

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
Specifies the ID of an administrative user.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: AdminId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an administrative user object.
To obtain an administrative user object, use the Get-CMAdministrativeUser cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of administrative user names in the format of \<domain\>\\\<user\>.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: DisplayName, LogonName, UserName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Specifies an array of names of security roles.
Valid values are: 

- Application Administrator
- Application Author
- Application Deployment Manager
- Asset Manager
- Compliance Settings Manager
- Discovery Operator
- Endpoint Protection Manager
- Full Administrator
- Infrastructure Administrator
- Operating System Deployment Manager
- Operations Administrator
- Read-only Analyst
- Remote Tools Operator
- Security Administrator
- Software Update Manager
- Custom-defined security roles

```yaml
Type: String[]
Parameter Sets: SearchByName, SearchByIdMandatory
Aliases: RoleNames

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

[Get-CMAdministrativeUser](./Get-CMAdministrativeUser.md)

[New-CMAdministrativeUser](./New-CMAdministrativeUser.md)


