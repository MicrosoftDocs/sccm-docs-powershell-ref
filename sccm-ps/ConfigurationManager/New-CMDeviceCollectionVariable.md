---
author: aczechowski
description: Creates a device collection variable.
external help file: AdminUI.PS.Collections.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMDeviceCollectionVariable
titleSuffix: Configuration Manager
---

# New-CMDeviceCollectionVariable

## SYNOPSIS
Creates a device collection variable.

## SYNTAX

### NewByValueMandatory (Default)
```
New-CMDeviceCollectionVariable -InputObject <IResultObject> -VariableName <String> [-Value <String>]
 [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewByIdMandatory
```
New-CMDeviceCollectionVariable -CollectionId <String> -VariableName <String> [-Value <String>]
 [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewByNameMandatory
```
New-CMDeviceCollectionVariable -CollectionName <String> -VariableName <String> [-Value <String>]
 [-IsMask <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMDeviceCollectionVariable** cmdlet creates a device collection variable.
You can use a device collection variable to define custom task sequence variables and their associated values to be used by the resources in a collection.
Task sequence variables are a set of name and value pairs that provide a mechanism to configure and customize the steps of a task sequence when the task sequence is deployed to a specific collection.

## EXAMPLES

### Example 1: Create a device collection variable
```
PS XYZ:\> $Collection = Get-CMCollection -Name "Device"
PS XYZ:\> New-CMDeviceCollectionVariable -Collection $Collection -VariableName "testTS" -Value "test001"
```

The first command gets the device collection object named Device and stores the object in the $Collection variable.

The second command creates a collection variable named testTS with the value test001 for the collection object stored in $Collection.

## PARAMETERS

### -CollectionId
Specifies the ID of a device collection.

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
Specifies the name of a device collection.

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

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
Specifies a device collection object.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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
Indicates whether the collection variable value displays in the Configuration Manager console.

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
Specifies a value for the collection variable.

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
Specifies a name for the collection variable.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Planning a Task Sequence Strategy in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=260806)

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollectionVariable](Get-CMDeviceCollectionVariable.md)

[Set-CMDeviceCollectionVariable](Set-CMDeviceCollectionVariable.md)

[Remove-CMDeviceCollectionVariable](Remove-CMDeviceCollectionVariable.md)

[Get-CMUserCollection](Get-CMUserCollection.md)


