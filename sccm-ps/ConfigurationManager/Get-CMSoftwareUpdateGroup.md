---
author: aczechowski
description: Gets software update groups.
external help file: AdminUI.PS.Sum.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMSoftwareUpdateGroup
titleSuffix: Configuration Manager
---

# Get-CMSoftwareUpdateGroup

## SYNOPSIS
Gets software update groups.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateGroup [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateGroup -Id <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateGroup** cmdlet gets one or more software update groups in Microsoft System Center Configuration Manager.
A software update group is a collection of one or more software updates.
You can add software updates to a software update group and then deploy the group to clients.
After you deploy a software update group, you can add new software updates to the group and System Center Configuration Manager automatically deploys them.

## EXAMPLES

### Example 1: Get software update groups
```
PS XYZ:\> Get-CMSoftwareUpdateGroup
```

This command gets all software update groups.

### Example 2: Get a software update group by using an ID
```
PS XYZ:\> Get-CMSoftwareUpdateGroup -Id "ST10000D"
```

This command gets a software update group that has the ID ST10000D.

### Example 3: Get a software update group by using a name
```
PS XYZ:\> Get-CMSoftwareUpdateGroup -Name "SUGroupD01"
```

This command gets a software update group object named SUGroupD01.

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
Specifies an array of IDs of software update groups.

```yaml
Type: Int32[]
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software update groups.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMSoftwareUpdateGroup](New-CMSoftwareUpdateGroup.md)

[Remove-CMSoftwareUpdateGroup](Remove-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdateGroup](Set-CMSoftwareUpdateGroup.md)


