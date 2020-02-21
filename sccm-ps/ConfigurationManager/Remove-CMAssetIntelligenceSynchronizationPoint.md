---
author: aczechowski
description: Removes an Asset Intelligence synchronization point.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Remove-CMAssetIntelligenceSynchronizationPoint
titleSuffix: Configuration Manager
---

# Remove-CMAssetIntelligenceSynchronizationPoint

## SYNOPSIS
Removes an Asset Intelligence synchronization point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAssetIntelligenceSynchronizationPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMAssetIntelligenceSynchronizationPoint [-SiteCode <String>] [-Force] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAssetIntelligenceSynchronizationPoint** cmdlet removes an Asset Intelligence synchronization point from a site system.
After you remove an Asset Intelligence synchronization point, the Microsoft System Center Configuration Manager sites that used the synchronization point cannot connect to System Center Online.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove an Asset Intelligence synchronization point
```
PS XYZ:\> Remove-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "CMDIV-WEST04.CORP.CONTOSO.COM" -SiteCode "CM1"
```

This command removes the Asset Intelligence synchronization point on the System Center Configuration Manager site that has the site code CM1 on the site system server named CMDIV-WEST04.CORP.CONTOSO.COM.

### Example 2: Remove an Asset Intelligence synchronization point by using an object variable
```
PS XYZ:\> $AIsync = Get-CMAssetIntelligenceSynchronizationPoint -SiteSystemServerName "WEST04.CORP.CONTOSO.COM" -SiteCode "ST1"
PS XYZ:\> Remove-CMAssetIntelligenceSynchronizationPoint -InputObject $AIsync
```

The first command gets the Asset Intelligence synchronization point on the System Center Configuration Manager site that has the site code ST1 on the site system server named CMDIV-WEST04.CORP.CONTOSO.COM.
The command stores the results in the $AIsync variable.

The second command removes the Asset Intelligence synchronization point stored in the $AIsync variable.

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
Specifies an Asset Intelligence synchronization point object.
To get a **CMAssetIntelligenceSynchronizationPoint** object, use the Get-CMAssetIntelligenceSynchronizationPoint cmdlet.

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

### -SiteCode
Specifies the three-letter site code of the Configuration Manager site that hosts the site system role.

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
Specifies an array of fully qualified domain names (FQDN) of the servers that host the site system role.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMAssetIntelligenceSynchronizationPoint](Add-CMAssetIntelligenceSynchronizationPoint.md)

[Get-CMAssetIntelligenceSynchronizationPoint](Get-CMAssetIntelligenceSynchronizationPoint.md)

[Set-CMAssetIntelligenceSynchronizationPoint](Set-CMAssetIntelligenceSynchronizationPoint.md)


