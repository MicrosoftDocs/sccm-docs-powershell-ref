---
title: Add-CMOutOfBandServicePoint
titleSuffix: Configuration Manager
description: Adds an out of band service point to Configuration Manager.
ms.date: 04/29/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Add-CMOutOfBandServicePoint

## SYNOPSIS
Adds an out of band service point to Configuration Manager.

## SYNTAX

### OutOfBandServicePointByValue (Default)
```
Add-CMOutOfBandServicePoint -ErrorRetryCount <Int32> -ErrorRetryMinutesDelay <Int32>
 -TransmissionThreadCount <Int32> -TransmissionStartMins <Int32> [-Thumbprint <String>]
 [-EnableCrlChecking <Boolean>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### OutOfBandServicePoint
```
Add-CMOutOfBandServicePoint [-SiteSystemServerName] <String> [-SiteCode <String>] -ErrorRetryCount <Int32>
 -ErrorRetryMinutesDelay <Int32> -TransmissionThreadCount <Int32> -TransmissionStartMins <Int32>
 [-Thumbprint <String>] [-EnableCrlChecking <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### OutOfBandServicePointWithCert
```
Add-CMOutOfBandServicePoint [-SiteSystemServerName] <String> [-SiteCode <String>] -ErrorRetryCount <Int32>
 -ErrorRetryMinutesDelay <Int32> -TransmissionStartMins <Int32> -Certificate <X509Certificate2>
 -EnableCrlChecking <Boolean> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### OutOfBandServicePointWithCertByValue
```
Add-CMOutOfBandServicePoint -ErrorRetryCount <Int32> -ErrorRetryMinutesDelay <Int32>
 -TransmissionStartMins <Int32> -Certificate <X509Certificate2> -EnableCrlChecking <Boolean>
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMOutOfBandServicePoint** cmdlet adds an out of band service point to Microsoft System Center Configuration Manager.
An out of band service point is a site system role that provisions and configures Intel Active Management Technology (AMT)-based computers for Microsoft System Center Configuration Manager.

For more information about out of band management for System Center Configuration Manager see [Introduction to Out of Band Management in Configuration Manager](http://go.microsoft.com/fwlink/?linkid=252706) in the TechNet library.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Add an out of band service point by using a site code
```
PS XYZ:\>Add-CMOutOfBandServicePoint -SiteSystemServerName "cmcen-dist02.tsqa.contoso.com" -SiteCode "CM2" -Thumbprint "916EC36F1068D47DE48A02A788A9DB137CD0B674"
```

This command adds an out of band service point to the Microsoft System Center Configuration Manager site that has the site code named CM2 on the site system named cmcen-dist02.tsqa.contoso.com.

## PARAMETERS

### -Certificate
Specifies the trusted root certificate for out of band management.

```yaml
Type: X509Certificate2
Parameter Sets: OutOfBandServicePointWithCert, OutOfBandServicePointWithCertByValue
Aliases: 
Required: True
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

### -EnableCrlChecking
Indicates whether the out of band service point verifies the certificate revocation list (CRL) for the provisioning certificate.

```yaml
Type: Boolean
Parameter Sets: OutOfBandServicePointByValue, OutOfBandServicePoint
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Boolean
Parameter Sets: OutOfBandServicePointWithCert, OutOfBandServicePointWithCertByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorRetryCount


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumSendRetryCount
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ErrorRetryMinutesDelay


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: RetryIntervalMinutes
Required: True
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
Parameter Sets: OutOfBandServicePointByValue, OutOfBandServicePointWithCertByValue
Aliases: SiteServer
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for the Configuration Manager site that hosts this site system role.

```yaml
Type: String
Parameter Sets: OutOfBandServicePoint, OutOfBandServicePointWithCert
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
Parameter Sets: OutOfBandServicePoint, OutOfBandServicePointWithCert
Aliases: Name, ServerName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Thumbprint
Specifies the thumbprint of the AMT provisioning certificate.

```yaml
Type: String
Parameter Sets: OutOfBandServicePointByValue, OutOfBandServicePoint
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TransmissionStartMins


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ThreadsOffset, TransmissionStartMinutesInterval
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TransmissionThreadCount


```yaml
Type: Int32
Parameter Sets: OutOfBandServicePointByValue, OutOfBandServicePoint
Aliases: MaximumThreadCount
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

[Get-CMOutOfBandServicePoint](Get-CMOutOfBandServicePoint.md)

[Remove-CMOutOfBandServicePoint](Remove-CMOutOfBandServicePoint.md)

[Set-CMOutOfBandServicePoint](Set-CMOutOfBandServicePoint.md)


