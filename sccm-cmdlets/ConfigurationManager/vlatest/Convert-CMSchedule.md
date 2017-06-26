---
external help file: AdminUI.PS.Common.dll-Help.xml
ms.assetid: 8D8F8DC3-4AC4-417A-BA50-30E81D02EE6E
online version: https://go.microsoft.com/fwlink/?linkid=833868
schema: 2.0.0
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
The **Convert-CMSchedule** cmdlet decodes and encodes schedule tokens into and from Microsoft System Center Configuration Manager interval strings.

## EXAMPLES

### Example 1: Convert a schedule string
```
PS C:\>Convert-CMSchedule -ScheduleString "02C159C0381A200002C159C0381B200002C159C0381C200002C159C0381D200002C159C0381E2000"
```

This command converts a schedule string into a schedule token.

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

### -InputObject
{{Fill InputObject Description}}

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


