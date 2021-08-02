---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2020
online version:
schema: 2.0.0
---

# Get-CMCollectionFullEvaluationStatus

## SYNOPSIS

Get the full evaluation status for a collection.

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

Get the full evaluation status for a collection. For more information, see [How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view).

> [!TIP]
> The collection evaluation process happens on primary sites, not on the central administration site (CAS). Use this cmdlet when connected to a primary site.

## EXAMPLES

### Example 1: Show status for collections with long full evaluation

This example first uses **Get-CMCollectionFullEvaluationStatus** to get the status of full evaluation for all collections. It then uses the **Where-Object** cmdlet to filter the results to the collections where the full evaluation time was greater than five seconds (5000 milliseconds).

```powershell
Get-CMCollectionFullEvaluationStatus | Where-Object Length -gt 5000
```

## PARAMETERS

### -Id

Specify the ID of a collection to query. For example, `"SMS00002"`.

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

Specify a collection object to query. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet. This parameter currently only accepts a single collection object.

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

Set this parameter to `$true` to filter the results to collections whose membership recently changed. In other words, where the **MemberChanges** attribute isn't `0`.

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

Specify the name of a collection to query. For example, `"All Users"`.

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

[Get-CMCollectionEvaluationStatus](Get-CMCollectionEvaluationStatus.md)

[Get-CMCollectionIncrementalEvaluationStatus](Get-CMCollectionIncrementalEvaluationStatus.md)

[Get-CMCollectionInfoFromEvaluationQueue](Get-CMCollectionInfoFromEvaluationQueue.md)

[Get-CMCollectionInfoFromFullEvaluationQueue](Get-CMCollectionInfoFromFullEvaluationQueue.md)

[Get-CMCollectionInfoFromIncrementalEvaluationQueue](Get-CMCollectionInfoFromIncrementalEvaluationQueue.md)

[Get-CMCollectionInfoFromManualEvaluationQueue](Get-CMCollectionInfoFromManualEvaluationQueue.md)

[Get-CMCollectionInfoFromNewEvaluationQueue](Get-CMCollectionInfoFromNewEvaluationQueue.md)

[How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view)

[Collection evaluation in Configuration Manager](/mem/configmgr/core/clients/manage/collections/collection-evaluation)
