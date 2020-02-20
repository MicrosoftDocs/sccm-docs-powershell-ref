---
author: aczechowski
description: Runs a Configuration Manager deployment summarization.
external help file: AdminUI.PS.Deployments.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Invoke-CMDeploymentSummarization
titleSuffix: Configuration Manager
---

# Invoke-CMDeploymentSummarization

## SYNOPSIS
Runs a Configuration Manager deployment summarization.

## SYNTAX

### SearchByCollectionIdMandatory (Default)
```
Invoke-CMDeploymentSummarization -CollectionId <String> [-SoftwareName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMDeploymentSummarization -DeploymentId <String> [-SoftwareName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByCollectionNameMandatory
```
Invoke-CMDeploymentSummarization -CollectionName <String> [-SoftwareName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMDeploymentSummarization [-SoftwareName <String>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMDeploymentSummarization** cmdlet runs a Microsoft System Center Configuration Manager deployment summarization as soon as possible.
Summarization compiles information about current deployment of software from the Configuration Manager site database.
By default, Configuration Manager runs this summarization every four hours.
If you use this cmdlet to create the summarization immediately, it does not interfere with the regular schedule of creating the current summarization.

You can specify a deployment summarization by ID or by collection or you can specify a deployment summarization object.

## EXAMPLES

### Example 1: Invoke a deployment summarization
```
PS XYZ:\>Invoke-CMDeploymentSummarization -CollectionName "CMWest"
```

This command runs a deployment summarization for the collection named CMWest.

## PARAMETERS

### -CollectionId
```yaml
Type: String
Parameter Sets: SearchByCollectionIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies a name of a collection.

```yaml
Type: String
Parameter Sets: SearchByCollectionNameMandatory
Aliases:

Required: True
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

### -DeploymentId
Specifies an ID of a deployment.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
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

### -InputObject
Specifies a deployment summarization object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Collection, DeploymentSummary

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareName
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
