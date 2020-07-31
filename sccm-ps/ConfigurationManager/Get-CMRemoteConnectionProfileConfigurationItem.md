---
description: Gets a remote connection profile configuration item.
external help file: AdminUI.PS.Dcm-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMRemoteConnectionProfileConfigurationItem
---

# Get-CMRemoteConnectionProfileConfigurationItem

## SYNOPSIS
Gets a remote connection profile configuration item.

## SYNTAX

### ByValue (Default)
```
Get-CMRemoteConnectionProfileConfigurationItem [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMRemoteConnectionProfileConfigurationItem [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMRemoteConnectionProfileConfigurationItem [-Name] <String> [-Fast] [<CommonParameters>]
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

### -Fast
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
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
