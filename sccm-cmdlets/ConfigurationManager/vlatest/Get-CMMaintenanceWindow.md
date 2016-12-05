---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833736
schema: 2.0.0
ms.assetid: 78ED339E-4DB8-4C21-B704-85031ECF01F8
---

# Get-CMMaintenanceWindow

## SYNOPSIS
Gets the maintenance windows for a collection.

## SYNTAX

### ByCollectionValue (Default)
```
Get-CMMaintenanceWindow [-Collection] <IResultObject> [-MaintenanceWindowName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionId
```
Get-CMMaintenanceWindow [-CollectionId] <String> [-MaintenanceWindowName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionName
```
Get-CMMaintenanceWindow [-CollectionName] <String> [-MaintenanceWindowName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMaintenanceWindow** cmdlet gets the maintenance windows for specified collections.

## EXAMPLES

### Example 1: Get maintenance windows
```
PS C:\>Get-CMMaintenanceWindow -CollectionID "AAA0004D"
```

This command gets the maintenance windows for the specified collection.

## PARAMETERS

### -Collection


```yaml
Type: IResultObject
Parameter Sets: ByCollectionValue
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId
Specifies an array of collection IDs.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName


```yaml
Type: String
Parameter Sets: ByCollectionName
Aliases: 

Required: True
Position: 0
Default value: None
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

### -MaintenanceWindowName


```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMMaintenanceWindow](./New-CMMaintenanceWindow.md)

[Remove-CMMaintenanceWindow](./Remove-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](./Set-CMMaintenanceWindow.md)


