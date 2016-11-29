---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834130
schema: 2.0.0
ms.assetid: C01E6314-2F4A-4D25-B420-F73CA7F48CBD
---

# Get-CMBaseline

## SYNOPSIS
Gets configuration baselines.

## SYNTAX

### SearchByName (Default)
```
Get-CMBaseline [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBaseline [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByParentBaselineIdMandatory
```
Get-CMBaseline -ParentBaselineId <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaselineNameMandatory
```
Get-CMBaseline -ParentBaselineName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaseline
```
Get-CMBaseline [-ParentBaseline] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMBaseline** cmdlet gets one or more configuration baselines.

## EXAMPLES

### Example 1: Get configuration baselines by using a parent baseline name
```
PS C:\>Get-CMBaseline -ParentBaselineName "ParentBaselineContoso01"
```

This command gets the child configuration baselines in the parent baseline configuration item named ParentBaselineContoso01.

### Example 2: Get configuration baselines by using a parent baseline ID
```
PS C:\>Get-CMBaseline -ParentBaselineId "16777357"
```

This command gets the child configuration baselines in the parent baseline configuration item that has the identity 16777357.

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

### -Id
Specifies an array of IDs of configuration baselines.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration baselines.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentBaseline
Specifies a **CMParentBaseline** object.

```yaml
Type: IResultObject
Parameter Sets: SearchByParentBaseline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentBaselineId
Specifies the ID of a parent baseline object.

```yaml
Type: Int32
Parameter Sets: SearchByParentBaselineIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentBaselineName
Specifies the name of a parent baseline.

```yaml
Type: String
Parameter Sets: SearchByParentBaselineNameMandatory
Aliases: 

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

[Disable-CMBaseline](./Disable-CMBaseline.md)

[Enable-CMBaseline](./Enable-CMBaseline.md)

[Export-CMBaseline](./Export-CMBaseline.md)

[Import-CMBaseline](./Import-CMBaseline.md)

[New-CMBaseline](./New-CMBaseline.md)

[Remove-CMBaseline](./Remove-CMBaseline.md)

[Set-CMBaseline](./Set-CMBaseline.md)

[Get-CMBaselineSummarizationSchedule](./Get-CMBaselineSummarizationSchedule.md)


