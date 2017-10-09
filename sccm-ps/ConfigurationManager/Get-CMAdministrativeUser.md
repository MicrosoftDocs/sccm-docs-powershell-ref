---
external help file: AdminUI.PS.Rba.dll-Help.xml
ms.assetid: E10E2966-E438-49C0-A115-868CEDE6D8BB
online version: https://go.microsoft.com/fwlink/?linkid=834069
schema: 2.0.0
---

# Get-CMAdministrativeUser

## SYNOPSIS
Gets an administrative user.

## SYNTAX

### SearchByName (Default)
```
Get-CMAdministrativeUser [-Name <String>] [-RoleName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAdministrativeUser -Id <String> [-RoleName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAdministrativeUser** cmdlet gets one or more administrative users in Microsoft System Center Configuration Manager.
An administrative user has a defined set of permissions and may be a member of one or more scopes or roles.

## EXAMPLES

### Example 1: Get all the administrative users
```
PS C:\> Get-CMAdministrativeUser
```

This command gets all administrative users.

### Example 2: Get administrative user by name
```
PS C:\> Get-CMAdministrativeUser -Name "testDomain\myAdminUser"
```

This command gets the administrative user named AdminUser1.

## PARAMETERS

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

### -Name
Specifies the name of the administrative user in the form \<domain\>\\\<user\>.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: DisplayName, LogonName, UserName

Required: False
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
Parameter Sets: (All)
Aliases: RoleNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMAdministrativeUser](New-CMAdministrativeUser.md)

[Remove-CMAdministrativeUser](Remove-CMAdministrativeUser.md)


