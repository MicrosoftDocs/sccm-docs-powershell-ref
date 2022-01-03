---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Remove-CMDeviceCollectionVariable
---

# Remove-CMDeviceCollectionVariable

## SYNOPSIS

Remove a device collection variable.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMDeviceCollectionVariable -Collection <IResultObject> [-Force] -VariableName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMDeviceCollectionVariable -CollectionId <String> [-Force] -VariableName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMDeviceCollectionVariable -CollectionName <String> [-Force] -VariableName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a device collection variable.
Default collections can't have variables. Any collection that you target should have an ID that starts with the site code, not `SMS`.

For more information, see [How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a device collection variable

The first command gets the device collection object named **Device** and stores it in the **$Collection** variable.

The second command removes the device collection variable named **testTS** from the device collection stored in the **$Collection** variable.
Specifying the **Force** parameter indicates that you aren't prompted before the variable is removed.

```powershell
$Collection = Get-CMCollection -Name "Device"
Remove-CMDeviceCollectionVariable -Collection $Collection -VariableName "testTS" -Force
```

### Example 2: Remove all variables from a device collection

This example first uses the **Get-CMDeviceCollectionVariable** cmdlet to get all variables on the device collection **IT Servers** and stores the objects in the **vars** array variable. It then loops through each item in the array, and removes the variable by name.

The **Force** parameter is used so that you're not prompted to remove each variable.

```powershell
$collName = "IT servers"
$vars = Get-CMDeviceCollectionVariable -CollectionName $collName

foreach ( $var in $vars ) {
  Remove-CMDeviceCollectionVariable -CollectionName $collName -VariableName $var -Force
}
```

Since the **VariableName** parameter doesn't allow wildcards, use this process if you need to quickly clear all variables from a device collection.

## PARAMETERS

### -Collection

Specify a device collection object to remove its variables. To get this object, use the [Get-CMCollection](Get-CMCollection.md) or [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlets.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CollectionId

Specify the ID of a device collection to remove its variables. This value is the **CollectionID** property, for example, `XYZ00012`. Since you can't set variables on default collections, this value starts with the site code, not `SMS`.

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

Specify the name of a device collection to remove its variables.

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

### -Force

Forces the command to run without asking for user confirmation.

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

Specify the name of a collection variable to remove. This parameter doesn't accept wildcard characters.

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

[Get-CMDeviceCollectionVariable](Get-CMDeviceCollectionVariable.md)
[New-CMDeviceCollectionVariable](New-CMDeviceCollectionVariable.md)
[Set-CMDeviceCollectionVariable](Set-CMDeviceCollectionVariable.md)

[Get-CMCollection](Get-CMCollection.md)
[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Remove-CMDeviceVariable](Remove-CMDeviceVariable.md)

[How to set task sequence variables](/mem/configmgr/osd/understand/using-task-sequence-variables#bkmk_set)
