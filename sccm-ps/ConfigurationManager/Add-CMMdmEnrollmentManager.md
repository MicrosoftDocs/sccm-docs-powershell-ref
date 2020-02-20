---
author: aczechowski
description: Adds a Device Enrollment Manager.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Add-CMMdmEnrollmentManager
titleSuffix: Configuration Manager
---

# Add-CMMdmEnrollmentManager

## SYNOPSIS
Adds a Device Enrollment Manager.

## SYNTAX

### ByValue (Default)
```
Add-CMMdmEnrollmentManager -InputObject <IResultObject[]> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Add-CMMdmEnrollmentManager -Id <Int32[]> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMMdmEnrollmentManager -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMMdmEnrollmentManager** cmdlet adds a Device Enrollment Manager to the Microsoft Intune subscription.

## EXAMPLES

### Example 1: Add a device enrollment manager using the pipeline
```
PS XYZ:\> Get-CMUser -Name "Contoso\User01" | Add-CMMdmEnrollmentManager
```

This command gets the user object named User01 and uses the pipeline operator to pass the object to **Add-CMMdmEnrollmentManager**, which adds the user as a device enrollment manager.

### Example 2: Add a device enrollment manager by name
```
PS XYZ:\> Add-CMMdmEnrollmentManager -Name "Contoso\User02"
```

This command adds the user named User02 as a device enrollment manager.

## PARAMETERS

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

### -Id
Specifies an array of Configuration Manager user IDs.

```yaml
Type: Int32[]
Parameter Sets: ById
Aliases: Ids

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an array of user objects.
To obtain a user object, use the [Get-CMUser](Get-CMUser.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: ByValue
Aliases: User, EnrollmentManager, Users, EnrollmentManagers

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a Configuration Manager user.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### IResultObject#SMS_MDMDeviceEnrollmentManagers

## NOTES

## RELATED LINKS

[Get-CMMdmEnrollmentManager](Get-CMMdmEnrollmentManager.md)

[Get-CMUser](Get-CMUser.md)

[Remove-CMMdmEnrollmentManager](Remove-CMMdmEnrollmentManager.md)


