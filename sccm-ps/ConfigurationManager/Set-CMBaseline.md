---
description: Changes the settings of configuration baselines.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMBaseline
---

# Set-CMBaseline

## SYNOPSIS
Changes the settings of configuration baselines.

## SYNTAX

### SetByIdMandatory (Default)
```
Set-CMBaseline [-AddBaseline <String[]>] [-AddCategory <String[]>] [-AddOptionalConfigurationItem <String[]>]
 [-AddOSConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddSoftwareUpdate <String[]>] [-AllowComanagedClients <Boolean>]
 [-ClearBaseline] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearRequiredConfigurationItem] [-ClearSoftwareUpdate]
 [-Description <String>] [-DesiredConfigurationDigestPath <String>] -Id <Int32> [-NewName <String>] [-PassThru]
 [-RemoveBaseline <String[]>] [-RemoveCategory <String[]>] [-RemoveOptionalConfigurationItem <String[]>]
 [-RemoveOSConfigurationItem <String[]>] [-RemoveProhibitedConfigurationItem <String[]>]
 [-RemoveRequiredConfigurationItem <String[]>] [-RemoveSoftwareUpdate <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMBaseline [-AddBaseline <String[]>] [-AddCategory <String[]>] [-AddOptionalConfigurationItem <String[]>]
 [-AddOSConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddSoftwareUpdate <String[]>] [-AllowComanagedClients <Boolean>]
 [-ClearBaseline] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearRequiredConfigurationItem] [-ClearSoftwareUpdate]
 [-Description <String>] [-DesiredConfigurationDigestPath <String>] -Name <String> [-NewName <String>]
 [-PassThru] [-RemoveBaseline <String[]>] [-RemoveCategory <String[]>]
 [-RemoveOptionalConfigurationItem <String[]>] [-RemoveOSConfigurationItem <String[]>]
 [-RemoveProhibitedConfigurationItem <String[]>] [-RemoveRequiredConfigurationItem <String[]>]
 [-RemoveSoftwareUpdate <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMBaseline [-AddBaseline <String[]>] [-AddCategory <String[]>] [-AddOptionalConfigurationItem <String[]>]
 [-AddOSConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddSoftwareUpdate <String[]>] [-AllowComanagedClients <Boolean>]
 [-ClearBaseline] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearRequiredConfigurationItem] [-ClearSoftwareUpdate]
 [-Description <String>] [-DesiredConfigurationDigestPath <String>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-RemoveBaseline <String[]>] [-RemoveCategory <String[]>]
 [-RemoveOptionalConfigurationItem <String[]>] [-RemoveOSConfigurationItem <String[]>]
 [-RemoveProhibitedConfigurationItem <String[]>] [-RemoveRequiredConfigurationItem <String[]>]
 [-RemoveSoftwareUpdate <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBaseline** cmdlet changes the settings of one or more configuration baselines in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

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

### -AllowComanagedClients
Starting in version 1906, use this parameter to set the following option on the configuration baseline properties: **Always apply this baseline even for co-managed clients**


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

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

[Disable-CMBaseline](Disable-CMBaseline.md)

[Enable-CMBaseline](Enable-CMBaseline.md)

[Export-CMBaseline](Export-CMBaseline.md)

[Get-CMBaseline](Get-CMBaseline.md)

[Import-CMBaseline](Import-CMBaseline.md)

[New-CMBaseline](New-CMBaseline.md)

[Remove-CMBaseline](Remove-CMBaseline.md)

[Get-CMBaselineXMLDefinition](Get-CMBaselineXMLDefinition.md)

[Get-CMBaselineSummarizationSchedule](Get-CMBaselineSummarizationSchedule.md)
