---
description: Converts schedule tokens into and from interval strings.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Convert-CMSchedule
---

# Convert-CMSchedule

## SYNOPSIS
Converts schedule tokens into and from interval strings.

## SYNTAX

### ByToken (Default)
```
Convert-CMSchedule [-InputObject] <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByString
```
Convert-CMSchedule [-ScheduleString] <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Convert-CMSchedule** cmdlet decodes and encodes schedule tokens into and from Configuration Manager interval strings.

In Configuration Manager, scheduling information is configured by using schedule tokens. The interval strings can be used to set schedule properties when defining or modifying objects.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Convert a schedule string
```
PS XYZ:\>Convert-CMSchedule -ScheduleString "02C159C0381A200002C159C0381B200002C159C0381C200002C159C0381D200002C159C0381E2000"
```

This command converts a schedule string into a schedule token.

## PARAMETERS

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

### -InputObject
```yaml
Type: IResultObject[]
Parameter Sets: ByToken
Aliases: ScheduleToken

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ScheduleString
Specifies an array of interval strings.

```yaml
Type: String[]
Parameter Sets: ByString
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
## OUTPUTS

### IResultObject#SMS_ScheduleToken
### System.String
### System.String[]
## NOTES

## RELATED LINKS

[Get-CMClientStatusUpdateSchedule](Get-CMClientStatusUpdateSchedule.md)

[Get-CMBaselineSummarizationSchedule](Get-CMBaselineSummarizationSchedule.md)

[Get-CMOperatingSystemImageUpdateSchedule](Get-CMOperatingSystemImageUpdateSchedule.md)

[Get-CMEndpointProtectionSummarizationSchedule](Get-CMEndpointProtectionSummarizationSchedule.md)

[Get-CMSoftwareUpdateSummarizationSchedule](Get-CMSoftwareUpdateSummarizationSchedule.md)

[New-CMSchedule](New-CMSchedule.md)


