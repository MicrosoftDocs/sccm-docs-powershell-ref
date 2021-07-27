---
description: Removes a state migration point from a Configuration Manager site.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMStateMigrationPoint
---

# Remove-CMStateMigrationPoint

## SYNOPSIS
Removes a state migration point from a Configuration Manager site.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMStateMigrationPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMStateMigrationPoint [-Force] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMStateMigrationPoint** cmdlet removes a state migration point from a Configuration Manager site.
This site system role stores user information while you perform an operating system deployment.
If you remove a state migration point, you also remove all associated stored user information.

Each state migration point can be a member of only one Configuration Manager site.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a specified migration point
```
PS XYZ:\> Remove-CMStateMigrationPoint -SiteCode "CM1" -SiteSystemServerName "SMP01.Western.Contoso.com"
```

This command removes a state migration point that belongs to the site that has the site code CM1.
The command specifies the name of computer that hosts the site system role.

### Example 2: Remove a migration point using a variable
```
PS XYZ:\> $CMSMP = Get-CMStateMigrationPoint -SiteCode "CM1" -SiteSystemServerName "SMP01.TSQA.Contoso.com"
PS XYZ:\> Remove-CMStateMigrationPoint -InputObject $CMSMP
```

The first command uses the Get-CMStateMigrationPoint to get a state migration point that belongs to the specified site and has the specified host name, and then stores that object in the $CMSMP variable.

The second command removes the state migration point stored in the $CMSMP variable.

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
Specifies a state migration point object.
To obtain a state migration point object, use the Get-CMStateMigrationPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: StateMigrationPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the host name for a state migration point.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

Required: True
Position: 0
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

## NOTES

## RELATED LINKS

[Add-CMStateMigrationPoint](Add-CMStateMigrationPoint.md)

[Get-CMStateMigrationPoint](Get-CMStateMigrationPoint.md)


