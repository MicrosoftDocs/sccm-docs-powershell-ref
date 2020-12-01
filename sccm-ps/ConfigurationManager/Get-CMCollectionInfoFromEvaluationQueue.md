---
external help file: AdminUI.PS.Collections.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMCollectionInfoFromEvaluationQueue

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByName (Default)
```
Get-CMCollectionInfoFromEvaluationQueue [[-Name] <String>] -EvaluationTypeOption <EvaluationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollectionInfoFromEvaluationQueue [-Id] <String> -EvaluationTypeOption <EvaluationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMCollectionInfoFromEvaluationQueue [-InputObject] <IResultObject> -EvaluationTypeOption <EvaluationType>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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

### -EvaluationTypeOption
{{ Fill EvaluationTypeOption Description }}

```yaml
Type: EvaluationType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Incremental, Manual, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill Id Description }}

```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: ByName
Aliases: CollectionName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_CollectionInfoInFullEvaluationQueue

### IResultObject#SMS_CollectionInfoInFullEvaluationQueue

### IResultObject[]#SMS_CollectionInfoInIncrementalEvaluationQueue

### IResultObject#SMS_CollectionInfoInIncrementalEvaluationQueue

### IResultObject[]#SMS_CollectionInfoInManualEvaluationQueue

### IResultObject#SMS_CollectionInfoInManualEvaluationQueue

### IResultObject[]#SMS_CollectionInfoInNewEvaluationQueue

### IResultObject#SMS_CollectionInfoInNewEvaluationQueue

## NOTES

## RELATED LINKS
