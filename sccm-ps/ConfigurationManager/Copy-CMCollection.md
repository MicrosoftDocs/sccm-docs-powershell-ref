---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Copy-CMCollection
---

# Copy-CMCollection

## SYNOPSIS

Copy a collection to a new one.

## SYNTAX

### ByName (Default)
```
Copy-CMCollection -Name <String> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Copy-CMCollection -Id <String> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValue
```
Copy-CMCollection -InputObject <IResultObject> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to clone an existing collection to a new copy.

For more information, see [How to manage collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/manage-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Copy-CMCollection -Name "testUser" -NewName "testUserNew"
```

This command exports the collection named testUser to a new collection named testUserNew.

## PARAMETERS

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

### -Id

Specify the ID of a collection to copy. This value is the **CollectionID** property, for example, `XYZ00012`.

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

### -InputObject

Specify a collection object to copy. To get this object, use the [Get-CMCollection](Get-CMCollection.md), [Get-CMDeviceCollection](Get-CMDeviceCollection.md), or [Get-CMUserCollection](Get-CMUserCollection.md) cmdlets.

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

### -Name

Specify the name of a collection to copy.

```yaml
Type: String
Parameter Sets: ByName
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specify the name of the new collection.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewCollectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_Collection
### IResultObject#SMS_Collection

## NOTES

For more information on this return object and its properties, see [SMS_Collection server WMI class](/mem/configmgr/develop/reference/core/clients/collections/sms_collectionsettings-server-wmi-class).

## RELATED LINKS

[Export-CMCollection](Export-CMCollection.md)
[Get-CMCollection](Get-CMCollection.md)
[Get-CMCollectionMember](Get-CMCollectionMember.md)
[Get-CMCollectionSetting](Get-CMCollectionSetting.md)
[Import-CMCollection](Import-CMCollection.md)
[Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md)
[New-CMCollection](New-CMCollection.md)
[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
