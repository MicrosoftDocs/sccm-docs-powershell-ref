---
author: aczechowski
description: Removes a state migration point from a Configuration Manager site.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMStateMigrationPoint
titleSuffix: Configuration Manager
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
Remove-CMStateMigrationPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMStateMigrationPoint** cmdlet removes a state migration point from a Microsoft System Center Configuration Manager site.
This site system role stores user information while you perform an operating system deployment.
If you remove a state migration point, you also remove all associated stored user information.

Each state migration point can be a member of only one System Center Configuration Manager site.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMStateMigrationPoint](Add-CMStateMigrationPoint.md)

[Get-CMStateMigrationPoint](Get-CMStateMigrationPoint.md)


