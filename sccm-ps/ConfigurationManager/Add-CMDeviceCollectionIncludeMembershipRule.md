---
description: Adds an Include Collections membership rule to a device collection.
external help file: AdminUI.PS.Collections-help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMDeviceCollectionIncludeMembershipRule
---

# Add-CMDeviceCollectionIncludeMembershipRule

## SYNOPSIS
Adds an Include Collections membership rule to a device collection.

## SYNTAX

### ByNameAndName (Default)
```
Add-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionName <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndValue
```
Add-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameAndId
```
Add-CMDeviceCollectionIncludeMembershipRule -CollectionName <String> -IncludeCollectionId <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndValue
```
Add-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndId
```
Add-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionId <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdAndName
```
Add-CMDeviceCollectionIncludeMembershipRule -CollectionId <String> -IncludeCollectionName <String> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndValue
```
Add-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollection <IResultObject>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndId
```
Add-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionId <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueAndName
```
Add-CMDeviceCollectionIncludeMembershipRule -InputObject <IResultObject> -IncludeCollectionName <String>
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMDeviceCollectionIncludeMembershipRule** cmdlet adds an Include Collections membership rule to a device collection.
An Include Collections membership rule includes members of other device collections in the device collection where the rule is applied.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add an Include Collections membership rule
```
PS XYZ:\>Add-CMDeviceCollectionIncludeMembershipRule -CollectionName "Device" -IncludeCollectionName "All Systems"
```

This command adds the device collection named All Systems as an Include Collections membership rule associated with the device collection named Device.

### Example 2: Add an Include Membership rule to a collection by using the pipeline
```
PS XYZ:\> Get-CMCollection -Name "Device" | Add-CMDeviceCollectionIncludeMembershipRule -IncludeCollectionName "All Systems"
```

This command gets the collection object named Device and uses the pipeline operator to pass the object to **Add-CMDeviceCollectionIncludeMembershipRule**.
**Add-CMDeviceCollectionIncludeMembershipRule** adds the device collection named All Systems as an Include Collections membership rule associated with the device collection object.

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

### -IncludeCollection
Specifies a device collection object to include in the membership rule.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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
Specifies the ID of a device collection to include in the membership rule.

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
Specifies the name of a device collection to include in the membership rule.

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
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Introduction to Collections in Configuration Manager](https://go.microsoft.com/fwlink/p/?LinkID=259433)

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollectionIncludeMembershipRule](Get-CMDeviceCollectionIncludeMembershipRule.md)

[Remove-CMDeviceCollectionIncludeMembershipRule](Remove-CMDeviceCollectionIncludeMembershipRule.md)


