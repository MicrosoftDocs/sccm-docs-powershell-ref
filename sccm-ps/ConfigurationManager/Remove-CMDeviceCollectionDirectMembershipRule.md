---
external help file: AdminUI.PS.Collections-help.xml
ms.assetid: 26DED564-E45B-4654-84F5-05707F1080A8
online version: https://go.microsoft.com/fwlink/?linkid=834044
schema: 2.0.0
---

# Remove-CMDeviceCollectionDirectMembershipRule

## SYNOPSIS
Removes a direct membership rule from a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -ResourceName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -Resource <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionName <String> -ResourceId <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -Resource <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -ResourceId <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMDeviceCollectionDirectMembershipRule -CollectionId <String> -ResourceName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -Resource <IResultObject> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMDeviceCollectionDirectMembershipRule -InputObject <IResultObject> -ResourceName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDeviceCollectionDirectMembershipRule** cmdlet removes a direct membership rule from a device collection.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Remove a direct membership rule
```
PS XYZ:\> Remove-CMDeviceCollectionDirectMembershipRule -CollectionName "Device01" -ResourceId 2097152004 -Force
```

This command removes the direct membership rule for the resource with the ID of 2097152004 from the collection named Device01.
Specifying the *Force* parameter indicates that the user is not prompted before the rule is removed.

### Example 2: Remove a direct membership rule by using the pipeline
```
PS XYZ:\> Get-CMCollection -Name "Device02" | Remove-CMDeviceCollectionDirectMembershipRule -Force
```

This command gets the collection object named Device02 and uses the pipeline operator to pass the object to **Remove-CMDeviceCollectionDirectMembershipRule** which removes the direct membership rule for the resource with the ID of 2097152004 from the collection object.
Specifying the *Force* parameter indicates that the user is not prompted before the rule is removed.

## PARAMETERS

### -CollectionId
Specifies the ID of a device collection.

```yaml
Type: String
Parameter Sets: ByIdAndValue, ByIdAndId, ByIdAndName
Aliases: Id

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
Parameter Sets: ByNameAndName, ByNameAndValue, ByNameAndId
Aliases: Name

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

### -Force
Forces the command to run without asking for user confirmation.

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: ByValueAndValue, ByValueAndId, ByValueAndName
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Resource
Specifies a resource object.
To obtain a resource object, use the **Get-CMResource** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByNameAndValue, ByIdAndValue, ByValueAndValue
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
Type: String
Parameter Sets: ByNameAndId, ByIdAndId, ByValueAndId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceName
Specifies the name of a resource.

```yaml
Type: String
Parameter Sets: ByNameAndName, ByIdAndName, ByValueAndName
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

[Add-CMDeviceCollectionDirectMembershipRule](Add-CMDeviceCollectionDirectMembershipRule.md)

[Remove-CMDeviceCollectionExcludeMembershipRule](Remove-CMDeviceCollectionExcludeMembershipRule.md)

[Remove-CMDeviceCollectionIncludeMembershipRule](Remove-CMDeviceCollectionIncludeMembershipRule.md)

[Remove-CMDeviceCollectionQueryMembershipRule](Remove-CMDeviceCollectionQueryMembershipRule.md)


