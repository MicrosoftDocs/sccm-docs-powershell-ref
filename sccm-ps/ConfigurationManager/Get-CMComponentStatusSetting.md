---
description: Gets Configuration Manager component status settings.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMComponentStatusSetting
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

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get settings for components
```
PS XYZ:\> Get-CMComponentStatusSetting -SiteCode "CAS" -ComponentName SMS_REPL*
```

This command gets status setting objects for the site that has the site code CAS for components with names that begin with SMS_REPL.

### Example 2: Get settings for components on specified systems
```
PS XYZ:\> Get-CMComponentStatusSetting -SiteSystemName VM* -ComponentName SMS_REPL*
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### ComponentStatusSetting[]

### ComponentStatusSetting

## NOTES

## RELATED LINKS

[Get-CMComponentStatusMessage](Get-CMComponentStatusMessage.md)


