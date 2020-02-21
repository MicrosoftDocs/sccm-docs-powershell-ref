---
author: aczechowski
description: Gets configuration baselines.
external help file: AdminUI.PS.Dcm.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMBaseline
titleSuffix: Configuration Manager
---

# Get-CMBaseline

## SYNOPSIS
Gets configuration baselines.

## SYNTAX

### SearchByName (Default)
```
Get-CMBaseline [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBaseline [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByParentBaselineIdMandatory
```
Get-CMBaseline -ParentBaselineId <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaselineNameMandatory
```
Get-CMBaseline -ParentBaselineName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaseline
```
Get-CMBaseline [-ParentBaseline] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBaseline** cmdlet gets one or more configuration baselines.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get configuration baselines by using a parent baseline name
```
PS XYZ:\> Get-CMBaseline -ParentBaselineName "ParentBaselineContoso01"
```

This command gets the child configuration baselines in the parent baseline configuration item named ParentBaselineContoso01.

### Example 2: Get configuration baselines by using a parent baseline ID
```
PS XYZ:\> Get-CMBaseline -ParentBaselineId "16777357"
```

This command gets the child configuration baselines in the parent baseline configuration item that has the identity 16777357.

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
Specifies an array of IDs of configuration baselines.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration baselines.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentBaseline
Specifies a **CMParentBaseline** object.

```yaml
Type: IResultObject
Parameter Sets: SearchByParentBaseline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentBaselineId
Specifies the ID of a parent baseline object.

```yaml
Type: Int32
Parameter Sets: SearchByParentBaselineIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentBaselineName
Specifies the name of a parent baseline.

```yaml
Type: String
Parameter Sets: SearchByParentBaselineNameMandatory
Aliases:

Required: True
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

[Disable-CMBaseline](Disable-CMBaseline.md)

[Enable-CMBaseline](Enable-CMBaseline.md)

[Export-CMBaseline](Export-CMBaseline.md)

[Import-CMBaseline](Import-CMBaseline.md)

[New-CMBaseline](New-CMBaseline.md)

[Remove-CMBaseline](Remove-CMBaseline.md)

[Set-CMBaseline](Set-CMBaseline.md)

[Get-CMBaselineSummarizationSchedule](Get-CMBaselineSummarizationSchedule.md)


