<<<<<<< HEAD
---
title: Set-CMFallbackStatusPoint
titleSuffix: Configuration Manager
description: Changes the throttle interval or the message count for a Configuration Manager fallback status point.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 958D9892-86AF-461B-A025-5EB7E3C9CCFF
online version: https://go.microsoft.com/fwlink/?linkid=833854
schema: 2.0.0
>>>>>>> master
---

# Set-CMFallbackStatusPoint

## SYNOPSIS
Changes the throttle interval or the message count for a Configuration Manager fallback status point.

## SYNTAX

### SetByValue (Default)
```
Set-CMFallbackStatusPoint -InputObject <IResultObject> [-StateMessageCount <Int32>] [-ThrottleSec <Int32>]
 [-ThrottleMins <Int32>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMFallbackStatusPoint [-SiteCode <String>] [-SiteSystemServerName] <String> [-StateMessageCount <Int32>]
 [-ThrottleSec <Int32>] [-ThrottleMins <Int32>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMFallbackStatusPoint** cmdlet changes the throttle interval or the message count for a fallback status point.
A fallback status point is a site system role.
You can specify the site system name and site code for a fallback status point or use the [Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md) cmdlet to obtain a fallback status point object.

Microsoft System Center Configuration Manager can use one or more fallback status points to collect state messages for a site and send them to a server that is running Configuration Manager.
Throttling prevents the fallback status point from sending too many messages together, which can affect performance.
You can use the *StateMessagesCount* and *ThrottleMinutesInterval* parameters to limit how many messages a fallback status point sends during a defined period.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Change message and threshold settings for a fallback status point
```
PS XYZ:\> $CMFSP = Get-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "Server21.West01.Contoso.com"
PS XYZ:\> Set-CMFallbackStatusPoint -InputObject $CMFSP -StateMessagesCount 1000 -ThrottleMinutesInterval 60
```

The first command gets a fallback status point for the site that has the site code CM1 and the system name Server21.West01.Contoso.com and stores that object in the $CMFSP variable.

The second command sets the count of state messages to 1,000 and the throttle interval to 60 minutes for the object stored in $CMFSP.

### Example 2: Change message and threshold settings
```
PS XYZ:\> Set-CMFallbackStatusPoint -SiteCode "CM1" -SiteSystemServerName "Server21.West01.Contoso.com" -StateMessagesCount 1000 -ThrottleMinutesInterval 60
```

This command sets the count of state messages to 1,000 and the throttle interval to 60 minutes for the fallback status point for the site that has the site code CM1 and the system name Server21.West01.Contoso.com.

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
Specifies a fallback status point role.
To obtain a fallback status point role, use the [Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: FallbackStatusPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Specifies the site code for a fallback status point.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the site system name for a fallback status point.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StateMessageCount
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StateMessagesCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ThrottleMinutesInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleSec
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Add-CMFallbackStatusPoint](Add-CMFallbackStatusPoint.md)

[Get-CMFallbackStatusPoint](Get-CMFallbackStatusPoint.md)

[Remove-CMFallbackStatusPoint](Remove-CMFallbackStatusPoint.md)
