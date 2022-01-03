---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Get-CMDeviceCollectionVariable
---

# Get-CMDeviceCollectionVariable

## SYNOPSIS

Get a device collection variable.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMDeviceCollectionVariable -CollectionName <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMDeviceCollectionVariable -Collection <IResultObject> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeviceCollectionVariable -CollectionId <String> [-VariableName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the task sequence variables on a device collection.
Default collections can't have variables. Any collection that you target should have an ID that starts with the site code, not `SMS`.

For more information, see [How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a device collection variable by name

This command gets the collection variable named testTS for the device collection named Device.

```powershell
Get-CMDeviceCollectionVariable -CollectionName "DeviceCollection02" -VariableName "testTS"
```

### Example 2: Get all unmasked variables for a collection

This example gets all variables from the collection **IT servers**, and filters the list to only the variables that aren't hidden. It then shows the name and value for each variable in a table.

```powershell
Get-CMDeviceCollectionVariable -CollectionName "IT servers" | Where-Object { -not $_.IsMasked } | Select-Object Name, Value
```

## PARAMETERS

### -Collection

Specify a device collection object to get its variables. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specify the ID of a device collection to get its variables. This value is the **CollectionID** property, for example, `XYZ00012`. Since you can't set variables on default collections, this value starts with the site code, not `SMS`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a device collection to get its variables.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
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

### -VariableName

Specify the name of a collection variable to get.

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

### None

## OUTPUTS

### IResultObject[]#SMS_CollectionVariable
### IResultObject#SMS_CollectionVariable

## NOTES

For more information on this return object and its properties, see [SMS_CollectionVariable server WMI class](/mem/configmgr/develop/reference/osd/sms_collectionvariable-server-wmi-class).

## RELATED LINKS

[New-CMDeviceCollectionVariable](New-CMDeviceCollectionVariable.md)
[Remove-CMDeviceCollectionVariable](Remove-CMDeviceCollectionVariable.md)
[Set-CMDeviceCollectionVariable](Set-CMDeviceCollectionVariable.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMDeviceVariable](Get-CMDeviceVariable.md)

[How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set)
