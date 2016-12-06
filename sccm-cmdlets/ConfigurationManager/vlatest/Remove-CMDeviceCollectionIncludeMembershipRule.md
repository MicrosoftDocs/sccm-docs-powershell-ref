---
external help file: AdminUI.PS.Collections-help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834051
schema: 2.0.0
ms.assetid: D0AB3D9A-6F2D-4373-9FC7-60990D9D8CCD
---

# Remove-CMDeviceCollectionIncludeMembershipRule

## SYNOPSIS
Removes an Include Collections membership rule from a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionName <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Remove-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionName <String> [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Remove-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Remove-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Remove-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionName <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDeviceCollectionIncludeMembershipRule** cmdlet removes an Include Collections membership rule from a device collection.

## EXAMPLES

### Example 1: Remove an Include Collections membership rule
```
PS C:\>Remove-CMDeviceCollectionIncludeMembershipRule -CollectionName "Device" -IncludeCollectionName "All Systems" -Force
```

This command removes the Include Collections membership rule named All Systems from the device collection named Device.
Specifying the *Force* parameter indicates that the membership rule is removed without prompting the user.

### Example 2: Remove an include membership rule by using the pipeline
```
PS C:\>Get-CMCollection -Name "Device" | Remove-CMDeviceCollectionIncludeMembershipRule -IncludeCollectionName "All Systems" -Force
```

This command gets the device collection object named Device and uses the pipeline operator to pass the object to **Remove-CMDeviceCollectionIncludeMembershipRule**.
**Remove-CMDeviceCollectionIncludeMembershipRule** removes the Include Collections membership rule named All Systems from the device collection object.
Specifying the *Force* parameter indicates that the membership rule is removed without prompting the user.

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

### -IncludeCollection
Specifies a device collection object included in a membership rule.
To obtain a collection object, use the Get-CMCollection cmdlet.

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

### -IncludeCollectionId
Specifies the ID of a device collection included in a membership rule.

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

### -IncludeCollectionName
Specifies the name of a device collection included in a membership rule.

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

### -InputObject


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

[Add-CMDeviceCollectionIncludeMembershipRule](./Add-CMDeviceCollectionIncludeMembershipRule.md)

[Get-CMCollection](./Get-CMCollection.md)

[Get-CMDeviceCollectionIncludeMembershipRule](./Get-CMDeviceCollectionIncludeMembershipRule.md)

[Get-CMDeviceCollection](./Get-CMDeviceCollection.md)

[Remove-CMDeviceCollectionExcludeMembershipRule](./Remove-CMDeviceCollectionExcludeMembershipRule.md)

[Remove-CMDeviceCollectionQueryMembershipRule](./Remove-CMDeviceCollectionQueryMembershipRule.md)


