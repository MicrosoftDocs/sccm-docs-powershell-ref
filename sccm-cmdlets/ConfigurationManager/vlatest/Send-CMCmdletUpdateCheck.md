---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833597
schema: 2.0.0
ms.assetid: 15162B1F-B421-431D-A171-5B38A0FDBC0B
---

# Send-CMCmdletUpdateCheck

## SYNOPSIS
Performs an unscheduled cmdlet update check.

## SYNTAX

```
Send-CMCmdletUpdateCheck [-Timeout <TimeSpan>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Send-CMCmdletUpdateCheck** cmdlet performs an unscheduled cmdlet update check.
An unscheduled check does not consider policy settings.

## EXAMPLES

### Example 1: Perform a cmdlet update check
```
PS C:\> $Timeout = 50 * 24 * 3600
PS C:\> Send-CMCmdletUpdateCheck -Timeout $Timeout
```

The first command creates a time span and stores the time span in the $Timeout variable.

The second command starts a cmdlet update check that specifies the timeout time span stored in $Timeout.

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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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

### -Timeout
Specifies a time span to wait before timing out while checking for a cmdlet update.

```yaml
Type: TimeSpan
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

[Get-CMCmdletUpdateCheck](./Get-CMCmdletUpdateCheck.md)

[Set-CMCmdletUpdateCheck](./Set-CMCmdletUpdateCheck.md)


