---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2021
schema: 2.0.0
title: Get-CMAdministrativeUser
---

# Get-CMAdministrativeUser

## SYNOPSIS

Get an administrative user.

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

Use this cmdlet to get one or more administrative users in Configuration Manager. An administrative user has a defined set of permissions and may be a member of one or more scopes or roles. An _administrative user_ in Configuration Manager defines a local or domain user or group. For more information about security roles, see [Fundamentals of role-based administration in Configuration Manager](/mem/configmgr/core/understand/fundamentals-of-role-based-administration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all administrative users

This command gets all administrative users. It displays the output as a table showing the account name (**LogonName**), security roles (**RoleNames**), security scopes (**CategoryNames**), and collections (**CollectionNames**).

```powershell
Get-CMAdministrativeUser | Select-Object LogonName, RoleNames, CategoryNames, CollectionNames
```

### Example 2: Get an administrative user by name

This command gets the administrative user named **jqpublic**.

```powershell
Get-CMAdministrativeUser -Name "Contoso\jqpublic"
```

### Example 3: Get all users with specific scope

This command gets all administrative users with the **Default** scope and displays the account names.

```powershell
Get-CMAdministrativeUser | Where-Object { $_.CategoryNames -contains "Default" } | Select-Object LogonName
```

### Example 4: Get all users with specific role

This command gets all administrative users with the **Full Administrator** role and displays the account names.

```powershell
Get-CMAdministrativeUser -RoleName "Full Administrator" | Select-Object LogonName
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

Specify the ID of the administrative user to get. This value is the `AdminID` property. It's an integer value, for example `16777234`.

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

Specify the name of the administrative user to get. For example, `domain\username` or `domain\groupname`

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: DisplayName, LogonName, UserName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -RoleName

Specify an array of security role names. This name can be for a built-in or custom role. To see the list of built-in security roles, see [Security roles](/mem/configmgr/core/understand/fundamentals-of-role-based-administration#security-roles).

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_Admin

### IResultObject#SMS_Admin

## NOTES

For more information on this return object and its properties, see [SMS_Admin server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_admin-server-wmi-class).

## RELATED LINKS

[New-CMAdministrativeUser](New-CMAdministrativeUser.md)

[Remove-CMAdministrativeUser](Remove-CMAdministrativeUser.md)

[New-CMAdministrativeUserPermission](New-CMAdministrativeUserPermission.md)

[Automate role-based administration with Windows PowerShell](/mem/configmgr/core/servers/deploy/configure/configure-role-based-administration#automate-with-windows-power-shell)
