---
author: aczechowski
description: Gets how often Configuration Manager evaluates collection membership.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMCollectionMembershipEvaluationComponent
titleSuffix: Configuration Manager
---

# Get-CMCollectionMembershipEvaluationComponent

## SYNOPSIS
Gets how often Configuration Manager evaluates collection membership.

## SYNTAX

```
Get-CMCollectionMembershipEvaluationComponent [-SiteSystemServerName <String>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCollectionMembershipEvaluationComponent** cmdlet gets the value for how often Microsoft System Center Configuration Manager evaluates collections.
Configuration Manager queries the database at a regular interval to check for changes in collection membership.
You can specify which value to get by site server name or site code.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get an evaluation period for a site code
```
PS XYZ:\> Get-CMCollectionMembershipEvaluationComponent -SiteCode "CM4"
```

This command gets the evaluation frequency for collection membership for the specified site code.

### Example 2: Get an evaluation period for a system
```
PS XYZ:\> Get-CMCollectionMembershipEvaluationComponent -SiteSystemServerName "CM01.West01.Contoso.com"
```

This command gets the evaluation frequency for the server named CM01.West01.Contoso.com.

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

### -SiteCode
Specifies a site codes for a Configuration Manager site.

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

### -SiteSystemServerName
Specifies an array of names for Configuration Manager servers.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMCollectionMembershipEvaluationComponent](Set-CMCollectionMembershipEvaluationComponent.md)


