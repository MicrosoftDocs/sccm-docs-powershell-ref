---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833618
schema: 2.0.0
ms.assetid: 8E441DD5-9BDD-4B76-9734-103AF85B59FB
---

# Add-CMCollectionToDistributionPointGroup

## SYNOPSIS

## SYNTAX

### AddById_Object (Default)
```
Add-CMCollectionToDistributionPointGroup -CollectionId <String> -DistributionPointGroup <IResultObject>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddById_Name
```
Add-CMCollectionToDistributionPointGroup -CollectionId <String> -DistributionPointGroupName <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddById_Id
```
Add-CMCollectionToDistributionPointGroup -CollectionId <String> -DistributionPointGroupId <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddByName_Name
```
Add-CMCollectionToDistributionPointGroup -CollectionName <String> -DistributionPointGroupName <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddByName_Id
```
Add-CMCollectionToDistributionPointGroup -CollectionName <String> -DistributionPointGroupId <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddByName_Object
```
Add-CMCollectionToDistributionPointGroup -CollectionName <String> -DistributionPointGroup <IResultObject>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddByObject_Object
```
Add-CMCollectionToDistributionPointGroup -Collection <IResultObject> -DistributionPointGroup <IResultObject>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddByObject_Name
```
Add-CMCollectionToDistributionPointGroup -Collection <IResultObject> -DistributionPointGroupName <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AddByObject_Id
```
Add-CMCollectionToDistributionPointGroup -Collection <IResultObject> -DistributionPointGroupId <String>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
```

## PARAMETERS

### -Collection
```yaml
Type: IResultObject
Parameter Sets: AddByObject_Object, AddByObject_Name, AddByObject_Id
Aliases: DeviceCollection, UserCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId
```yaml
Type: String
Parameter Sets: AddById_Object, AddById_Name, AddById_Id
Aliases: DeviceCollectionId, UserCollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
```yaml
Type: String
Parameter Sets: AddByName_Name, AddByName_Id, AddByName_Object
Aliases: DeviceCollectionName, UserCollectionName

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

### -DistributionPointGroup
```yaml
Type: IResultObject
Parameter Sets: AddById_Object, AddByName_Object, AddByObject_Object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId
```yaml
Type: String
Parameter Sets: AddById_Id, AddByName_Id, AddByObject_Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
```yaml
Type: String
Parameter Sets: AddById_Name, AddByName_Name, AddByObject_Name
Aliases: 

Required: True
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

### -PassThru
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


