---
title: Get-CMObjectLockDetails
titleSuffix: Configuration Manager
description: Gets object lock details.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMObjectLockDetails

## SYNOPSIS
Gets object lock details.

## SYNTAX

```
Get-CMObjectLockDetails [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMObjectLockDetails** cmdlet gets the object lock details for an object.

## EXAMPLES

### Example 1: Get object lock details by passing an application object through the pipeline
```
PS ABC:\> Get-CMApplication -Name "Application01" | Get-CMObjectLockDetails
```

This command gets the application object named Application01 and uses the pipeline operator to pass the object to **Get-CMObjectLockDetails**, which gets the object lock details for the application.

### Example 2: Get object lock details by getting an application object
```
PS ABC:\> $AppObject = Get-CMApplication -Name "testApp"
PS ABC:\> Get-CMObjectLockDetails -InputObject $AppObject
```

The first command gets the application object named testApp and stores the object in the $AppObject variable.

The second object gets the object lock details for the application stored in $AppObject.

## PARAMETERS

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
Specifies a Configuration Manager object output from another cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Lock-CMObject](Lock-CMObject.md)

[Unlock-CMObject](Unlock-CMObject.md)
