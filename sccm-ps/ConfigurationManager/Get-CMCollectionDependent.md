---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/21/2020
online version:
schema: 2.0.0
---

# Get-CMCollectionDependent

## SYNOPSIS

Get a collection's dependent relationships.

## SYNTAX

### SearchByName
```
Get-CMCollectionDependent -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMCollectionDependent -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMCollectionDependent -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

This cmdlet gets the target collection's dependent relationships. The target collection is a limiting collection for one or more other collections.

For more information, see [View collection relationships](/mem/configmgr/core/clients/manage/collections/manage-collections#view-collection-relationships).

## EXAMPLES

### Example 1: Get the collection relationships by pipeline object

```powershell
Get-CMCollection -Name "All Users" | Get-CMCollectionDependent
```

### Example 2: Get the collection relationships by ID

This example is functionally the same as the first, where the built-in **All Users** collection typically has ID **SMS00002**.

```powershell
Get-CMCollectionDependent -Id "SMS00002"
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
Parameter Sets: SearchById
Aliases: CollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a collection object to query. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify a collection name to query. For example, `"All Users"`.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMCollectionDependency](Get-CMCollectionDependency.md)

[View collection relationships](/mem/configmgr/core/clients/manage/collections/manage-collections#view-collection-relationships)
