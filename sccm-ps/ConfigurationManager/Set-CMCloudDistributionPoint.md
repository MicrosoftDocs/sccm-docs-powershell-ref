---
external help file: AdminUI.PS.Content.dll-Help.xml
ms.assetid: F2F9DBD4-F429-4913-82E7-E3E160D4A926
online version: https://go.microsoft.com/fwlink/?linkid=833730
schema: 2.0.0
---

# Set-CMCloudDistributionPoint

## SYNOPSIS
Changes settings for a cloud-based distribution point.

## SYNTAX

### SetByValue (Default)
```
Set-CMCloudDistributionPoint -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-TrafficOutGB <Int32>] [-StorageQuotaGB <Int32>] [-StorageQuotaGrow <Boolean>]
 [-TrafficOutStopService <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMCloudDistributionPoint -Id <String> [-NewName <String>] [-Description <String>] [-TrafficOutGB <Int32>]
 [-StorageQuotaGB <Int32>] [-StorageQuotaGrow <Boolean>] [-TrafficOutStopService <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMCloudDistributionPoint -Name <String> [-NewName <String>] [-Description <String>] [-TrafficOutGB <Int32>]
 [-StorageQuotaGB <Int32>] [-StorageQuotaGrow <Boolean>] [-TrafficOutStopService <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMCloudDistributionPoint** cmdlet changes settings for a cloud-based distribution point.

In Microsoft System Center Configuration Manager, you can use a cloud service in Windows Azure to host a distribution point for storing files to download to clients.
You can send packages and apps to and host packages and apps in cloud distribution points. 
For more information about cloud distribution points, see [Planning for Content Management in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266223) on TechNet.

You can use the **Set-CMCloudDistributionPoint** cmdlet to specify storage alert thresholds and warning levels for content that you deploy to a cloud distribution point.
You can also use the cmdlet to configure settings that enable users and devices to access the content.
You can provide a name and description for the cloud distribution point.

## EXAMPLES

### Example 1: Set values for a distribution point
```
PS C:\> Set-CMCloudDistributionPoint -Id 16777237 -Description "Western distribution point" -Name "West01" -StorageQuotaInGB 50 -TrafficOutInGB 50
```

This command sets the description and name for a distribution point to the provided strings.
It also sets values for the storage quota and data transfer.

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

### -Id
Specifies an array of identifiers for one or more cloud distribution points.
You can use a comma-separated list.

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
Specifies a cloud distribution point object.
To obtain a cloud distribution point object, you can use the [Get-CMCloudDistributionPoint](Get-CMCloudDistributionPoint.md) cmdlet.

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
Specifies a name for a cloud distribution point.

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

### -NewName
Specifies a new name for the cloud-based distribution point.

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

### -StorageQuotaGB
Specifies the threshold value, in gigabytes, that triggers errors or warnings for total content storage.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: StorageQuotaInGB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageQuotaGrow
Specifies whether the storage quota can grow.
By default, the amount of stored data cannot exceed the value of the *StorageQuotaInGB* parameter.
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

### -TrafficOutGB
Specifies the threshold value, in gigabytes, that triggers errors or warnings, for monthly traffic out of Windows Azure Storage Service.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TrafficOutInGB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficOutStopService
Specifies whether Configuration Manager stops data transfers after the distribution point reaches the quota specified in the *TrafficOutInGB* parameter.
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

[Get-CMCloudDistributionPoint](Get-CMCloudDistributionPoint.md)

[New-CMCloudDistributionPoint](New-CMCloudDistributionPoint.md)

[Remove-CMCloudDistributionPoint](Remove-CMCloudDistributionPoint.md)

[Start-CMCloudDistributionPoint](Start-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](Stop-CMCloudDistributionPoint.md)
