---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2020
online version:
schema: 2.0.0
---

# Get-CMCollectionEvaluationStatus

## SYNOPSIS

Get the status of collection evaluation.

## SYNTAX

### ByName (Default)
```
Get-CMCollectionEvaluationStatus [-IsMemberChanged <Boolean>] -EvaluationTypeOption <EvaluationType>
 [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollectionEvaluationStatus [-IsMemberChanged <Boolean>] -EvaluationTypeOption <EvaluationType>
 [-Id] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMCollectionEvaluationStatus [-IsMemberChanged <Boolean>] -EvaluationTypeOption <EvaluationType>
 [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Get the status of collection evaluation. For more information, see [How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view).

> [!TIP]
> The collection evaluation process happens on primary sites, not on the central administration site (CAS). Use this cmdlet when connected to a primary site.

## EXAMPLES

### Example 1: Show status for collections with long full evaluation

This example first uses **Get-CMCollectionEvaluationStatus** to get the status of full evaluation for all collections. It then uses the **Where-Object** cmdlet to filter the results to the collections where the full evaluation time was greater than five seconds (5000 milliseconds).

```powershell
Get-CMCollectionEvaluationStatus -EvaluationTypeOption Full | Where-Object Length -gt 5000
```

### Example 2: Show summary of full evaluation on built-in collections that recently changed

This example first uses the **Get-CMCollection** cmdlet to get all collections whose name starts with `All`. The results of this query will include all built-in collections such as **All Systems** and **All Users**. It then passes those results to the **Get-CMCollectionEvaluationStatus** cmdlet to get their full evaluation status, only if they had any recent member changes. It then uses the **Select-Object** cmdlet to only display the name of the collection, how many milliseconds full evaluation took, and how many members changed. By default, the output displays as a table.

```powershell
Get-CMCollection -Name "All*" | Get-CMCollectionEvaluationStatus -EvaluationTypeOption Full -IsMemberChanged $True | Select-Object CollectionName, Length, MemberChanges
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

Specify the type of evaluation for which to get the status, either `Full` or `Incremental`. For more information, see [Collection evaluation in Configuration Manager](/mem/configmgr/core/clients/manage/collections/collection-evaluation).

```yaml
Type: EvaluationType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Incremental

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

### IResultObject[]#SMS_CollectionEvaluationFull
### IResultObject#SMS_CollectionEvaluationFull
### IResultObject[]#SMS_CollectionEvaluationIncremental
### IResultObject#SMS_CollectionEvaluationIncremental
## NOTES

## RELATED LINKS

[Get-CMCollectionFullEvaluationStatus](Get-CMCollectionFullEvaluationStatus.md)

[Get-CMCollectionIncrementalEvaluationStatus](Get-CMCollectionIncrementalEvaluationStatus.md)

[Get-CMCollectionInfoFromEvaluationQueue](Get-CMCollectionInfoFromEvaluationQueue.md)

[Get-CMCollectionInfoFromFullEvaluationQueue](Get-CMCollectionInfoFromFullEvaluationQueue.md)

[Get-CMCollectionInfoFromIncrementalEvaluationQueue](Get-CMCollectionInfoFromIncrementalEvaluationQueue.md)

[Get-CMCollectionInfoFromManualEvaluationQueue](Get-CMCollectionInfoFromManualEvaluationQueue.md)

[Get-CMCollectionInfoFromNewEvaluationQueue](Get-CMCollectionInfoFromNewEvaluationQueue.md)

[How to view collection evaluation](/mem/configmgr/core/clients/manage/collections/collection-evaluation-view)

[Collection evaluation in Configuration Manager](/mem/configmgr/core/clients/manage/collections/collection-evaluation)
