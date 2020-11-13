---
description: Creates a cloud management gateway.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMCloudManagementGateway
---

# New-CMCloudManagementGateway

## SYNOPSIS
Creates a cloud management gateway.

## SYNTAX

### Interactive
```
New-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-EnvironmentSetting <AzureEnvironment>] [-Force]
 [-GroupName <String>] [-IsUsingExistingGroup <Boolean>] [-Region <AzureRegion>]
 [-ServiceCertPassword <SecureString>] -ServiceCertPath <String> [-ServiceName <String>]
 [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>] [-StorageWarningPct <Int32>]
 [-SubscriptionId <String>] [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>]
 [-TrafficOutStopService <Boolean>] [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Non-Interactive
```
New-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-EnvironmentSetting <AzureEnvironment>] [-Force]
 -GroupName <String> [-Region <AzureRegion>] -ServerAppClientId <String> [-ServiceCertPassword <SecureString>]
 -ServiceCertPath <String> [-ServiceName <String>] [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>]
 [-StorageWarningPct <Int32>] -SubscriptionId <String> [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>]
 [-TrafficOutStopService <Boolean>] [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>]
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

### -CARootCert
{{ Fill CARootCert Description }}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: CARootCertification, CARootCertifications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CheckClientCertRevocation
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: VerifyClientCertificateRevocation

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

### -EnableCloudDPFunction
{{ Fill EnableCloudDPFunction Description }}

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

### -EnableStorageQuota
{{ Fill EnableStorageQuota Description }}

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

### -EnableTrafficOut
{{ Fill EnableTrafficOut Description }}

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

### -EnforceProtocol
{{ Fill EnforceProtocol Description }}

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

### -EnvironmentSetting
{{ Fill EnvironmentSetting Description }}

```yaml
Type: AzureEnvironment
Parameter Sets: (All)
Aliases: AzureEnvironmentOption
Accepted values: AzurePublicCloud, AzureUSGovernmentCloud

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
{{ Fill Force Description }}

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

### -GroupName
{{ Fill GroupName Description }}

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Non-Interactive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsUsingExistingGroup
{{ Fill IsUsingExistingGroup Description }}

```yaml
Type: Boolean
Parameter Sets: Interactive
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
Accepted values: EastUS, SouthCentralUS, WestEurope, SoutheastAsia, WestUS2, WestCentralUS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerAppClientId
{{ Fill ServerAppClientId Description }}

```yaml
Type: String
Parameter Sets: Non-Interactive
Aliases: ServerApplicationClientId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertPassword
{{ Fill ServiceCertPassword Description }}

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: ServiceCertificatePassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertPath
{{ Fill ServiceCertPath Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceCertificatePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
{{ Fill ServiceName Description }}

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

### -StorageCriticalPct
{{ Fill StorageCriticalPct Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StorageCriticalPercent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaGB
{{ Fill StorageQuotaGB Description }}

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

### -StorageWarningPct
{{ Fill StorageWarningPct Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StorageWarningPercent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Non-Interactive
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
Aliases: TrafficCriticalPercent

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

### -TrafficOutStopService
{{ Fill TrafficOutStopService Description }}

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

### -TrafficWarningPct
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TrafficWarningPercent

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

## NOTES

## RELATED LINKS
