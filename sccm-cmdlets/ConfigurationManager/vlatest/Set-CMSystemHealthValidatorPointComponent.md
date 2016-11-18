---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 27842BB3-EBB9-41C0-9713-53C515D27E2B
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

To specify a system health validator point to modify, specify a site code or name, or you can use the Get-CMSystemHealthValidatorPointComponent cmdlet to get a system health validator point to modify.

## EXAMPLES

### Example 1: Modify settings of a system health validator point by using a name
```
PS C:\>Set-CMSystemHealthValidatorPointComponent -Name "SHVPC02.TSQA.Contoso.com" -QueryInterval 60 -ValidityPeriod 24
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
To obtain a system health validator point, use the **Get-CMSystemHealthValidatorPointComponent** cmdlet.

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

[Get-CMSystemHealthValidatorPointComponent](./Get-CMSystemHealthValidatorPointComponent.md)

[Set-CMCollectionMembershipEvaluationComponent](./Set-CMCollectionMembershipEvaluationComponent.md)

[Set-CMEmailNotificationComponent](./Set-CMEmailNotificationComponent.md)

[Set-CMManagementPointComponent](./Set-CMManagementPointComponent.md)

[Set-CMOutOfBandManagementComponent](./Set-CMOutOfBandManagementComponent.md)

[Set-CMSoftwareUpdatePointComponent](./Set-CMSoftwareUpdatePointComponent.md)

[Set-CMStatusReportingComponent](./Set-CMStatusReportingComponent.md)


