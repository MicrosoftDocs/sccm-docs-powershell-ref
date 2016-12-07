---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833868
schema: 2.0.0
ms.assetid: 8D8F8DC3-4AC4-417A-BA50-30E81D02EE6E
---

# Convert-CMSchedule

## SYNOPSIS
Converts schedule tokens into and from interval strings.

## SYNTAX

### ByToken (Default)
```
Convert-CMSchedule [-ScheduleToken] <IResultObject[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByString
```
Convert-CMSchedule [-ScheduleString] <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Convert-CMSchedule** cmdlet decodes and encodes schedule tokens into and from Microsoft System Center Configuration Manager interval strings.

## EXAMPLES

### Example 1: Convert a schedule string
```
PS C:\>Convert-CMSchedule -ScheduleString "02C159C0381A200002C159C0381B200002C159C0381C200002C159C0381D200002C159C0381E2000"
```

This command converts a schedule string into a schedule token.

## PARAMETERS

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

### -ScheduleString
Specifies an array of interval strings.

```yaml
Type: String[]
Parameter Sets: ByString
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleToken
Specifies an array of Configuration Manager schedule objects output from another cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: ByToken
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMClientStatusUpdateSchedule](./Get-CMClientStatusUpdateSchedule.md)

[Get-CMBaselineSummarizationSchedule](./Get-CMBaselineSummarizationSchedule.md)

[Get-CMOperatingSystemImageUpdateSchedule](./Get-CMOperatingSystemImageUpdateSchedule.md)

[Get-CMEndpointProtectionSummarizationSchedule](./Get-CMEndpointProtectionSummarizationSchedule.md)

[Get-CMSoftwareUpdateSummarizationSchedule](./Get-CMSoftwareUpdateSummarizationSchedule.md)

[New-CMSchedule](./New-CMSchedule.md)


