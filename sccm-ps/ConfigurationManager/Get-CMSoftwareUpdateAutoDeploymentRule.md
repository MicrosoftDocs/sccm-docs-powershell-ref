---
author: aczechowski
description: Gets Configuration Manager deployment rules for automatic software updates.
external help file: AdminUI.PS.Sum.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Get-CMSoftwareUpdateAutoDeploymentRule
titleSuffix: Configuration Manager
---

# Get-CMSoftwareUpdateAutoDeploymentRule

## SYNOPSIS
Gets Configuration Manager deployment rules for automatic software updates.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateAutoDeploymentRule [[-Name] <String>] [-IsServicingPlan <Boolean>] [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateAutoDeploymentRule [-Id] <Int32[]> [-IsServicingPlan <Boolean>] [-Fast]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateAutoDeploymentRule** cmdlet gets specified Microsoft System Center Configuration Manager deployment rules for automatic software updates.

System Center Configuration Manager uses rules to manage automatic deployment of software updates.
When a rule runs, System Center Configuration Manager adds updates that qualify for the rule to a software update group.
The System Center Configuration Manager server downloads content files and copies them to distribution points, and then updates client computers.

You can specify rules by ID or by name.
You can use this cmdlet to get deployment rules for automatic software updates to use with other cmdlets, such as the Invoke-CMSoftwareUpdateAutoDeploymentRule cmdlet or the [Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

## EXAMPLES

### Example 1: Get a deployment rule by name
```
PS XYZ:\> Get-CMSoftwareUpdateAutoDeploymentRule -Name "Weekly Driver Updates"
```

This command gets a deployment rule named Weekly Driver Updates.

### Example 2: Get a deployment rule by ID
```
PS XYZ:\> Get-CMSoftwareUpdateAutoDeploymentRule -Id "16777217"
```

This command gets a deployment rule that has the ID 16777217.

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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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
Specifies an array of IDs for rules for automatic deployment of software updates.
This value is the **AutoDeploymentID** property of the deployment rule object.

```yaml
Type: Int32[]
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsServicingPlan
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

### -Name
Specifies a name of a rule for automatic deployment of software updates.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: 0
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

[Disable-CMSoftwareUpdateAutoDeploymentRule](Disable-CMSoftwareUpdateAutoDeploymentRule.md)

[Enable-CMSoftwareUpdateAutoDeploymentRule](Enable-CMSoftwareUpdateAutoDeploymentRule.md)

[Invoke-CMSoftwareUpdateAutoDeploymentRule](Invoke-CMSoftwareUpdateAutoDeploymentRule.md)

[New-CMSoftwareUpdateAutoDeploymentRule](New-CMSoftwareUpdateAutoDeploymentRule.md)

[Remove-CMSoftwareUpdateAutoDeploymentRule](Remove-CMSoftwareUpdateAutoDeploymentRule.md)

[Set-CMSoftwareUpdateAutoDeploymentRule](Set-CMSoftwareUpdateAutoDeploymentRule.md)


