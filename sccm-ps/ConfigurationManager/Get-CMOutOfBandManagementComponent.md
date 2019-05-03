---
title: Get-CMOutOfBandManagementComponent
titleSuffix: Configuration Manager
description: Gets an out of band management component.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMOutOfBandManagementComponent

## SYNOPSIS
Gets an out of band management component.

## SYNTAX

```
Get-CMOutOfBandManagementComponent [-SiteSystemServerName <String>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOutOfBandManagementComponent** cmdlet gets the site system computer that has the out of band management role.
The out of band management role manages computers that have the Intel vPro chip set and a version of Intel Active Management Technology (Intel AMT) that System Center Configuration Manager supports.
Out of band management lets you connect to a computer AMT management controller when the computer is turned off, in hibernation, or otherwise unresponsive through the operating system.

## EXAMPLES

### Example 1: Get an out of band management component by using a site code
```
PS C:\> Get-CMOutOfBandManagementComponent -SiteCode "CM4"
```

This command gets the out of band management component from the client site that has code CM4.

### Example 2: Get an out of band management component by using a site server name
```
PS C:\> Get-CMOutOfBandManagementComponent -SiteSystemServerName "condev-test04.tsqa.corp.contoso.com"
```

This command gets the out of band management component from the site server named condev-test04.tsqa.corp.contoso.com in the client site.

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

### -SiteCode
Specifies assigned site of a client by using a code.

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

### -SiteSystemServerName
Specifies an array of site system server names.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name
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



