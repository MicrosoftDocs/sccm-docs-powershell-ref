---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: New-CMDeviceCollectionVariable
---

# New-CMDeviceCollectionVariable

## SYNOPSIS

Create a device collection variable.

## SYNTAX

### NewByValueMandatory (Default)
```
New-CMDeviceCollectionVariable -InputObject <IResultObject> [-IsMask <Boolean>] [-Value <String>]
 -VariableName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewByIdMandatory
```
New-CMDeviceCollectionVariable -CollectionId <String> [-IsMask <Boolean>] [-Value <String>]
 -VariableName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewByNameMandatory
```
New-CMDeviceCollectionVariable -CollectionName <String> [-IsMask <Boolean>] [-Value <String>]
 -VariableName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a device collection variable.
You can use a device collection variable to define custom task sequence variables and their associated values to be used by the devices in a collection.
Task sequence variables are a set of name and value pairs that provide a mechanism to configure and customize the steps of a task sequence when the task sequence is deployed to a specific collection.

Default collections can't have variables. Any collection that you target should have an ID that starts with the site code, not `SMS`.

For more information, see [How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a device collection variable

The first command gets the device collection object named **Device** and stores it in the **$Collection** variable.

The second command creates a collection variable named **testTS** with the value **test001** for the collection object stored in **$Collection**.

```powershell
$Collection = Get-CMCollection -Name "Device"
New-CMDeviceCollectionVariable -Collection $Collection -VariableName "testTS" -Value "test001"
```

## PARAMETERS

### -CollectionId

Specify the ID of a device collection on which to create the variable. This value is the **CollectionID** property, for example, `XYZ00012`. Since you can't set variables on default collections, this value starts with the site code, not `SMS`.

```yaml
Type: String
Parameter Sets: NewByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a device collection on which to create the variable.

```yaml
Type: String
Parameter Sets: NewByNameMandatory
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

### -InputObject

Specify a device collection object on which to create the variable. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: NewByValueMandatory
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsMask

Set this parameter to `$true` to indicate that the variable value is hidden. Masked values aren't displayed in the Configuration Manager console, the **Value** property on the WMI class **SMS_CollectionVariable**, or the task sequence log file. The task sequence can still use the variable.

You can't unmask a variable once it's hidden. If you mask a variable's value, but then don't want it masked, you need to delete and recreate the variable.

If you don't include this parameter, values aren't masked by default.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value

Specify a value for the collection variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: VariableValue

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VariableName

Specify a name for the collection variable to create.

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

### IResultObject[]#SMS_CollectionSettings
### IResultObject#SMS_CollectionSettings

## NOTES

For more information on this return object and its properties, see [SMS_CollectionSettings server WMI class](/mem/configmgr/develop/reference/core/clients/collections/sms_collectionsettings-server-wmi-class).

## RELATED LINKS

[Get-CMDeviceCollectionVariable](Get-CMDeviceCollectionVariable.md)
[Remove-CMDeviceCollectionVariable](Remove-CMDeviceCollectionVariable.md)
[Set-CMDeviceCollectionVariable](Set-CMDeviceCollectionVariable.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[New-CMDeviceVariable](New-CMDeviceVariable.md)

[How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set)
