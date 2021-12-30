---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: New-CMCollection
---

# New-CMCollection

## SYNOPSIS

Create a device or user collection.

## SYNTAX

### ByName (Default)
```
New-CMCollection -CollectionType <CollectionType> [-Comment <String>] -LimitingCollectionName <String>
 -Name <String> [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>]
 [-VariablePriority <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByValue
```
New-CMCollection -CollectionType <CollectionType> [-Comment <String>] -InputObject <IResultObject>
 -Name <String> [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>]
 [-VariablePriority <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById
```
New-CMCollection -CollectionType <CollectionType> [-Comment <String>] -LimitingCollectionId <String>
 -Name <String> [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>]
 [-VariablePriority <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a device or user collection.

The limiting collection determines which resources can be a member of the collection that you create.
For instance, when you use the **All Systems** collection as the limiting collection, since it's a device collection, the new device collection can include any device in the Configuration Manager hierarchy.

To scope the type of collection that you create, you can also use the [New-CMDeviceCollection](New-CMDeviceCollection.md) or [New-CMUserCollection](New-CMUserCollection.md) cmdlets.

After you create a collection, add resources to the collection with membership rules.
To add members to the collection, use one of the cmdlets to add membership rules, for example:

- [Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)
- [Add-CMUserCollectionQueryMembershipRule](Add-CMUserCollectionQueryMembershipRule.md)

For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a user collection

This command creates a user collection named **testUser** that sets the **All Users** collection as the limiting collection.

```powershell
New-CMCollection -CollectionType User -LimitingCollectionName "All Users" -Name "testUser"
```

### Example 2: Set the limiting collection through the pipeline

This command first uses the **Get-CMCollection** to get the **All Users** collection object. It then uses the pipeline operator to pass the object to the **New-CMCollection** cmdlet, which creates a collection named **testUser**. The limiting collection for the new **testUser** collection is the **All Users** collection.

```powershell
Get-CMCollection -Name "All Users" | New-CMCollection -Name "testUser" -CollectionType "User"
```

## PARAMETERS

### -CollectionType

Specify the type of collection to create. This parameter is functionally the same as using the [New-CMDeviceCollection](New-CMDeviceCollection.md) or [New-CMUserCollection](New-CMUserCollection.md) cmdlets.

```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases:
Accepted values: User, Device

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

Specify an object for the limiting collection. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: LimitingCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitingCollectionId

Specify the ID of the limiting collection. This value is the **CollectionID** property, for example, `XYZ00012` or `SMS00001`.

```yaml
Type: String
Parameter Sets: ById
Aliases: LimitToCollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionName

Specify the name of the limiting collection.

```yaml
Type: String
Parameter Sets: ByName
Aliases: LimitToCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name for the new collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

To create variables on a device collection, use the [New-CMDeviceCollectionVariable](New-CMDeviceCollectionVariable.md) cmdlet.

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

### IResultObject#SMS_Collection

## NOTES

For more information on this return object and its properties, see [SMS_Collection server WMI class](/mem/configmgr/develop/reference/core/clients/collections/sms_collection-server-wmi-class).

## RELATED LINKS

[Copy-CMCollection](Copy-CMCollection.md)
[Export-CMCollection](Export-CMCollection.md)
[Get-CMCollection](Get-CMCollection.md)
[Get-CMCollectionMember](Get-CMCollectionMember.md)
[Get-CMCollectionSetting](Get-CMCollectionSetting.md)
[Import-CMCollection](Import-CMCollection.md)
[Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md)
[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[New-CMDeviceCollectionVariable](New-CMDeviceCollectionVariable.md)

[New-CMDeviceCollection](New-CMDeviceCollection.md)
[New-CMUserCollection](New-CMUserCollection.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
