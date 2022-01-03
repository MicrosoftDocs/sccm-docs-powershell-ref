---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Get-CMDeviceCollectionQueryMembershipRule
---

# Get-CMDeviceCollectionQueryMembershipRule

## SYNOPSIS

Get a query membership rule for a device collection.

## SYNTAX

### ByName (Default)
```
Get-CMDeviceCollectionQueryMembershipRule -CollectionName <String> [-RuleName <String>] [<CommonParameters>]
```

### ById
```
Get-CMDeviceCollectionQueryMembershipRule -CollectionId <String> [-RuleName <String>] [<CommonParameters>]
```

### ByValue
```
Get-CMDeviceCollectionQueryMembershipRule -InputObject <IResultObject> [-RuleName <String>]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more query membership rules for a device collection.
A _query_ rule lets you dynamically update the membership of a collection based on a query that is run on a schedule.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

For more information about membership rules, see [Introduction to collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/introduction-to-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all query membership rules for the All Systems collection

This command gets the query membership rules from the default device collection named **All Systems**.

```powershell
Get-CMDeviceCollectionQueryMembershipRule -CollectionName "All Systems"
```

### Example 2: View the query expression for a rule on the All Systems collection

This command gets the query membership rule named **All Systems** from the **All Systems** collection and returns the query expression.

```powershell
Get-CMDeviceCollectionQueryMembershipRule -CollectionId "SMS00001" -RuleName "All Systems" | Select-Object QueryExpression
```

## PARAMETERS

### -CollectionId

Specify the ID of the device collection to get the rule. This value is the **CollectionID** property, for example, `XYZ00012` or `SMS00001`.

```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of the device collection to get the rule.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for the device collection to get the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

### -RuleName

Specify the name of the query rule to get from the collection.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)
[Remove-CMDeviceCollectionQueryMembershipRule](Remove-CMDeviceCollectionQueryMembershipRule.md)

[Get-CMCollectionQueryMembershipRule](Get-CMCollectionQueryMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMUserCollectionQueryMembershipRule](Get-CMUserCollectionQueryMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
