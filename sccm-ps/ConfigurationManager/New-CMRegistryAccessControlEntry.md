---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
online version:
schema: 2.0.0
---

# New-CMRegistryAccessControlEntry

## SYNOPSIS

Create a registry key access control entry.

## SYNTAX

```
New-CMRegistryAccessControlEntry [-AccessOption <AccessType>] -GroupOrUserName <String>
 [-Permission <RegistryPermissions[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an access control entry (ACE) for a registry key. An access control entry defines specific permissions for a specific user or group. You can use this object with the **New-CMRequirementRuleRegistryKeyPermissionValue** cmdlet to create a requirement rule on an application deployment type that verifies registry key permissions.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a requirement rule for registry key permissions

This example first uses the **Get-CMGlobalCondition** cmdlet to get a custom global condition. Then it creates two access control entries for specific users. Next it uses the **New-CMRequirementRuleRegistryKeyPermissionValue** cmdlet to create the requirement rule object. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$myGC = Get-CMGlobalCondition -Name "LOB app registry key"

$userName = "contoso\jqpublic"
$ce = New-CMRegistryAccessControlEntry -GroupOrUserName $userName -AccessOption Allow -Permission Read,Write

$userName2 = "contoso\jdoe"
$ce2 = New-CMRegistryAccessControlEntry -GroupOrUserName $userName2 -AccessOption Allow -Permission Read

$myRule = $myGC | New-CMRequirementRuleRegistryKeyPermissionValue -Exclusive $false -ControlEntry $ce,$ce2

Set-CMScriptDeploymentType -ApplicationName "Central app" -DeploymentTypeName "Install" -AddRequirement $myRule
```

## PARAMETERS

### -AccessOption

Specify whether this ACE is to `Allow` or `Deny` access.

```yaml
Type: AccessType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

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

### -GroupOrUserName

Specify the group or user name for this ACE. Use standard "domain\name" format. For example, `contoso\jqpublic` or `"nwtraders\All IT Users"`.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Permission

Specify an array of one or more permissions for this ACE. Use the **AccessOption** parameter to specify whether these permissions `Allow` or `Deny` access.

```yaml
Type: RegistryPermissions[]
Parameter Sets: (All)
Aliases: Permissions
Accepted values: ChangePermissions, CreateLink, CreateSubkey, Delete, EnumerateSubkeys, FullControl, Notify, QueryValue, Read, ReadPermissions, SetValue, TakeOwnership, Write

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

### System.Object
## NOTES

## RELATED LINKS

[New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
