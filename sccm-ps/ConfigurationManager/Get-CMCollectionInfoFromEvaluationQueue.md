---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2020
online version:
schema: 2.0.0
---

# Get-CMCollectionInfoFromEvaluationQueue

## SYNOPSIS

Get collection information from the evaluation queue.

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

Get collection information from the evaluation queue. For more information, see [How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view).

> [!TIP]
> The collection evaluation process happens on primary sites, not on the central administration site (CAS). Use this cmdlet when connected to a primary site.

## EXAMPLES

### Example 1: Show all collections due for full evaluation

```powershell
Get-CMCollectionInfoFromEvaluationQueue -EvaluationTypeOption Full
```

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

### -EvaluationTypeOption

Specify the type of evaluation queue for which to get the status. For more information, see [Monitoring collection evaluation queues](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view#monitoring-collection-evaluation-queues).

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

### -Id

Specify the ID of a collection to query. For example, `"SMS00002"`.

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

Specify a collection object to query. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify the name of a collection to query. For example, `"All Users"`.

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

[Get-CMCollectionEvaluationStatus](Get-CMCollectionEvaluationStatus.md)

[Get-CMCollectionFullEvaluationStatus](Get-CMCollectionFullEvaluationStatus.md)

[Get-CMCollectionIncrementalEvaluationStatus](Get-CMCollectionIncrementalEvaluationStatus.md)

[Get-CMCollectionInfoFromFullEvaluationQueue](Get-CMCollectionInfoFromFullEvaluationQueue.md)

[Get-CMCollectionInfoFromIncrementalEvaluationQueue](Get-CMCollectionInfoFromIncrementalEvaluationQueue.md)

[Get-CMCollectionInfoFromManualEvaluationQueue](Get-CMCollectionInfoFromManualEvaluationQueue.md)

[Get-CMCollectionInfoFromNewEvaluationQueue](Get-CMCollectionInfoFromNewEvaluationQueue.md)

[How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view)

[Collection evaluation in Configuration Manager](/mem/configmgr/core/clients/manage/collections/collection-evaluation)
