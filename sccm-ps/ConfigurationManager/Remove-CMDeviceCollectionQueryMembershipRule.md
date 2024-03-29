---
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Remove-CMDeviceCollectionQueryMembershipRule
---

# Remove-CMDeviceCollectionQueryMembershipRule

## SYNOPSIS

Remove a query membership rule from a device collection.

## SYNTAX

### ByValue (Default)
```
Remove-CMDeviceCollectionQueryMembershipRule -InputObject <IResultObject> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMDeviceCollectionQueryMembershipRule -CollectionName <String> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Remove-CMDeviceCollectionQueryMembershipRule -CollectionId <String> -RuleName <String> [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a query membership rule from a device collection.
A _query_ rule lets you dynamically update the membership of a collection based on a query that is run on a schedule.
You can't remove query rules from the default collections. Any collection that you target should have an ID that starts with the site code, not `SMS`.
For more information, see [How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections).

When you remove a query membership rule from a collection, multiple resources may no longer be members of the collection. This action can cause any software or configuration deployment to not apply to the devices.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove the query membership rules for a device collection

This command removes the query membership rule named **TPM** from the device collection named **Windows 10 devices**.

```powershell
Remove-CMDeviceCollectionQueryMembershipRule -CollectionName "Windows 10 devices" -RuleName "TPM" -Force
```

## PARAMETERS

### -CollectionId

Specify the ID of the device collection to remove the rule. This value is the **CollectionID** property, for example, `XYZ00012`. Since you can't remove the query rules from default collections, this ID starts with the site code and not `SMS`.

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

Specify the name of the device collection to remove the rule.

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

### -Force

Run the command without asking for confirmation.

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

Specify an object for the device collection to remove the rule. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

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

Specify the name of the query rule to remove from the collection.

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

[Get-CMDeviceCollectionQueryMembershipRule](Get-CMDeviceCollectionQueryMembershipRule.md)
[Add-CMDeviceCollectionQueryMembershipRule](Add-CMDeviceCollectionQueryMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Remove-CMCollectionQueryMembershipRule](Remove-CMDeviceCollectionQueryMembershipRule.md)

[Remove-CMUserCollectionQueryMembershipRule](Remove-CMUserCollectionQueryMembershipRule.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
