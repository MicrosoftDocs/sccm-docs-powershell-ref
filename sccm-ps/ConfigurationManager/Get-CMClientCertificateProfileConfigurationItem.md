---
title: Get-CMClientCertificateProfileConfigurationItem
titleSuffix: Configuration Manager
description: Gets a client certificate profile configuration item.
ms.date: 05/02/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Get-CMClientCertificateProfileConfigurationItem

## SYNOPSIS
Gets a client certificate profile configuration item.

## SYNTAX

### ByValue (Default)
```
Get-CMClientCertificateProfileConfigurationItem [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMClientCertificateProfileConfigurationItem [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMClientCertificateProfileConfigurationItem [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

