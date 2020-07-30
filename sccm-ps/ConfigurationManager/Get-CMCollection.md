---
description: Gets a Configuration Manager collection.
external help file: AdminUI.PS.Collections.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMCollection
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
The **Get-CMCollection** cmdlet gets a Configuration Manager collection.

Configuration Manager collections provide a way to manage users, computers, and other resources in your organization. They not only give you a means to organize your resources, but they also give you a means to distribute Configuration Manager packages to clients and users.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a collection by name
```
PS XYZ:\> Get-CMCollection -Name "testUser"
```

This command gets the collection named testUser.

### Example 2: Get a collection for a distribution point group
```
PS XYZ:\> Get-CMDistributionPointGroup -Name "testDPGroup" | Get-CMCollection
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_Collection

### IResultObject#SMS_Collection

## NOTES

## RELATED LINKS

[Export-CMCollection](Export-CMCollection.md)

[Get-CMDistributionPointGroup](Get-CMDistributionPointGroup.md)

[Import-CMCollection](Import-CMCollection.md)

[New-CMCollection](New-CMCollection.md)

[Remove-CMCollection](Remove-CMCollection.md)

[Set-CMCollection](Set-CMCollection.md)


