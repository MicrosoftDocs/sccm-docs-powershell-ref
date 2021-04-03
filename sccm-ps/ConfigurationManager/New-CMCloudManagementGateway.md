---
description: Create a cloud management gateway.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: New-CMCloudManagementGateway
---

# New-CMCloudManagementGateway

## SYNOPSIS

Create a cloud management gateway.

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

Use this cmdlet to create a cloud management gateway (CMG) service in Azure. For more information on how to use this cmdlet to create a cloud management gateway (CMG), see [2010 release notes: Cloud management gateway](/powershell/sccm/2010-release-notes#cloud-management-gateway).

For more information, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

Starting in version 2010, the following parameters were removed from this cmdlet:

- GovernmentSubscription
- ManagementCertificatePassword
- ManagementCertificatePath
- PassThru
- RootCertificatePath
- ServiceCertificatePassword
- ServiceCertificatePath
- ServiceCName

For more information on the other changes to this cmdlet in version 2010, see [2010 release notes](/powershell/sccm/2010-release-notes#cloud-management-gateway).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
$Path = "c:\TestPath\RootCA.cer"
$Type = [Microsoft.ConfigurationManagement.AdminConsole.AzureServices.CertificateStore]::RootCA
$Cert =@{$Path = $Type}

$Password = "0HNy*c@63kAe" | ConvertTo-SecureString -AsPlainText -Force

New-CMCloudManagementGateway -ServiceCertPath "c:\TestPath\ServiceCert.pfx" -EnvironmentSetting AzurePublicCloud -SubscriptionId "e517b8cb-a969-4d1e-b2ea-ae1e6c052020" -ServiceCertPassword $Password -ServiceName "GraniteFalls.CloudApp.Net" -Description "EastUS CMG for Contoso" -Region EastUS -VMInstanceCount 2 -CARootCert $Cert -CheckClientCertRevocation $False -EnforceProtocol $True -IsUsingExistingGroup $true -GroupName "Resource group 1"
```

### Example 2

```powershell
New-CMCloudManagementGateway -ServiceCertPath "c:\TestPath\ServiceCert.pfx" -EnvironmentSetting AzurePublicCloud -SubscriptionId "e517b8cb-a969-4d1e-b2ea-ae1e6c052020" -ServiceCertPassword $Password -ServiceName "GraniteFalls.CloudApp.Net" -Description "EastUS CMG for Contoso" -Region EastUS -VMInstanceCount 2 -CARootCert $Cert -CheckClientCertRevocation $False -EnforceProtocol $True -GroupName "Resource group 1" -EnableCloudDPFunction $true -EnableTrafficOut $true -TrafficOutStopService $true -TrafficOutGB 10000 -TrafficWarningPct 50 -TrafficCriticalPct 90 -EnableStorageQuota $true -StorageQuotaGB 2000 -StorageWarningPct 50 -StorageCriticalPct 90 -Force
```

## PARAMETERS

### -CARootCert

Applies to version 2010 and later. Add root certificates to the cloud service.

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

Set this parameter to `true` to verify client certificate revocation. A certificate revocation list (CRL) must be publicly published for this verification to work. For more information, see [Publish the certificate revocation list](/mem/configmgr/core/clients/manage/cmg/security-and-privacy-for-cloud-management-gateway#bkmk_crl).

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

An optional description of the CMG, to better identify it in the Configuration Manager console.

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

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

Applies to version 2010 and later. Enable or disable the option to **Allow CMG to function as a cloud distribution point and serve content from Azure storage**.

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

Applies to version 2010 and later. Enable or disable the option to **Specify storage alert threshold**.

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

Applies to version 2010 and later. Enable or disable the option to **Turn on 14-day threshold and alerts for monitoring outbound data transfer**.

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

Applies to version 2010 and later. Enable or disable the option to **Enforce TLS 1.2**.

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

Specify Azure environment to deploy the CMG: in the global Azure cloud (`AzurePublicCloud`) or the Azure Government cloud (`AzureUSGovernmentCloud`).

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

Applies to version 2010 and later. Run the command without asking for confirmation. If the service certificate contains multiple DNS names, use this parameter to avoid warnings from the cmdlet.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

Applies to version 2010 and later. Specify the name of the Azure resource group.

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

Applies to version 2010 and later. Specify if the Azure resource group already exists.

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

Specify the Azure service region, for example: `WestUS2`.

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

Applies to version 2010 and later. Specify the client ID of the Azure AD server app. Use this parameter for non-user interaction mode. In the CMG properties, this value is the **Azure AD app name**.

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

Applies to version 2010 and later. Specify the password for the service certificate.

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

Applies to version 2010 and later. Specify the path to the service certificate. For more information, see [CMG server authentication certificate](/mem/configmgr/core/clients/manage/cmg/server-auth-cert).

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

Applies to version 2010 and later. Specify the Azure service name. If you don't specify this parameter, Configuration Manager uses the service certificate's first DNS name. If the certificate has more than one DNS name, use this parameter to specify which one to use.

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

Applies to version 2010 and later. Specify an integer value for the **Generate Critical alert (% of storage alert threshold)**. For example, `90`.

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

Applies to version 2010 and later. Specify an integer value for the **Storage alert threshold (GB)**. For example, `2`.

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

Applies to version 2010 and later. Specify an integer value for the **Generate Warning alert (% of storage alert threshold)**. For example, `50`.

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

Specify the ID of the Azure subscription where you want to deploy this new cloud service. The format of this value is a standard GUID.

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

If you enable alerts for monitoring outbound data transfer, specify the percentage of threshold for raising a **Critical** alert. This value is `90` by default.

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

If you enable storage alerts, use this parameter to specify the storage alert threshold in **GB**. The default value is `2`.

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

Applies to version 2010 and later. Enable or disable the option to **Stop this service when the critical threshold is exceeded**.

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

If you enable alerts for monitoring outbound data transfer, specify the percentage of threshold for raising a **Warning** alert. This value is `50` by default.

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

Specify the instance count of virtual machines for the CMG in Azure.

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

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

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

[Get-CMCloudManagementGateway](Get-CMCloudManagementGateway.md)
[Remove-CMCloudManagementGateway](Remove-CMCloudManagementGateway.md)
[Set-CMCloudManagementGateway](Set-CMCloudManagementGateway.md)
[Start-CMCloudManagementGateway](Start-CMCloudManagementGateway.md)
[Stop-CMCloudManagementGateway](Stop-CMCloudManagementGateway.md)
[Import-CMAADServerApplication](Import-CMAADServerApplication.md)

[Import-CMAADClientApplication](Import-CMAADClientApplication.md)

[New-CMCloudManagementAzureService](New-CMCloudManagementAzureService.md)

[New-CMCloudManagementGateway](New-CMCloudManagementGateway.md)

[Add-CMCloudManagementGatewayConnectionPoint](Add-CMCloudManagementGatewayConnectionPoint.md)

[Set-CMCloudManagementAzureService](Set-CMCloudManagementAzureService.md)

[CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview)
