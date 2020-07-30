---
description: Gets security roles.
external help file: AdminUI.PS.Rba.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSecurityRole
---

# Get-CMSecurityRole

## SYNOPSIS
Gets security roles.

## SYNTAX

### SearchByName (Default)
```
Get-CMSecurityRole [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSecurityRole -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSecurityRole** cmdlet gets one or more security roles in Microsoft System Center Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get all security roles
```
PS XYZ:\> Get-CMSecurityRole
```

This command gets all security roles in Configuration Manager.

### Example 2: Get a security role by using an ID
```
PS XYZ:\> Get-CMSecurityRole -Id "SMS000CR"
```

This command gets the security role that has the ID SMS000CR.

### Example 3: Get a security role by using a wildcard
```
PS XYZ:\> Get-CMSecurityRole -Name App*
```

This command gets all security roles that have a name that starts with App.

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
Specifies an array of IDs of security roles.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of security roles.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### IResultObject[]#SMS_Role

### IResultObject#SMS_Role

## NOTES

## RELATED LINKS

[Copy-CMSecurityRole](Copy-CMSecurityRole.md)

[Export-CMSecurityRole](Export-CMSecurityRole.md)

[Import-CMSecurityRole](Import-CMSecurityRole.md)

[Remove-CMSecurityRole](Remove-CMSecurityRole.md)

[Remove-CMSecurityRoleFromAdministrativeUser](Remove-CMSecurityRoleFromAdministrativeUser.md)

[Set-CMSecurityRole](Set-CMSecurityRole.md)


