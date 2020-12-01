---
external help file: AdminUI.PS.Collections-help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMCollectionFullEvaluationStatus

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByName (Default)
```
Get-CMCollectionFullEvaluationStatus [-Name <String>] [-IsMemberChanged <Boolean>] [<CommonParameters>]
```

### ById
```
Get-CMCollectionFullEvaluationStatus -Id <String> [-IsMemberChanged <Boolean>] [<CommonParameters>]
```

### ByValue
```
Get-CMCollectionFullEvaluationStatus -InputObject <IResultObject> [-IsMemberChanged <Boolean>]
 [<CommonParameters>]
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

### -Id
{{ Fill Id Description }}

```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId

Required: True
Position: Named
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsMemberChanged
{{ Fill IsMemberChanged Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: ByName
Aliases: CollectionName

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

### System.Object
## NOTES

## RELATED LINKS
