---
author: aczechowski
description: Sets how often Configuration Manager evaluates collections for membership.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMCollectionMembershipEvaluationComponent
titleSuffix: Configuration Manager
---

# Set-CMCollectionMembershipEvaluationComponent

## SYNOPSIS
Sets how often Configuration Manager evaluates collections for membership.

## SYNTAX

```
Set-CMCollectionMembershipEvaluationComponent [-SiteSystemServerName <String>] [-SiteCode <String>]
 -EvaluationMins <Int32> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCollectionMembershipEvaluationComponent** cmdlet changes how often Microsoft System Center Configuration Manager evaluates collections.
Configuration Manager queries the database at a regular interval to check for changes in collection membership.
You can specify which site to change by site server name or site code.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Set an evaluation period for a site code
```
PS XYZ:\> Set-CMCollectionMembershipEvaluationComponent -MinutesInterval 5 -SiteCode "CM4"
```

This command sets the evaluation frequency to five minutes for the specified site code.

### Example 2: Set an evaluation period for a system
```
PS XYZ:\> Set-CMCollectionMembershipEvaluationComponent -MinutesInterval 6 -SiteSystemName "CM01.West01.Contoso.com"
```

This command sets the evaluation frequency to six minutes for the server named CM01.West01.Contoso.com.

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

### -EvaluationMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinutesInterval

Required: True
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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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
Specifies an array of a site codes for Configuration Manager sites.

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
**Note**: This parameter is deprecated starting with version 1610, and may be removed in a future release.

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

[Get-CMCollectionMembershipEvaluationComponent](Get-CMCollectionMembershipEvaluationComponent.md)
