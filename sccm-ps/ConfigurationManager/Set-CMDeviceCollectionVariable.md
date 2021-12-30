---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Set-CMDeviceCollectionVariable
---

# Set-CMDeviceCollectionVariable

## SYNOPSIS

Configure a device collection variable.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDeviceCollectionVariable -InputObject <IResultObject> [-IsMask <Boolean>] [-NewVariableName <String>]
 [-NewVariableValue <String>] -VariableName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByIdMandatory
```
Set-CMDeviceCollectionVariable -CollectionId <String> [-IsMask <Boolean>] [-NewVariableName <String>]
 [-NewVariableValue <String>] -VariableName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMDeviceCollectionVariable -CollectionName <String> [-IsMask <Boolean>] [-NewVariableName <String>]
 [-NewVariableValue <String>] -VariableName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change a device collection variable.

Default collections can't have variables. Any collection that you target should have an ID that starts with the site code, not `SMS`.

For more information, see [How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change a variable name

The first command gets the device collection object named **Device** and stores it in the **$Collection** variable.

The second command changes the name of the collection variable **testTS** to **NewVariable**.

```powershell
$Collection = Get-CMCollection -Name "Device"
Set-CMDeviceCollectionVariable -Collection $Collection -VariableName "testTS" -NewVariableName "NewVariable"
```

### Example 2: Change a variable value

This command changes the value of the variable **testTS** on the **Device** collection. It sets the new variable value to **12**.

```powershell
Set-CMDeviceCollectionVariable -CollectionName "Device" -VariableName "testTS" -NewVariableValue 12
```

## PARAMETERS

### -CollectionId

Specify the ID of a device collection to configure a variable. This value is the **CollectionID** property, for example, `XYZ00012`. Since you can't set variables on default collections, this value starts with the site code, not `SMS`.

```yaml
Type: String
Parameter Sets: SetByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a device collection to configure a variable.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
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

Specify a device collection object to configure a variable. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
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

### -NewVariableName

Specify a new name for the collection variable. Use this parameter to rename the variable.

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

### -NewVariableValue

Specify a new value for the collection variable.

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

### -VariableName

Specify the name of the collection variable to change.

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

To set the variable priority, use the [Set-CMCollection](Set-CMCollection.md) cmdlet with the **VariablePriority** parameter. To view the current variable priority, use the [Get-CMCollectionSetting](Get-CMCollectionSetting.md) cmdlet.

## RELATED LINKS

[Get-CMDeviceCollectionVariable](Get-CMDeviceCollectionVariable.md)
[New-CMDeviceCollectionVariable](New-CMDeviceCollectionVariable.md)
[Remove-CMDeviceCollectionVariable](Remove-CMDeviceCollectionVariable.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Set-CMDeviceVariable](Set-CMDeviceVariable.md)

[How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set)
