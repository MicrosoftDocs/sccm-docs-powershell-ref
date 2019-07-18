---
external help file: AdminUI.PS.Rba.dll-Help.xml
ms.assetid: 2DF67D4D-B111-4F6B-956A-EB72BCA1EEDC
online version: https://go.microsoft.com/fwlink/?linkid=834228
schema: 2.0.0
---

# New-CMAdministrativeUser

## SYNOPSIS
Creates an administrative user.

## SYNTAX

```
New-CMAdministrativeUser -Name <String> -RoleName <String[]> [-SecurityScopeName <String[]>]
 [-CollectionName <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAdministrativeUser** cmdlet creates an administrative user for Microsoft System Center Configuration Manager.
At the same time that you create the administrative user account, you can give the new administrative user access to collections of Configuration Manager resources.
You can also define the types of access that the new administrative user has to each collection by assigning security roles to the user.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Add an administrative user
```
PS XYZ:\> New-CMAdministrativeUser -Name "Consoto\AdminUser1" -RoleName "Application Administrator","Software Update Manager" -SecurityScopeName "scope1","scope2" -CollectionName "userCollection1","deviceCollection1"
```

This command adds the user named AdminUser1 as an administrative user to the Application Administrator and Software Update Manager security roles.
The command also adds admin1 to the security scopes named scope1 and scope 2, and to the collections userCollection1 and deviceCollection1.

## PARAMETERS

### -CollectionName
Specifies an array of collection names.
The cmdlet assigns the new administrative user to each of these collections.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
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

### -Name
Specifies the name of the administrative user in the form \<domain\>\\\<user\>.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LogonName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
Specifies an array of names for the roles that you assign to an administrative user.
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
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityScopeName
Specifies an array of names of security scopes.
A security scope name can be "Default" or the name of a custom security scope.
The cmdlet assigns the security scopes that you specify to the administrative user.

```yaml
Type: String[]
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

[Get-CMAdministrativeUser](Get-CMAdministrativeUser.md)

[Remove-CMAdministrativeUser](Remove-CMAdministrativeUser.md)


