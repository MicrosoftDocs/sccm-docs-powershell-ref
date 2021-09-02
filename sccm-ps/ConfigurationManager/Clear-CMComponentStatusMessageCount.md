---
description: Changes the component status message count to zero.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Clear-CMComponentStatusMessageCount
---

# Clear-CMComponentStatusMessageCount

## SYNOPSIS
Changes the component status message count to zero.

## SYNTAX

```
Clear-CMComponentStatusMessageCount -ComponentName <String> [-ComputerName <String>] -Severity <Severity>
 [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Clear-CMComponentStatusMessageCount** cmdlet changes the component status message count to zero (0).

Configuration Manager indicates whether operations succeed or fail and include other information in component status messages.
Threads or processes send component status messages to Configuration Manager sites, identified by site codes.

You can define which message count to set to zero by the component that created the messages, severity of the messages, and the site code of the Configuration Manager server that receives the messages.
You can also specify the computer that hosts that component.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Clear message count
```
PS XYZ:\>Clear-CMComponentStatusMessageCount -ComponentName "SMS_HIERARCHY_MANAGER" -Severity All -SiteCode "CM1"
```

This command changes the message count to zero for the component SMS_HIERARCHY_MANAGER for all message severity types.
The command specifies the site that has the site code CM1.

### Example 2: Clear error message count
```
PS XYZ:\>Clear-CMComponentStatusMessageCount -ComponentName "SMS_DISTRIBUTION_MANAGER" -Severity Error -SiteCode "CM1" -ComputerName "West34.Western.Contoso.com"
```

This command changes the message count to zero for the component SMS_DISTRIBUTION_MANAGER for error messages.
The command specifies the site that has the site code CM1, and includes the computer name West34.Western.Contoso.com.

## PARAMETERS

### -ComponentName
Specifies the name of a component that creates messages.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName
Specifies the name of a computer that hosts the component.

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

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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
Specifies the severity of a component status message.
The acceptable values for this parameter are:

- All
- Error
- Information
- Warning

```yaml
Type: Severity
Parameter Sets: (All)
Aliases:
Accepted values: All, Error, Warning, Information

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.
Status messages originate in this site.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMComponentStatusMessage](Get-CMComponentStatusMessage.md)


