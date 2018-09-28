---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: B6EE1D79-4D2D-4971-8F24-F7EEADA0A292
online version: https://go.microsoft.com/fwlink/?linkid=834212
schema: 2.0.0
---

# Get-CMCollection

## SYNOPSIS
Gets a Configuration Manager collection.

## SYNTAX

### ByName (Default)
```
Get-CMCollection [-Name <String>] [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMCollection -Id <String> [-CollectionType <CollectionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMCollection -DistributionPointGroupName <String> [-CollectionType <CollectionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMCollection -DistributionPointGroupId <String> [-CollectionType <CollectionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByDPGroup
```
Get-CMCollection -DistributionPointGroup <IResultObject> [-CollectionType <CollectionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCollection** cmdlet gets a Microsoft System Center Configuration Manager collection. 

Configuration Manager collections provide a way to manage users, computers, and other resources in your organization. They not only give you a means to organize your resources, but they also give you a means to distribute Configuration Manager packages to clients and users.

## EXAMPLES

### Example 1: Get a collection by name
```
PS C:\> Get-CMCollection -Name "testUser"
```

This command gets the collection named testUser.

### Example 2: Get a collection for a distribution point group
```
PS C:\> Get-CMDistributionPointGroup -Name "testDPGroup" | Get-CMCollection
```

This command gets the distribution point group object named testDPGroup and uses the pipeline operator to pass the object to **Get-CMCollection**, which gets the collection associated with the distribution point group.

## PARAMETERS

### -CollectionType
Specifies a type for the collection.
Valid values are:

- Root
- User
- Device
- Unknown

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

### -DistributionPointGroup
Specifies a distribution point group object that is associated with a collection.
To obtain a distribution point group object, use the [Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByDPGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId
Specifies the ID of the distribution point group that is associated with the collection.

```yaml
Type: String
Parameter Sets: ByDPGroupId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
Specifies the name of the distribution point group that is associated with a collection.

```yaml
Type: String
Parameter Sets: ByDPGroupName
Aliases: 

Required: True
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

### -Id
Specifies a collection ID.
If you do not specify a collection, all collections in the hierarchy are returned.

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

### -Name
Specifies a collection name.
If you do not specify a collection, all collections in the hierarchy are returned.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

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

### IResultObject[]#SMS_Collection

## NOTES

## RELATED LINKS

[Export-CMCollection](Export-CMCollection.md)

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Import-CMCollection](Import-CMCollection.md)

[New-CMCollection](New-CMCollection.md)

[Remove-CMCollection](Remove-CMCollection.md)

[Set-CMCollection](Set-CMCollection.md)


