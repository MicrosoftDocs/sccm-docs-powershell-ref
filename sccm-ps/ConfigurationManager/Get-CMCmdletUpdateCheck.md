---
title: Get-CMCmdletUpdateCheck
titleSuffix: Configuration Manager
description: Gets a cmdlet update check configuration object.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMCmdletUpdateCheck

## SYNOPSIS
Gets a cmdlet update check configuration object.

## SYNTAX

### User (Default)
```
Get-CMCmdletUpdateCheck [-CurrentUser] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### System
```
Get-CMCmdletUpdateCheck [-System] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCmdletUpdateCheck** cmdlet gets an update check configuration object and indicates if user policy is being overridden by system policy.

**Note:** This cmdlet is deprecated starting with version 1610, and may be removed in a future release.

## EXAMPLES

### Example 1: Get the update check configuration
```
PS XYZ:\> Get-CMCmdletUpdateCheck -CurrentUser
```

This command gets the update check configuration for the current user.

## PARAMETERS

### -CurrentUser
Indicates that the update check configuration for the current user is returned.
This parameter lets you know if the system policy is overriding user policy.

```yaml
Type: SwitchParameter
Parameter Sets: User
Aliases: User
Required: False
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

### -System
Indicates that the update check for the system is returned.
This parameter lets you know what is being overridden by system policy.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.Common.Update.CMCmdletUpdateConfiguration

## NOTES

## RELATED LINKS

[Send-CMCmdletUpdateCheck](Send-CMCmdletUpdateCheck.md)

[Set-CMCmdletUpdateCheck](Set-CMCmdletUpdateCheck.md)
