---
title: Get-CMOutOfBandServicePoint
titleSuffix: Configuration Manager
description: Gets an out of band service point.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMOutOfBandServicePoint

## SYNOPSIS
Gets an out of band service point.

## SYNTAX

### SearchByName
```
Get-CMOutOfBandServicePoint [-SiteCode <String>] [[-SiteSystemServerName] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMOutOfBandServicePoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOutOfBandServicePoint** cmdlet gets an out of band service point.
An out of band service point is a site system role that provisions and configures Intel Active Management Technology (AMT)-based computers for Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Get an out of band service point
```
PS C:\> Get-CMOutOfBandServicePoint -SiteSystemServerName "cmcen-dist02.tsqa.corp.contoso.com" -SiteCode "CM1" >>\Results\Get-CMOutOfBandServicePoint_data.txt"
```

This command get an out of band service point that is associated with the site system named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM and the site code CM1.
The command directs the output to the text file Get-CMOutOfBandServicePoint_data.txt.

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
Specifies the site code of the Configuration Manager site that hosts the site system role.

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
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

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

[Set-CMOutOfBandServicePoint](Set-CMOutOfBandServicePoint.md)

[Add-CMOutOfBandServicePoint](Add-CMOutOfBandServicePoint.md)

[Remove-CMOutOfBandServicePoint](Remove-CMOutOfBandServicePoint.md)


