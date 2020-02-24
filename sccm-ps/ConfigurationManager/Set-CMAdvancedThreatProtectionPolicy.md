---
author: aczechowski
description: Sets an advanced threat protection policy.
external help file: AdminUI.PS.Dcm.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMAdvancedThreatProtectionPolicy
titleSuffix: Configuration Manager
---

# Set-CMAdvancedThreatProtectionPolicy

## SYNOPSIS
Sets an advanced threat protection policy.

## SYNTAX

### SetByValue (Default)
```
Set-CMAdvancedThreatProtectionPolicy [-InputObject] <IResultObject> [-Description <String>]
 [-Digest <ConfigurationItem>] [-DigestPath <String>] [-DigestXml <String>] [-NewName <String>]
 [-FilePath <String>] [-SampleSharingType <SampleSharingType>]
 [-TelemetryReportingFrequencyType <TelemetryReportingFrequencyType>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMAdvancedThreatProtectionPolicy [-Id] <Int32> [-Description <String>] [-Digest <ConfigurationItem>]
 [-DigestPath <String>] [-DigestXml <String>] [-NewName <String>] [-FilePath <String>]
 [-SampleSharingType <SampleSharingType>] [-TelemetryReportingFrequencyType <TelemetryReportingFrequencyType>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetOrderById
```
Set-CMAdvancedThreatProtectionPolicy [-Id] <Int32> -Order <PriorityChangeType> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMAdvancedThreatProtectionPolicy [-Name] <String> [-Description <String>] [-Digest <ConfigurationItem>]
 [-DigestPath <String>] [-DigestXml <String>] [-NewName <String>] [-FilePath <String>]
 [-SampleSharingType <SampleSharingType>] [-TelemetryReportingFrequencyType <TelemetryReportingFrequencyType>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetOrderByName
```
Set-CMAdvancedThreatProtectionPolicy [-Name] <String> -Order <PriorityChangeType> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetOrderByValue
```
Set-CMAdvancedThreatProtectionPolicy [-InputObject] <IResultObject> -Order <PriorityChangeType> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
```yaml
Type: String
Parameter Sets: SetByValue, SetById, SetByName
Aliases: LocalizedDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digest
```yaml
Type: ConfigurationItem
Parameter Sets: SetByValue, SetById, SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DigestPath
```yaml
Type: String
Parameter Sets: SetByValue, SetById, SetByName
Aliases: DesiredConfigurationDigestPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DigestXml
```yaml
Type: String
Parameter Sets: SetByValue, SetById, SetByName
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

### -FilePath
```yaml
Type: String
Parameter Sets: SetByValue, SetById, SetByName
Aliases: ConfigurationFileLocation

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
```yaml
Type: Int32
Parameter Sets: SetById, SetOrderById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: SetByValue, SetOrderByValue
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SetByName, SetOrderByName
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
```yaml
Type: String
Parameter Sets: SetByValue, SetById, SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Order
```yaml
Type: PriorityChangeType
Parameter Sets: SetOrderById, SetOrderByName, SetOrderByValue
Aliases:
Accepted values: Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -SampleSharingType
```yaml
Type: SampleSharingType
Parameter Sets: SetByValue, SetById, SetByName
Aliases:
Accepted values: None, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TelemetryReportingFrequencyType
```yaml
Type: TelemetryReportingFrequencyType
Parameter Sets: SetByValue, SetById, SetByName
Aliases:
Accepted values: Normal, Expedited

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItem

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
