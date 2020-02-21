---
author: aczechowski
description: Creates a cloud management gateway.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMCloudManagementGateway
titleSuffix: Configuration Manager
---

# New-CMCloudManagementGateway

## SYNOPSIS
Creates a cloud management gateway.

## SYNTAX

```
New-CMCloudManagementGateway -SubscriptionId <String> [-GovernmentSubscription <Boolean>]
 -ManagementCertificatePath <String> [-Description <String>] -ServiceCName <String>
 -ServiceCertificatePath <String> -RootCertificatePath <String> [-TrafficOutGB <Int32>]
 [-TrafficWarningPct <Int32>] [-TrafficCriticalPct <Int32>] [-ManagementCertificatePassword <SecureString>]
 [-ServiceCertificatePassword <SecureString>] -Region <AzureRegion> [-VMInstanceCount <Int32>]
 [-CheckClientCertRevocation <Boolean>] [-EnvironmentSetting <AzureEnvironment>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -CheckClientCertRevocation
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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
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

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -EnvironmentSetting
{{ Fill EnvironmentSetting Description }}

```yaml
Type: AzureEnvironment
Parameter Sets: (All)
Aliases:
Accepted values: AzurePublicCloud, AzureUSGovernmentCloud

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -GovernmentSubscription
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

### -ManagementCertificatePassword
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementCertificatePath
```yaml
Type: String
Parameter Sets: (All)
Aliases: ManagementCertificate

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -Region
```yaml
Type: AzureRegion
Parameter Sets: (All)
Aliases:
Accepted values: AnywhereAsia, AnywhereEurope, AnywhereUS, EastAsia, EastUS, NorthCentralUS, NorthEurope, SouthCentralUS, SoutheastAsia, WestEurope, WestUS, WestUS2, WestCentralUS, USGovernmentIowa, USGovernmentVirginia, USGovernmentArizona, USGovernmentTexas, USDoDCentral, USDoDEast, AustraliaEast, AustraliaSoutheast, BrazilSouth, CanadaCentral, CanadaEast, CentralIndia, CentralUS, EastUS2, JapanEast, JapanWest, SouthIndia, UKSouth, UKWest, WestIndia, FranceSouth, FranceCentral, KoreaSouth, KoreaCentral, AustraliaCentral, AustraliaCentral2, ChinaEast, ChinaNorth, GermanyCentral, GermanyNortheast, SouthAfricaNorth, SouthAfricaWest

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootCertificatePath
```yaml
Type: String
Parameter Sets: (All)
Aliases: RootCertificate

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCName
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertificatePassword
```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertificatePath
```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceCertificate

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficCriticalPct
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficOutGB
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficWarningPct
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMInstanceCount
```yaml
Type: Int32
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_AzureService
IResultObject[]#SMS_SCI_SysResUse
IResultObject[]#SMS_Alert
IResultObject#SMS_Alert

## NOTES

## RELATED LINKS
