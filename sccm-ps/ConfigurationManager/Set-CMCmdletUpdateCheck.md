---
title: Set-CMCmdletUpdateCheck
titleSuffix: Configuration Manager
description: Configures update check settings on a per-user or per-system basis.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Set-CMCmdletUpdateCheck

## SYNOPSIS
Configures update check settings on a per-user or per-system basis.

## SYNTAX

### Value (Default)
```
Set-CMCmdletUpdateCheck -InputObject <CMCmdletUpdateConfiguration> [-IsUpdateCheckEnabled <Boolean>]
 [-IsUpdateCheckEnabledForCmdlet <Boolean>] [-IsUpdateCheckEnabledForProvider <Boolean>]
 [-CheckMinimumMins <Int32>] [-CheckTimeoutSec <Int32>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### User
```
Set-CMCmdletUpdateCheck [-CurrentUser] [-IsUpdateCheckEnabled <Boolean>]
 [-IsUpdateCheckEnabledForCmdlet <Boolean>] [-IsUpdateCheckEnabledForProvider <Boolean>]
 [-CheckMinimumMins <Int32>] [-CheckTimeoutSec <Int32>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### System
```
Set-CMCmdletUpdateCheck [-System] [-IsUpdateCheckEnabled <Boolean>] [-IsUpdateCheckEnabledForCmdlet <Boolean>]
 [-IsUpdateCheckEnabledForProvider <Boolean>] [-CheckMinimumMins <Int32>] [-CheckTimeoutSec <Int32>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCmdletUpdateCheck** cmdlet configures update check settings on a per-user or per-system basis.
You must be running as an administrator to set system settings.

**Note:** This cmdlet is deprecated starting with version 1610, and may be removed in a future release.

## EXAMPLES

### Example 1: Disable an update check
```
PS C:\> $UpdateConfig = Get-CMCmdletUpdateCheck -CurrentUser
PS C:\> Set-CMCmdletUpdateCheck -InputObject $UpdateConfig -IsUpdateCheckEnabled $False -CheckMinimumMins 5
```

The first command gets the cmdlet update check configuration object for the current user and stores the object in the $UpdateConfig variable.

The second command disables update check for the update check configuration object stored in $UpdateConfig.

### Example 2: Pass an update check configuration object and disable it
```
PS C:\> Get-CMCmdletUpdateCheck -CurrentUser | Set-CMCmdletUpdateCheck -IsUpdateCheckEnabled $False -CheckMinimumMins 5
```

This command gets the cmdlet update check configuration object for the current user and uses the pipeline operator to pass the object to **Set-CmdletUpdateCheck**, which disables update check for the configuration object.

## PARAMETERS

### -CheckMinimumMins
Specifies the minimum number of minutes to wait before checking for a cmdlet update.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CheckIntervalMinutes, CheckIntervalMins, CheckMinimumMinutes
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckTimeoutSec
Specifies the number of seconds to wait before timing out while checking for a cmdlet update.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CheckTimeoutSeconds
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

### -CurrentUser
Indicates that the update check for the current user is returned.

```yaml
Type: SwitchParameter
Parameter Sets: User
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
Specifies a cmdlet update configuration object.
To obtain a cmdlet update configuration object, use the [Get-CMCmdletUpdateCheck](Get-CMCmdletUpdateCheck.md) cmdlet.

```yaml
Type: CMCmdletUpdateConfiguration
Parameter Sets: Value
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsUpdateCheckEnabled
Indicates whether update check is enabled.

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

### -IsUpdateCheckEnabledForCmdlet
Indicates whether update check is enabled for the Configuration ManagerWindows PowerShell cmdlets.

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

### -IsUpdateCheckEnabledForProvider
Indicates whether update check is enabled for the Configuration Manager provider.

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

### -PassThru
Returns an object representing the item with which you are working.
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

### -System
Indicates that the update check for the system is returned.

```yaml
Type: SwitchParameter
Parameter Sets: System
Aliases:
Required: True
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

[Get-CMCmdletUpdateCheck](Get-CMCmdletUpdateCheck.md)

[Send-CMCmdletUpdateCheck](Send-CMCmdletUpdateCheck.md)
