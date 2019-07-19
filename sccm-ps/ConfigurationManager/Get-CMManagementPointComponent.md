<<<<<<< HEAD
---
title: Get-CMManagementPointComponent
titleSuffix: Configuration Manager
description: Gets a component for a Configuration Manager management point.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 69AC1D24-491C-4095-B924-5D78E948342B
online version: https://go.microsoft.com/fwlink/?linkid=833745
schema: 2.0.0
>>>>>>> master
---

# Get-CMManagementPointComponent

## SYNOPSIS
Gets a component for a Configuration Manager management point.

## SYNTAX

```
Get-CMManagementPointComponent [-SiteCode <String>] [-SiteSystemServerName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMManagementPointComponent** cmdlet gets a component of a management point for Microsoft System Center Configuration Manager.
A management point is a System Center Configuration Manager site that provides policy and service information to clients and receives configuration data from clients.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get a management point component
```
PS XYZ:\> Get-CMManagementPointComponent -SiteCode "CM1" >>\1\Get-CMManagementPointComponent_data.txt
```

This command gets a component that is associated with the site that has the code CM1.
The command directs the output to the file Get-CMManagementPointComponent_data.txt.

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
Specifies the site code for the management point.

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
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMManagementPointComponent](Set-CMManagementPointComponent.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Remove-CMManagementPoint](Remove-CMManagementPoint.md)


