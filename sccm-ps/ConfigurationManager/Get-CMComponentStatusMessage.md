<<<<<<< HEAD
---
title: Get-CMComponentStatusMessage
titleSuffix: Configuration Manager
description: Gets component status messages in Configuration Manager.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.SystemStatus.dll-Help.xml
ms.assetid: 3AABF576-B504-4756-A8B8-412E842306C3
online version: https://go.microsoft.com/fwlink/?linkid=834250
schema: 2.0.0
>>>>>>> master
---

# Get-CMComponentStatusMessage

## SYNOPSIS
Gets component status messages in Configuration Manager.

## SYNTAX

```
Get-CMComponentStatusMessage [-ComponentName <String>] [-ComputerName <String>] [-SiteCode <String>]
 [-Severity <Severity>] -StartTime <DateTime> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMComponentStatusMessage** cmdlet gets component status messages for a specified period.

Microsoft System Center Configuration Manager indicates whether operations succeed or fail and include other information in component status messages.
Threads or processes send component status messages to Configuration Manager sites, which are identified by site codes.

You can define which messages to get by the severity of the message, the component that created the message, the computer that hosts that component, or the Configuration Manager server that receives the message.
You must specify a viewing period, as a **TimeSpan** object.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get critical messages for a site
```
PS XYZ:\> Get-CMComponentStatusMessage -ViewingPeriod "2/1/2013 12:00 AM" -Severity Warning -SiteCode "CM1"
```

This command gets component status messages for the specified viewing period for the Configuration Manager site that has the site code CM1.
The command gets only warning messages.

## PARAMETERS

### -ComponentName
Specifies the name of a thread or process.
A thread or process sends a component status message.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Component

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Specifies the name of a computer.
A computer hosts a component that sends a status message.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MachineName

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

### -Severity
Specifies the severity of status messages. 
The acceptable values for this parameter are:

- ALL
- Error
- Information
- Warning

```yaml
Type: Severity
Parameter Sets: (All)
Aliases: 
Accepted values: All, Error, Warning, Information

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

### -StartTime
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: ViewingPeriod

Required: True
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

[Get-CMComponentStatusSetting](Get-CMComponentStatusSetting.md)


