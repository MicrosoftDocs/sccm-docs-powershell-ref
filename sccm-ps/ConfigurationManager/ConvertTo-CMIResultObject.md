---
author: aczechowski
description: Converts a **ManagementBaseObject** to an **IResultObject**.
external help file: AdminUI.PS.Common.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: ConvertTo-CMIResultObject
titleSuffix: Configuration Manager
---

# ConvertTo-CMIResultObject

## SYNOPSIS
Converts a **ManagementBaseObject** to an **IResultObject**.

## SYNTAX

```
ConvertTo-CMIResultObject -InputObject <ManagementBaseObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **ConvertTo-CMIResultObject** cmdlet converts a **ManagementBaseObject** to an **IResultObject**.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Convert a ManagementBaseObject to an IResultObject by passing a WMI object through the pipeline
```
PS ABC:\> $WmiObject = Get-WmiObject -Query "SELECT * FROM SMS_Site" -Namespace "root\sms\site_PS1"
PS ABC:\> $WmiObject | ConvertTo-CMIResultObject
```

The first command gets the site object with the code of PS1 and stores the object in the $WmiObject variable.

The second command uses the pipeline operator to pass the site object stored in $WmiObject to **ConvertTo-CMIResultObject**, which converts the site object to an **IResultObject**.

### Example 2: Convert a ManagementBaseObject to an IResultObject by getting a WMI object
```
PS ABC:\> $WmiObject = Get-WmiObject -Query "SELECT * FROM SMS_Site" -Namespace "root\sms\site_PS1"
PS ABC:\> ConvertTo-CMIResultObject -InputObject $WmiObject
```

The first command gets the site object with the code of PS1 and stores the object in the $WmiObject variable.

The second command converts the site object stored in $WmiObject to an **IResultObject**.

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

### -InputObject
Specifies the **ManagementBaseObject** to convert to an **IResultObject**.

```yaml
Type: ManagementBaseObject
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[ConvertFrom-CMIResultObject](./ConvertFrom-CMIResultObject.md)
