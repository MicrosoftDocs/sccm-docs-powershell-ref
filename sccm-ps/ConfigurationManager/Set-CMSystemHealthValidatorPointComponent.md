<<<<<<< HEAD
---
title: Set-CMSystemHealthValidatorPointComponent
titleSuffix: Configuration Manager
description: Modifies settings of a Configuration Manager system health validator point.
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
online version: https://go.microsoft.com/fwlink/?linkid=834123
schema: 2.0.0
ms.assetid: 27842BB3-EBB9-41C0-9713-53C515D27E2B
>>>>>>> master
---

# Set-CMSystemHealthValidatorPointComponent

## SYNOPSIS
Modifies settings of a Configuration Manager system health validator point.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Set-CMSystemHealthValidatorPointComponent [-SiteCode <String>] [-ADQueryMins <Int32>]
 [-StatementOfHealthValidityHours <Int32>] [-UseDateTime <Boolean>] [-Date <DateTime>] [-Time <DateTime>]
 [-StatementOfHealthStartTime <DateTime>] [-DesignateActiveDirectoryForest <Boolean>] [-DomainSuffix <String>]
 [-PublishAccount <String>] [-QueryAccount <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMSystemHealthValidatorPointComponent -InputObject <IResultObject> [-ADQueryMins <Int32>]
 [-StatementOfHealthValidityHours <Int32>] [-UseDateTime <Boolean>] [-Date <DateTime>] [-Time <DateTime>]
 [-StatementOfHealthStartTime <DateTime>] [-DesignateActiveDirectoryForest <Boolean>] [-DomainSuffix <String>]
 [-PublishAccount <String>] [-QueryAccount <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSystemHealthValidatorPointComponent** cmdlet modifies settings of a system health validator point.
A system health validator point is a Microsoft System Center Configuration Manager site system role that evaluates system health information reported by Windows clients for security related compliance.

You can modify whether the system health validator point uses the current Active Directory forest or a designated forest.
You can specify the accounts that the component uses to publish and query Active Directory Domain Services (AD DS).
You can set the validity period for cached statements of health and whether to accept statements of health only after a specific time.
Any changes you make apply to all system health validator points in the System Center Configuration Manager site.

To specify a system health validator point to modify, specify a site code or name, or you can use the [Get-CMSystemHealthValidatorPointComponent](Get-CMSystemHealthValidatorPointComponent.md) cmdlet to get a system health validator point to modify.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Modify settings of a system health validator point by using a name
```
PS XYZ:\> Set-CMSystemHealthValidatorPointComponent -Name "SHVPC02.TSQA.Contoso.com" -QueryInterval 60 -ValidityPeriod 24
```

This command modifies settings of a system health validator point named SHVPC02.TSQA.Contoso.com.
The command changes the query interval to 60 minutes and the validity period to 24 hours.

## PARAMETERS

### -ADQueryMins


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: QueryInterval
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

### -Date
Specifies a date, as a DateTime object.
To obtain a DateTime object, use the Get-Date cmdlet.
For more information, type Get-Help Get-Date.

If you specify a value of $True for the UseDateTime parameter, a client must create a statement of health after the date and time specified by using this parameter and the *Time* parameter.
The date and time must be in the past.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DesignateActiveDirectoryForest
Indicates whether the site system server and the system health validator points are in different Active Directory forests.
If the value is $True, specify an Active Directory forest by using the *DomainSuffix* parameter.
If no trust relationship exists between the forests, you may need to specify accounts by using the *PublishAccount* and *QueryAccount* parameters.

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

### -DomainSuffix
Specifies a domain suffix for a designated Active Directory forest.
If no trust relationship exists between this forest and the site system server forest, you may need to specify accounts by using the *PublishAccount* and *QueryAccount* parameters.

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
Specifies a system health validator point object.
To obtain a system health validator point, use the [Get-CMSystemHealthValidatorPointComponent](Get-CMSystemHealthValidatorPointComponent.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -PublishAccount
Specifies a health state reference publishing account, in the format Domain\User.
If you do not specify an account, the component uses the site system server account.

You must specify an account if no trust relationship exists between the site server domain and the domain suffix specified in the *DomainSuffix* parameter or if there is a trust relationship, but the site system server account lacks Full Control permission for the System Management Active Directory container.

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

### -QueryAccount
Specifies an account, in the format Domain\User, that the system health validator point uses to query AD DS for state references.
If you do not specify an account, the component uses the site system server account.

You must specify an account if no trust relationship exists between the site server domain and the domain suffix specified in the *DomainSuffix* parameter.

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

### -SiteCode
Specifies a site code in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatementOfHealthStartTime


```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatementOfHealthValidityHours


```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CacheServerPollingMins, ValidityPeriod, SohValidityHours
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Time
Specifies a time, as a DateTime object.
To obtain a DateTime object, use the Get-Date cmdlet.

If you specify a value of $True for the UseDateTime parameter, a client must create a statement of health after the date and time specified by using this parameter and the *Date* parameter.
The date and time must be in the past.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseDateTime
Indicates whether a client must create a statement of health after a specific date and time.
If you select a value of $True, specify the date and time by using the *Date* and *Time* parameters.
The date and time must be in the past.
The default value for this parameter is $False.

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

[Get-CMSystemHealthValidatorPointComponent](Get-CMSystemHealthValidatorPointComponent.md)

[Set-CMCollectionMembershipEvaluationComponent](Set-CMCollectionMembershipEvaluationComponent.md)

[Set-CMEmailNotificationComponent](Set-CMEmailNotificationComponent.md)

[Set-CMManagementPointComponent](Set-CMManagementPointComponent.md)

[Set-CMSoftwareUpdatePointComponent](Set-CMSoftwareUpdatePointComponent.md)

[Set-CMStatusReportingComponent](Set-CMStatusReportingComponent.md)
