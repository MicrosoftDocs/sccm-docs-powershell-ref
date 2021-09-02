---
description: Configure a cloud management gateway (CMG).
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: Set-CMCloudManagementGateway
---

# Set-CMCloudManagementGateway

## SYNOPSIS

Configure a cloud management gateway (CMG).

## SYNTAX

### SetByValue (Default)
```
Set-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-Force] -InputObject <IResultObject> [-PassThru]
 [-RemoveCertThumbprints <String[]>] [-ServiceCertPassword <SecureString>] [-ServiceCertPath <String>]
 [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>] [-StorageWarningPct <Int32>]
 [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>] [-TrafficOutStopService <Boolean>]
 [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-Force] -Id <String> [-PassThru]
 [-RemoveCertThumbprints <String[]>] [-ServiceCertPassword <SecureString>] [-ServiceCertPath <String>]
 [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>] [-StorageWarningPct <Int32>]
 [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>] [-TrafficOutStopService <Boolean>]
 [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCloudManagementGateway [-CARootCert <Hashtable>] [-CheckClientCertRevocation <Boolean>]
 [-Description <String>] [-EnableCloudDPFunction <Boolean>] [-EnableStorageQuota <Boolean>]
 [-EnableTrafficOut <Boolean>] [-EnforceProtocol <Boolean>] [-Force] -Name <String> [-PassThru]
 [-RemoveCertThumbprints <String[]>] [-ServiceCertPassword <SecureString>] [-ServiceCertPath <String>]
 [-StorageCriticalPct <Int32>] [-StorageQuotaGB <Int32>] [-StorageWarningPct <Int32>]
 [-TrafficCriticalPct <Int32>] [-TrafficOutGB <Int32>] [-TrafficOutStopService <Boolean>]
 [-TrafficWarningPct <Int32>] [-VMInstanceCount <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure a cloud management gateway (CMG).

For more information, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the CMG alerts configuration

```powershell
Set-CMCloudManagementGateway -Name "GraniteFalls" -EnableTrafficOut $true -TrafficOutGB 10000 -TrafficWarningPct 50 -TrafficCriticalPct 90 -EnableStorageQuota $true -StorageQuotaGB 2000 -StorageWarningPct 50 -StorageCriticalPct 90
```

### Example 2: Change the number of virtual machines for the CMG service

This example targets the CMG named **GraniteFalls** and changes the number of VMs to `4`.

```powershell
Set-CMCloudManagementGateway -Name "GraniteFalls" -VMInstancesCount 4
```

### Example 3: Enable the CMG to serve content from Azure storage

```powershell
Set-CMCloudManagementGateway -Name "GraniteFalls" -EnableCloudDPFunction $true
```

### Example 4: Add two new certificate authorities

```powershell
$path1 = "folder\root.cer"
$type1 = [Microsoft.ConfigurationManagement.AdminConsole.AzureServices.CertificateStore]::RootCA

$path2 = "folder\intermediate.cer"
$type2 = [Microsoft.ConfigurationManagement.AdminConsole.AzureServices.CertificateStore]::IntermediateCA

$cert = @{$path1 = $type1; $path2 = $type2}

Set-CMCloudManagementGateway -Name "GraniteFalls" -CARootCert $cert
```

### Example 5: Update the CMG server authentication certificate

This example targets the CMG named **GraniteFalls** and updates the CMG server authentication certificate.

```powershell
Set-CMCloudManagementGateway -Name "GraniteFalls" -ServiceCertPath "c:\TestPath\NewServiceCert.pfx" -ServiceCertPassword (ConvertTo-SecureString -String "tX*xJ11Nuo^B" -AsPlainText -Force)
```

### Example 6: Remove a root certificate from a CMG

```powershell
Set-CMCloudManagementGateway -Name "GraniteFalls" -RemoveCertThumbprints "A7CBA0014DEF847593569D05003D5B96A1D6A627"
```

## PARAMETERS

### -CARootCert

Add root certificates to the cloud service.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: CARootCertificate, CARootCertificates

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
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description of this CMG service to better identify it.

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

### -Force

Run the command without asking for confirmation. If the service certificate contains multiple DNS names, use this parameter to avoid warnings from the cmdlet.

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

### -Id

Specify the site's ID for the Azure service. The **Id** is the integer value stored in the site database for the service. For example, run the following SQL query, and look at the **ID** column: `select * from Azure_CloudService`.

```yaml
Type: String
Parameter Sets: SetById
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a CMG object to configure. To get this object, use the [Get-CMCloudManagementGateway](Get-CMCloudManagementGateway.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the CMG to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -RemoveCertThumbprints

Applies to version 2010 and later. Specify one or more certificate thumbprints to remove them as root or intermediate certificate authorities from the CMG.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCertPassword

Applies to version 2006 and later. Specify the password for the certificate in the **-ServiceCertPath**.

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

Applies to version 2006 and later. Specify the path to the service certificate. For more information, see [CMG server authentication certificate](/mem/configmgr/core/clients/manage/cmg/server-auth-cert).

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceCertificatePath

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

### -TrafficCriticalPct

If you enable alerts for monitoring outbound data transfer, specify the percentage of threshold for raising a **Critical** alert. This value is `90` by default.

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
Aliases: StopTrafficOutService

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
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMInstanceCount

Applies to version 2010 and later. Specify the instance count of virtual machines.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: VMInstancesCount

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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMCloudManagementGateway](Get-CMCloudManagementGateway.md)
[New-CMCloudManagementGateway](New-CMCloudManagementGateway.md)
[Remove-CMCloudManagementGateway](Remove-CMCloudManagementGateway.md)
[Start-CMCloudManagementGateway](Start-CMCloudManagementGateway.md)
[Stop-CMCloudManagementGateway](Stop-CMCloudManagementGateway.md)

[CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview)
