---
description: Sets a software update.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSoftwareUpdate
---

# Set-CMSoftwareUpdate

## SYNOPSIS
Sets a software update.

## SYNTAX

### SetById (Default)
```
Set-CMSoftwareUpdate [-CustomSeverity <CustomSeverityType>] -Id <String> [-MaximumExecutionMins <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareUpdate [-CustomSeverity <CustomSeverityType>] [-MaximumExecutionMins <Int32>] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValue
```
Set-CMSoftwareUpdate [-CustomSeverity <CustomSeverityType>] -InputObject <IResultObject>
 [-MaximumExecutionMins <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdate** cmdlet changes configuration settings for a software update.
You can use this cmdlet to set the severity and the maximum run time for an update.
A software update is an update to Windows or other software that Configuration Manager applies to a collection of computers.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a software update and change its settings
```
PS XYZ:\> Get-CMSoftwareUpdate -Name "Update for Windows 10 (KB3106932)" | Set-CMSoftwareUpdate -MaximumExecutionMins 10 -CustomSeverity Critical
```

This command gets the software update object named Update for Windows 10 (KB3106932) and uses the pipeline operator to pass the object to **Set-CMSoftwareUpdate**, which sets the severity of the update to Critical and the maximum installation time to 10 minutes.

### Example 2: Modify software update settings
```
PS XYZ:\> Set-CMSoftwareUpdate -Id 16777979 -MaximumExecutionMins 10 -CustomSeverity Critical
```

This command gets the software update with the ID of 16777979 and sets the severity of the update to Critical and the maximum installation time to 10 minutes.

## PARAMETERS

### -CustomSeverity
Specifies the severity for the software update.
Valid values are:

- Critical
- Important
- Low
- Moderate
- None

```yaml
Type: CustomSeverityType
Parameter Sets: (All)
Aliases:
Accepted values: None, Low, Moderate, Important, Critical

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
Specifies the ID of software updates.

```yaml
Type: String
Parameter Sets: SetById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software update object.
To obtain a software update object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumExecutionMins
Specifies, in minutes, the maximum amount of time that a software update has to complete installation on client computers.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumExecutionMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a software update.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName

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

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)

[Save-CMSoftwareUpdate](Save-CMSoftwareUpdate.md)

[Sync-CMSoftwareUpdate](Sync-CMSoftwareUpdate.md)
