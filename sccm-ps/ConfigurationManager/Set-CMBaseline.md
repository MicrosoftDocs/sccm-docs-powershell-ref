<<<<<<< HEAD
---
title: Set-CMBaseline
titleSuffix: Configuration Manager
description: Changes the settings of configuration baselines.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: 2DFC0BFA-2097-4838-949D-94AB419A2BD7
online version: https://go.microsoft.com/fwlink/?linkid=833671
schema: 2.0.0
>>>>>>> master
---

# Set-CMBaseline

## SYNOPSIS
Changes the settings of configuration baselines.

## SYNTAX

### SetByIdMandatory (Default)
```
Set-CMBaseline -Id <Int32> [-NewName <String>] [-Description <String>] [-AddCategory <String[]>]
 [-RemoveCategory <String[]>] [-DesiredConfigurationDigestPath <String>] [-ClearRequiredConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearSoftwareUpdate] [-ClearBaseline] [-RemoveRequiredConfigurationItem <String[]>]
 [-RemoveProhibitedConfigurationItem <String[]>] [-RemoveOptionalConfigurationItem <String[]>]
 [-RemoveOSConfigurationItem <String[]>] [-RemoveSoftwareUpdate <String[]>] [-RemoveBaseline <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddOptionalConfigurationItem <String[]>] [-AddOSConfigurationItem <String[]>]
 [-AddSoftwareUpdate <String[]>] [-AddBaseline <String[]>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMBaseline -Name <String> [-NewName <String>] [-Description <String>] [-AddCategory <String[]>]
 [-RemoveCategory <String[]>] [-DesiredConfigurationDigestPath <String>] [-ClearRequiredConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearSoftwareUpdate] [-ClearBaseline] [-RemoveRequiredConfigurationItem <String[]>]
 [-RemoveProhibitedConfigurationItem <String[]>] [-RemoveOptionalConfigurationItem <String[]>]
 [-RemoveOSConfigurationItem <String[]>] [-RemoveSoftwareUpdate <String[]>] [-RemoveBaseline <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddOptionalConfigurationItem <String[]>] [-AddOSConfigurationItem <String[]>]
 [-AddSoftwareUpdate <String[]>] [-AddBaseline <String[]>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMBaseline -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-AddCategory <String[]>] [-RemoveCategory <String[]>] [-DesiredConfigurationDigestPath <String>]
 [-ClearRequiredConfigurationItem] [-ClearProhibitedConfigurationItem] [-ClearOptionalConfigurationItem]
 [-ClearOSConfigurationItem] [-ClearSoftwareUpdate] [-ClearBaseline]
 [-RemoveRequiredConfigurationItem <String[]>] [-RemoveProhibitedConfigurationItem <String[]>]
 [-RemoveOptionalConfigurationItem <String[]>] [-RemoveOSConfigurationItem <String[]>]
 [-RemoveSoftwareUpdate <String[]>] [-RemoveBaseline <String[]>] [-AddRequiredConfigurationItem <String[]>]
 [-AddProhibitedConfigurationItem <String[]>] [-AddOptionalConfigurationItem <String[]>]
 [-AddOSConfigurationItem <String[]>] [-AddSoftwareUpdate <String[]>] [-AddBaseline <String[]>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBaseline** cmdlet changes the settings of one or more configuration baselines in Microsoft System Center Configuration Manager.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Add a membership to a security scope of a configuration baseline
```
PS XYZ:\> Set-CMBaseline -SecurityScopeAction AddMembership -SecurityScopeName "SecScope02" -Name "BLineContoso01"
```

This command adds membership to the security scope named SecScope02 for the configuration baseline named BLineContoso01.

### Example 2: Remove membership from a security scope of a configuration baseline
```
PS XYZ:\> Set-CMBaseline -SecurityScopeAction RemoveMembership -SecurityScopeName "SecScope02" -Name "BLineContoso01"
```

This command removes membership to the security scope named SecScope02 for the configuration baseline named BLineContoso01.

## PARAMETERS

### -AddBaseline
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddBaselines

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddCategory
Specifies an array of names of configuration categories to add to the configuration baselines.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOSConfigurationItem
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddOSConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOptionalConfigurationItem
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddOptionalConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProhibitedConfigurationItem
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProhibitedConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRequiredConfigurationItem
```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddRequiredConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSoftwareUpdate
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddSoftwareUpdates

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearBaseline
 

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

### -ClearOSConfigurationItem
 

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

### -ClearOptionalConfigurationItem
 

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

### -ClearProhibitedConfigurationItem
 

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

### -ClearRequiredConfigurationItem
 

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

### -ClearSoftwareUpdate
 

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

### -Description
Specifies a description of the configuration baseline.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DesiredConfigurationDigestPath
Specifies a path to the configuration data stored as a digest.

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
Specifies an array of IDs of configuration baselines.

```yaml
Type: Int32
Parameter Sets: SetByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a CMBaseline object.
To obtain a CMBaseline object, use the [Get-CMBaseline](Get-CMBaseline.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of configuration baselines.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the configuration baseline.

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

### -RemoveBaseline
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveBaselines

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCategory
Specifies an array of names of configuration categories to remove from the configuration baselines.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOSConfigurationItem
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveOSConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOptionalConfigurationItem
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveOptionalConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProhibitedConfigurationItem
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProhibitedConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRequiredConfigurationItem
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveRequiredConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSoftwareUpdate
 

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveSoftwareUpdates

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMBaseline](Disable-CMBaseline.md)

[Enable-CMBaseline](Enable-CMBaseline.md)

[Export-CMBaseline](Export-CMBaseline.md)

[Get-CMBaseline](Get-CMBaseline.md)

[Import-CMBaseline](Import-CMBaseline.md)

[New-CMBaseline](New-CMBaseline.md)

[Remove-CMBaseline](Remove-CMBaseline.md)

[Get-CMBaselineXMLDefinition](Get-CMBaselineXMLDefinition.md)

[Get-CMBaselineSummarizationSchedule](Get-CMBaselineSummarizationSchedule.md)
