---
title: Add-CMSystemHealthValidatorPoint
titleSuffix: Configuration Manager
description: Adds a validator point for system health in Configuration Manager.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Add-CMSystemHealthValidatorPoint

## SYNOPSIS
Adds a validator point for system health in Configuration Manager.

## SYNTAX

### ByValue (Default)
```
Add-CMSystemHealthValidatorPoint -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMSystemHealthValidatorPoint [-SiteSystemServerName] <String> [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMSystemHealthValidatorPoint** cmdlet adds a validator point for system health in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Add a system health validator point to a server for a site
```
PS C:\>Add-CMSystemHealthValidatorPoint -SiteCode "CM4" -SiteSystemServerName "Test01.TSQA.Contoso.com"
```

This command adds a system health validator point to the server named Test01.TSQA.Contoso.com for the site that has the site code CM4.

## PARAMETERS

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
Parameter Sets: ByValue
Aliases: SiteServer
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code that identifies the Configuration Manager site that hosts this site system role.

```yaml
Type: String
Parameter Sets: ByName
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
Parameter Sets: ByName
Aliases: Name, ServerName
Required: True
Position: 0
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

[Get-CMSystemHealthValidatorPoint](Get-CMSystemHealthValidatorPoint.md)

[Remove-CMSystemHealthValidatorPoint](Remove-CMSystemHealthValidatorPoint.md)


