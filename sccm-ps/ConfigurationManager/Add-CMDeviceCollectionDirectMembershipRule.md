---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: CEB87494-F554-4B05-A44B-978B1B418583
online version: https://go.microsoft.com/fwlink/?linkid=833642
schema: 2.0.0
---

# Add-CMDeviceCollectionDirectMembershipRule

## SYNOPSIS
Adds a Direct Rule membership rule to a device collection.

## SYNTAX

### ByCollectionIdAndResourceId (Default)
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -ResourceId <Int32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionIdAndResourceValue
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceId
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -ResourceId <Int32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionNameAndResourceValue
```
Add-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionValueAndResourceId
```
Add-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <Int32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionValueAndResourceValue
```
Add-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDeviceCollectionDirectMembershipRule** cmdlet adds a direct membership rule to a device collection.
A direct membership rule lets you explicitly choose the members of the device collection.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Add a direct membership rule
```
PS XYZ:\>Add-CMDeviceCollectionDirectMembershipRule -CollectionId "SC100056" -ResourceId 2097152004
```

This command adds a device collection direct membership rule to the collection with the ID of SC100056, and adds the resource with the ID of 2097152004 to the collection.

### Example 2: Add a direct membership rule by using the pipeline
```
PS XYZ:\> Get-CMCollection -Name "testCollection" | Add-CMDeviceCollectionDirectMembershipRule -ResourceId 2097152004
```

This command gets the collection object named testCollection and uses the pipeline operator to pass the object to **Add-CMDeviceCollectionDirectMembershipRule**, which adds the direct membership rule to the collection object, and the resource with the ID of 2097152004 to the collection.This command gets the collection named Collection07 by using the [Get-CMCollection](Get-CMCollection.md) cmdlet.
The command passes the collection to the current cmdlet by using the pipeline operator.
The cmdlet adds the direction membership rule that has the ID 2097152004 to that collection.

## PARAMETERS

### -CollectionId
Specifies the ID of a device collection.

```yaml
Type: String
Parameter Sets: ByCollectionIdAndResourceId, ByCollectionIdAndResourceValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a device collection.

```yaml
Type: String
Parameter Sets: ByCollectionNameAndResourceId, ByCollectionNameAndResourceValue
Aliases: 

Required: True
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
Specifies a device collection object.
To obtain a device collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionValueAndResourceId, ByCollectionValueAndResourceValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
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

### -Resource
Specifies a resource object.
To obtain a resource object, use the Get-CMResource cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByCollectionIdAndResourceValue, ByCollectionNameAndResourceValue, ByCollectionValueAndResourceValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the ID of a resource.

```yaml
Type: Int32
Parameter Sets: ByCollectionIdAndResourceId, ByCollectionNameAndResourceId, ByCollectionValueAndResourceId
Aliases: 

Required: True
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

[Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433)

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollectionDirectMembershipRule](Get-CMDeviceCollectionDirectMembershipRule.md)

[Remove-CMDeviceCollectionDirectMembershipRule](Remove-CMDeviceCollectionDirectMembershipRule.md)


