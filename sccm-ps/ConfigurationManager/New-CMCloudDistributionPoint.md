---
external help file: AdminUI.PS.Content.dll-Help.xml
ms.assetid: C659F1EB-43D3-4DD1-8AA4-6645726C7091
online version: https://go.microsoft.com/fwlink/?linkid=833584
schema: 2.0.0
---

# New-CMCloudDistributionPoint

## SYNOPSIS
Creates a cloud distribution point.

## SYNTAX

```
New-CMCloudDistributionPoint -SubscriptionId <String> [-SiteCode <String>] -ManagementCertificatePath <String>
 [-Description <String>] -ServiceCName <String> -ServiceCertificatePath <String> [-StorageQuotaGB <Int32>]
 [-StorageWarningThreshold <Int32>] [-StorageCriticalThreshold <Int32>] [-TrafficOutGB <Int32>]
 [-TrafficWarningThreshold <Int32>] [-TrafficCriticalThreshold <Int32>]
 [-ManagementCertificatePassword <SecureString>] [-ServiceCertificatePassword <SecureString>] -Region <Region>
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCloudDistributionPoint** cmdlet creates a cloud distribution point in Microsoft System Center Configuration Manager.

In System Center Configuration Manager, you can use a cloud service in Azure to host a distribution point for storing files to download to clients.
You can send packages and apps to and host packages and apps in cloud distribution points.
For more information about cloud distribution points, see [Planning for Content Management in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266223) on TechNet.

## EXAMPLES

### Example 1: Create a cloud distribution point
```
PS C:\> New-CMCloudDistributionPoint -ManagementCertificatePath "C:\Certificates\Management.pfx" -Region "WestUS" -ServiceCertificatePath "C:\Certificates\Distribution.pfx" -ServiceCName "distribution-server.contoso.com" -SiteCode "ContosoSite"-SubscriptionID "81c87063-04a3-4abf-8e4c-736569bc1f60"
```

This command creates a distribution with the canonical name server.contoso.com.
The distribution point is located in the WestUS Azure region and is associated with the Azure subscription 81c87063-04a3-4abf-8e4c-736569bc1f60.

## PARAMETERS

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

### -Description
Specifies a description for a cloud distribution point.

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

### -ManagementCertificatePassword
Specifies a password for a management certificate.

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
Specifies a location for a management certificate.

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
Returns the current working object.
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

### -Region
Specifies a region.
This is the Azure region where you want to create the cloud service that hosts this distribution point.
The acceptable values for this parameter are:

- AnywhereAsia
- AnywhereEurope
- AnywhereUS
- EastAsia
- EastUS
- NorthCentralUS
- NorthEurope
- SouthCentralUS
- SoutheastAsia
- WestEurope
- WestUS

```yaml
Type: Region
Parameter Sets: (All)
Aliases: 
Accepted values: AnywhereAsia, AnywhereEurope, AnywhereUS, EastAsia, EastUS, NorthCentralUS, NorthEurope, SouthCentralUS, SoutheastAsia, WestEurope, WestUS

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceCName
Specifies an alias, or CName, for a service.

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
Specifies a password for a service certificate.

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
Specifies a location for a service certificate.

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

### -SiteCode
Specifies a Configuration Manager site code.

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

### -StorageCriticalThreshold
Specifies the percentage for a critical alert to occur, based on the storage alert threshold.

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

### -StorageQuotaGB
Specifies the threshold value, in gigabytes, that triggers errors or warnings for total content storage.

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

### -StorageWarningThreshold
Specifies the percentage for a warning alert to occur, based on the storage alert threshold.

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

### -SubscriptionId
Specifies a subscription ID for your Azure account.
To get a subscription ID, use the Azure Management Portal.

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

### -TrafficCriticalThreshold
Specifies the percentage for a critical alert to occur, based on the traffic out alert threshold.

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
Specifies the threshold value, in gigabytes, that triggers errors or warnings, for monthly traffic out of Azure Storage Service.

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

### -TrafficWarningThreshold
Specifies the percentage for a warning alert to occur, based on the traffic out alert threshold.

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

[Get-CMCloudDistributionPoint](Get-CMCloudDistributionPoint.md)

[Remove-CMCloudDistributionPoint](Remove-CMCloudDistributionPoint.md)

[Set-CMCloudDistributionPoint](Set-CMCloudDistributionPoint.md)

[Start-CMCloudDistributionPoint](Start-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](Stop-CMCloudDistributionPoint.md)


