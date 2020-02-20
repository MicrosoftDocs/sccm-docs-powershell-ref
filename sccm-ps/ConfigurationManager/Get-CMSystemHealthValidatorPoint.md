---
title: Get-CMSystemHealthValidatorPoint
titleSuffix: Configuration Manager
description: Gets a system health validator point for Configuration Manager.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMSystemHealthValidatorPoint

## SYNOPSIS
Gets a system health validator point for Configuration Manager.

## SYNTAX

### SearchByName
```
Get-CMSystemHealthValidatorPoint [-SiteCode <String>] [[-SiteSystemServerName] <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMSystemHealthValidatorPoint -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSystemHealthValidatorPoint** cmdlet gets a system health validator point for a Microsoft System Center Configuration Manager site.
This site system role validates statements of health from a server that is running Network Policy Server (NPS).

You can specify a validator point by site system name, site code, or both.
You can use this cmdlet with the [Remove-CMSystemHealthValidatorPoint](Remove-CMSystemHealthValidatorPoint.md) cmdlet.

## EXAMPLES

### Example 1: Get a validator point
```
PS XYZ:\> Get-CMSystemHealthValidatorPoint -SiteCode "CM1" -SiteSystemServerName "Test01.TSQA.Contoso.com"
```

This command gets a system health validator point.
The command specifies the site code and the name of the server that hosts that system role.

## PARAMETERS

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the host name for a system health validator point.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: Name, ServerName
Required: False
Position: 0
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

[Add-CMSystemHealthValidatorPoint](Add-CMSystemHealthValidatorPoint.md)

[Remove-CMSystemHealthValidatorPoint](Remove-CMSystemHealthValidatorPoint.md)


