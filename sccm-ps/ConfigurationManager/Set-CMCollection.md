---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Set-CMCollection
---

# Set-CMCollection

## SYNOPSIS

Configure a device or user collection.

## SYNTAX

### SetByValue (Default)
```
Set-CMCollection [-Comment <String>] -InputObject <IResultObject> [-LimitingCollection <IResultObject>]
 [-LimitingCollectionId <String>] [-LimitingCollectionName <String>] [-NewName <String>] [-PassThru]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-VariablePriority <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMCollection -CollectionId <String> [-Comment <String>] [-LimitingCollection <IResultObject>]
 [-LimitingCollectionId <String>] [-LimitingCollectionName <String>] [-NewName <String>] [-PassThru]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-VariablePriority <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCollection [-Comment <String>] [-LimitingCollection <IResultObject>] [-LimitingCollectionId <String>]
 [-LimitingCollectionName <String>] -Name <String> [-NewName <String>] [-PassThru]
 [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>] [-VariablePriority <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure a device or user collection.

The limiting collection determines which resources can be a member of the collection.
For instance, when you use the **All Systems** collection as the limiting collection, the new collection can include any device in the Configuration Manager hierarchy.

Add resources to the collection with membership rules.
To add members to the collection, use one of the cmdlets to add membership rules, for example:

- [Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)
- [Add-CMUserCollectionQueryMembershipRule](Add-CMUserCollectionQueryMembershipRule.md)

You can't configure default collections. Any collection that you target should have an ID that starts with the site code, not `SMS`.

For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a collection

The first command gets the collection object named **testUser** and stores it in the **$userCollection** variable.

The second command updates the name of the collection.

```powershell
$userCollection = Get-CMCollection -Name "testUser"
Set-CMCollection -InputObject $userCollection -NewName "newTestUser"
```

## PARAMETERS

### -CollectionId

Specify the ID of the collection to configure. This value is the **CollectionID** property, for example, `XYZ00012`. You can't configure default collections, so this value starts with the site code, not `SMS`.

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

Specify an optional comment to describe and identify this collection.

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

Specify a collection object to configure. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

Specify an object for the limiting collection. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

Specify the ID of the limiting collection. This value is the **CollectionID** property, for example, `XYZ00012` or `SMS00001`.

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

Specify the name of the limiting collection.

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

Specify the name of a collection to configure.

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

Specify a new name for the collection. Use this parameter to rename it.

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

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

If you set the **RefreshType** parameter to either `Periodic` or `Both`, use this parameter to set the schedule. Specify a schedule object for when the site runs a full update of the collection membership. To get this object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

Specify how the collection membership is updated:

- `Manual` (1): An administrator manually triggers a membership update in the Configuration Manager console or with the [Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md) cmdlet.
- `Periodic` (2): The site does a full update on a schedule. It doesn't use incremental updates. If you don't specify a type, this value is the default.
- `Continuous` (4): The site periodically evaluates new resources and then adds new members. This type is also known as an _incremental update_. It doesn't do a full update on a schedule.
- `Both` (6): A combination of both `Periodic` and `Continuous`, with both incremental updates and a full update on a schedule.

If you specify either `Periodic` or `Both`, use the **RefreshSchedule** parameter to set the schedule.

> [!NOTE]
> The `None` value (0) is functionally the same as `Manual`.

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

### -VariablePriority

Specify an integer value from 1-9 for the priority of device collection variables. `1` is the lowest priority, and `9` is the highest.

To configure variables on a device collection, use the [Set-CMDeviceCollectionVariable](Set-CMDeviceCollectionVariable.md) cmdlet.

To view the current variable priority, use the [Get-CMCollectionSetting](Get-CMCollectionSetting.md) cmdlet.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DeviceCollectionVariablePrecedence

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Copy-CMCollection](Copy-CMCollection.md)
[Export-CMCollection](Export-CMCollection.md)
[Get-CMCollection](Get-CMCollection.md)
[Get-CMCollectionMember](Get-CMCollectionMember.md)
[Get-CMCollectionSetting](Get-CMCollectionSetting.md)
[Import-CMCollection](Import-CMCollection.md)
[Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md)
[New-CMCollection](New-CMCollection.md)
[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[Set-CMDeviceCollectionVariable](Set-CMDeviceCollectionVariable.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)
[Get-CMUserCollection](Get-CMUserCollection.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
