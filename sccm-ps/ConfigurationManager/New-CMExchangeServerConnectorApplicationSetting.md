<<<<<<< HEAD
---
title: New-CMExchangeServerConnectorApplicationSetting
titleSuffix: Configuration Manager
description: Creates application-related settings for a mobile device that uses a Exchange Server connector.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833666
schema: 2.0.0
ms.assetid: 7B26C797-B537-4CDE-A4FF-C9C58D05C29F
>>>>>>> master
---

# New-CMExchangeServerConnectorApplicationSetting

## SYNOPSIS
Creates application-related settings for a mobile device that uses a Exchange Server connector.

## SYNTAX

```
New-CMExchangeServerConnectorApplicationSetting [-UnsignedInstall <Boolean>] [-UnsignedApplication <Boolean>]
 [-BlockedApplication <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMExchangeServerConnectorApplicationSetting** cmdlet creates application-related settings for a mobile device that uses a Microsoft Exchange Server connector.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Set application options for an Exchange Server connector
```
PS XYZ:\> New-CMExchangeServerConnectorApplicationSetting -UnsignedApplication $False -UnsignedInstall $True -BlockedApplication "a1","a2"
```

This command sets these application options for an Exchange Server connector: 

- Allows the mobile device to install unsigned applications.
- Blocks unsigned applications from running on the mobile device.
- Blocks the two applications named a1 and a2 from running.

## PARAMETERS

### -BlockedApplication
Specifies an array of names of applications that the mobile device blocks from running.

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

### -UnsignedApplication
Indicates whether applications can run at the normal level on a mobile device.

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

### -UnsignedInstall
Indicates whether you can install unsigned applications on a mobile device.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMExchangeServerConnectorAccessRule](New-CMExchangeServerConnectorAccessRule.md)

[New-CMExchangeServerConnectorEmailManagementSetting](New-CMExchangeServerConnectorEmailManagementSetting.md)

[New-CMExchangeServerConnectorPasswordSetting](New-CMExchangeServerConnectorPasswordSetting.md)

[New-CMExchangeServerConnectorSecuritySetting](New-CMExchangeServerConnectorSecuritySetting.md)


