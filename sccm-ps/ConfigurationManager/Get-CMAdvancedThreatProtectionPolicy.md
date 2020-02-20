---
author: aczechowski
description: Gets an advanced threat protection policy
external help file: AdminUI.PS.Dcm-help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/01/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMAdvancedThreatProtectionPolicy
titleSuffix: Configuration Manager
---

# Get-CMAdvancedThreatProtectionPolicy

## SYNOPSIS
Gets an advanced threat protection policy

## SYNTAX

### ByValue (Default)
```
Get-CMAdvancedThreatProtectionPolicy [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMAdvancedThreatProtectionPolicy [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMAdvancedThreatProtectionPolicy [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -Fast
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
```yaml
Type: Int32
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
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
