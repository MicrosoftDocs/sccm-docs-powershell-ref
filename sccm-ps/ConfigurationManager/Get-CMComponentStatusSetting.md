---
title: Get-CMComponentStatusSetting
titleSuffix: Configuration Manager
description: Gets Configuration Manager component status settings.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMComponentStatusSetting

## SYNOPSIS
Gets Configuration Manager component status settings.

## SYNTAX

```
Get-CMComponentStatusSetting [-SiteSystemServerName <String>] [-ComponentName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMComponentStatusSetting** cmdlet gets component status setting objects.
These objects contain thresholds for Microsoft System Center Configuration Manager component status messages.

## EXAMPLES

### Example 1: Get settings for components
```
PS C:\> Get-CMComponentStatusSetting -SiteCode "CAS" -ComponentName SMS_REPL*
```

This command gets status setting objects for the site that has the site code CAS for components with names that begin with SMS_REPL.

### Example 2: Get settings for components on specified systems
```
PS C:\> Get-CMComponentStatusSetting -SiteSystemName VM* -ComponentName SMS_REPL*
```

This command gets status setting objects for systems with names that begin with VM for components with names that begin with SMS_REPL.

## PARAMETERS

### -ComponentName
Specifies a name of a thread or process.
A thread or process sends a component status message.
You can use wildcards.

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

### -SiteSystemServerName
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

[Get-CMComponentStatusMessage](Get-CMComponentStatusMessage.md)


