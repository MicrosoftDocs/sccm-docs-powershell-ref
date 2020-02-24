---
author: aczechowski
description: Sets a client setting enrollment.
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMClientSettingEnrollment
titleSuffix: Configuration Manager
---

# Set-CMClientSettingEnrollment

## SYNOPSIS
Sets a client setting enrollment.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingEnrollment [-EnableDevice <Boolean>] [-EnableModernDevice <Boolean>]
 [-EnrollmentProfileName <String>] [-ModernEnrollmentProfileName <String>] [-IntervalModernMins <Int32>]
 [-IntervalDeviceHr <Int32>] [-IntervalDeviceMins <Int32>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingEnrollment [-EnableDevice <Boolean>] [-EnableModernDevice <Boolean>]
 [-EnrollmentProfileName <String>] [-ModernEnrollmentProfileName <String>] [-IntervalModernMins <Int32>]
 [-IntervalDeviceHr <Int32>] [-IntervalDeviceMins <Int32>] [-DefaultSetting] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingEnrollment [-EnableDevice <Boolean>] [-EnableModernDevice <Boolean>]
 [-EnrollmentProfileName <String>] [-ModernEnrollmentProfileName <String>] [-IntervalModernMins <Int32>]
 [-IntervalDeviceHr <Int32>] [-IntervalDeviceMins <Int32>] -InputObject <IResultObject> [-PassThru]
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

### -DefaultSetting
```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

Required: True
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

### -EnableDevice
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableDeviceEnrollment

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableModernDevice
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableModernDeviceEnrollment

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnrollmentProfileName
```yaml
Type: String
Parameter Sets: (All)
Aliases: DeviceEnrollmentProfileName, MobileDeviceEnrollmentProfileName

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
```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IntervalDeviceHr
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PollingIntervalForDeviceHour

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IntervalDeviceMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PollingIntervalForDeviceMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IntervalModernMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PollingIntervalForModernDeviceMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ModernEnrollmentProfileName
```yaml
Type: String
Parameter Sets: (All)
Aliases: ModernDeviceEnrollmentProfileName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

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

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
