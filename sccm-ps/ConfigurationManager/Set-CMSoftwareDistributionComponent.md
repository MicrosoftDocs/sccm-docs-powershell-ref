---
author: aczechowski
description: Sets properties of a software distribution component in Configuration Manager.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMSoftwareDistributionComponent
titleSuffix: Configuration Manager
---

# Set-CMSoftwareDistributionComponent

## SYNOPSIS
Sets properties of a software distribution component in Configuration Manager.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Set-CMSoftwareDistributionComponent [-SiteCode <String>] [-MaximumPackageCount <Int32>]
 [-MaximumThreadCountPerPackage <Int32>] [-RetryCount <Int32>] [-DelayBeforeRetryingMins <Int32>]
 [-MulticastRetryCount <Int32>] [-MulticastDelayBeforeRetryingMins <Int32>]
 [-NetworkAccessAccountName <String[]>] [-AddNetworkAccessAccountName <String[]>]
 [-RemoveNetworkAccessAccountName <String[]>] [-CleanNetworkAccessAccountName] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySiteCodeMandatory_ClientComputerAccount
```
Set-CMSoftwareDistributionComponent [-SiteCode <String>] [-MaximumPackageCount <Int32>]
 [-MaximumThreadCountPerPackage <Int32>] [-RetryCount <Int32>] [-DelayBeforeRetryingMins <Int32>]
 [-MulticastRetryCount <Int32>] [-MulticastDelayBeforeRetryingMins <Int32>] [-ClientComputerAccount]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareDistributionComponent** cmdlet sets properties of a software distribution component in Microsoft System Center Configuration Manager.
You can configure the properties of an object to meet the demands that clients place on the System Center Configuration Manager site.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Set properties of a software distribution component
```
PS XYZ:\> Set-CMSoftwareDistributionComponent -SiteCode "CM2" -MaximumPackageCount 3 -MaximumThreadsPerPackage 6 -RetryCount 99 -DelayBeforeRetryingMinutes 31 -MulticastRetryCount 4 -MulticastDelayBeforeRetryingMinutes 2 -NetworkAccessAccount "Western\ElisaDaugherty"
```

The following command sets all properties for a software distribution component.

## PARAMETERS

### -AddNetworkAccessAccountName
{{ Fill AddNetworkAccessAccountName Description }}

```yaml
Type: String[]
Parameter Sets: SearchBySiteCodeMandatory
Aliases: AddNetworkAccessAccountNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanNetworkAccessAccountName
{{ Fill CleanNetworkAccessAccountName Description }}

```yaml
Type: SwitchParameter
Parameter Sets: SearchBySiteCodeMandatory
Aliases: CleanNetworkAccessAccountNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientComputerAccount
Indicates that the cmdlet uses a client computer account.

```yaml
Type: SwitchParameter
Parameter Sets: SearchBySiteCodeMandatory_ClientComputerAccount
Aliases:

Required: False
Position: Named
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

### -DelayBeforeRetryingMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DelayBeforeRetryingMinutes

Required: False
Position: Named
Default value: None
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

### -MaximumPackageCount
Specifies a maximum number of packages.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumThreadCountPerPackage
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumThreadsPerPackage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MulticastDelayBeforeRetryingMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MulticastDelayBeforeRetryingMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MulticastRetryCount
Specifies a retry count for multicast software distribution attempts.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkAccessAccountName
Specifies an account name for network access.

```yaml
Type: String[]
Parameter Sets: SearchBySiteCodeMandatory
Aliases: NetworkAccessAccountNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveNetworkAccessAccountName
{{ Fill RemoveNetworkAccessAccountName Description }}

```yaml
Type: String[]
Parameter Sets: SearchBySiteCodeMandatory
Aliases: RemoveNetworkAccessAccountNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RetryCount
Specifies a retry count.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code of a Configuration Manager site.

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

[Get-CMSoftwareDistributionComponent](Get-CMSoftwareDistributionComponent.md)
