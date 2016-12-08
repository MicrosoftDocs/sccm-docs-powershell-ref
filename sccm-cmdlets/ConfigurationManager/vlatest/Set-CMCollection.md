---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833739
schema: 2.0.0
ms.assetid: BFDDAC90-E647-44EB-9C5F-1486E267EDD5
---

# Set-CMCollection

## SYNOPSIS
Sets a collection.

## SYNTAX

### SetByValue (Default)
```
Set-CMCollection -InputObject <IResultObject> [-NewName <String>] [-Comment <String>]
 [-LimitingCollectionId <String>] [-LimitingCollectionName <String>] [-LimitingCollection <IResultObject>]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCollection -Name <String> [-NewName <String>] [-Comment <String>] [-LimitingCollectionId <String>]
 [-LimitingCollectionName <String>] [-LimitingCollection <IResultObject>] [-RefreshSchedule <IResultObject>]
 [-RefreshType <CollectionRefreshType>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMCollection -CollectionId <String> [-NewName <String>] [-Comment <String>]
 [-LimitingCollectionId <String>] [-LimitingCollectionName <String>] [-LimitingCollection <IResultObject>]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
**The Set-CMCollection** cmdlet changes settings for a collection in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get a collection and modify it
```
PS C:\> $userCollection = Get-CMCollection -Name "testUser"
PS C:\> Set-CMCollection -CollectionId $userCollection -NewName "newTestUser"
```

The first command gets the collection object named testUser and stores the object in the $userCollection variable.

The second command updates the name of the collection in $userCollection.

### Example 2: Pass a collection and modify it
```
PS C:\> Get-CMCollection -Name "testUser" | Set-CMCollection -NewName "newTestUser"
```

This command gets the collection object named testUser and uses the pipeline operator to pass the object to **Set-CMCollection**, which updates its name to newTestUser.

## PARAMETERS

### -CollectionId
Specifies a collection ID.

```yaml
Type: String
Parameter Sets: SetById
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies a comment for the collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject
Specifies a collection object.
To obtain a collection object, use the [Get-CMCollection](./Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: Collection
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitingCollection
Specifies a collection object to use as a scope for this collection.
To obtain a collection object, use the [Get-CMCollection](./Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionId
Specifies the ID of a collection to use as a scope for this collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LimitToCollectionId
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionName
Specifies the name of a collection to use as a scope for this collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LimitToCollectionName
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a collection.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -RefreshSchedule
Specifies a schedule that determines when Configuration Manager refreshes the collection.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshType
Specifies how Configuration Manager refreshes the collection.
Valid values are:

- None
- Manual 
- Periodic
- Continuous
- Both

```yaml
Type: CollectionRefreshType
Parameter Sets: (All)
Aliases: 
Accepted values: None, Manual, Periodic, Continuous, Both
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCollection](./Get-CMCollection.md)

[Export-CMCollection](./Export-CMCollection.md)

[Import-CMCollection](./Import-CMCollection.md)

[New-CMCollection](./New-CMCollection.md)

[Remove-CMCollection](./Remove-CMCollection.md)
