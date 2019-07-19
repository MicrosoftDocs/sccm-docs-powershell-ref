<<<<<<< HEAD
---
title: Get-CMConnectionManager
titleSuffix: Configuration Manager
description: Gets the Connection Manager instance associated with the currently-connected site server.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Common.dll-Help.xml
ms.assetid: 688A2F48-7E58-4D4C-97B9-D79933FE4618
online version: https://go.microsoft.com/fwlink/?linkid=834290
schema: 2.0.0
>>>>>>> master
---

# Get-CMConnectionManager

## SYNOPSIS
Gets the Connection Manager instance associated with the currently-connected site server.

## SYNTAX

```
Get-CMConnectionManager [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConnectionManager** cmdlet gets the Connection Manager instance associated with the currently-connected site server.
The Connection Manager instance can be used for directly communicating with the SMS Provider.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get a Connection Manager instance
```
PS ABC:\> Get-CMConnectionManager
```

This command gets the connection manager instance associated with the currently-connected site server.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

