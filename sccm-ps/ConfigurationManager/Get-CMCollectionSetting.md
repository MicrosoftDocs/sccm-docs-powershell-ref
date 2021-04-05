---
description: Gets the settings for a collection.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCollectionSetting
---

# Get-CMCollectionSetting

## SYNOPSIS
Gets the settings for a collection.

## SYNTAX

### ByValue (Default)
```
Get-CMCollectionSetting [-CollectionType <CollectionType>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollectionSetting -CollectionId <String> [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMCollectionSetting -CollectionName <String> [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCollectionSetting** cmdlet gets the settings for a collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the settings for a collection by using the pipeline
```
PS XYZ:\> Get-CMCollection -Id MP500014 | Get-CMCollectionSetting -CollectionType Device
```

This command gets the collection object with the ID of MP500014 and uses the pipeline operator to pass the object to **Get-CMCollectionSetting**, which gets the device collection settings for the collection object.

### Example 2: Get the settings for a collection by name
```
PS XYZ:\> Get-CMCollectionSetting -CollectionName "Devicecol1"
```

This command gets the collection settings for the device collection named Devicecol1.

## PARAMETERS

### -CollectionId
Specifies the ID of a collection.

```yaml
Type: String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a collection.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionType
Specifies the collection type.
A collection type of User is 1.
A collection type of Device is 2.
You can specify the type by using either User or Device, or 1 or 2.

```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases:
Accepted values: User, Device

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -InputObject
Specifies a collection object.
To obtain a collection object, use the Get-CMCollection, Get-CMDeviceCollection or Get-CMUserCollection cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMUserCollection](Get-CMUserCollection.md)


