---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMDuplicateHardwareIdMacAddress

## SYNOPSIS

Use this cmdlet to add duplicate hardware identifiers by MAC address.

## SYNTAX

```
New-CMDuplicateHardwareIdMacAddress -MacAddress <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1910, use this cmdlet to add duplicate hardware identifiers by MAC address.

## EXAMPLES

### Example 1: Add a duplicate hardware entry for a MAC address

This example adds a duplicate hardware entry for the site by the device's network MAC address.

```powershell
New-CMDuplicateHardwareIdMacAddress -MacAddress '01:02:03:04:05:E0'
```

## PARAMETERS

### -DisableWildcardHandling

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

### -MacAddress

Specify the MAC address of the machine as a string with colon (`:`) delimiters. For example, `'01:02:03:04:05:E0'`

```yaml
Type: String
Parameter Sets: (All)
Aliases: DuplicateId, DuplicateHardwareId

Required: True
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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_CommonMacAddresses

## NOTES

## RELATED LINKS
