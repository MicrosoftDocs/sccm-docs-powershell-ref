---
author: aczechowski
description: Gets a Device Enrollment Manager.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMMdmEnrollmentManager
titleSuffix: Configuration Manager
---

# Get-CMMdmEnrollmentManager

## SYNOPSIS
Gets a Device Enrollment Manager.

## SYNTAX

### ByName (Default)
```
Get-CMMdmEnrollmentManager [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByValue
```
Get-CMMdmEnrollmentManager -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMMdmEnrollmentManger** cmdlet gets one or more Device Enrollment Managers.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Get a device enrollment manager by name
```
PS XYZ:\> Get-CMMdmEnrollmentManager -name "Contoso\User01"
```

This command gets the device enrollment manager named User01.

### Example 2: Get a device enrollment manager by ID
```
PS XYZ:\> Get-CMMdmEnrollmentManager -ID "1234567890"
```

This command gets the device enrollment manager named 1234567890.

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

### -Id
Specifies an array of Configuration Manager user IDs.

```yaml
Type: Int32[]
Parameter Sets: ByValue
Aliases: Ids, ResourceId, ResourceIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a Configuration Manager user.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_MDMDeviceEnrollmentManagers

## NOTES

## RELATED LINKS

[Add-CMMdmEnrollmentManager](Add-CMMdmEnrollmentManager.md)

[Remove-CMMdmEnrollmentManager](Remove-CMMdmEnrollmentManager.md)


