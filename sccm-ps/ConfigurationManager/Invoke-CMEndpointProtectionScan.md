---
description: Invokes a scan to detect malware on one or more devices in the Configuration Manager hierarchy.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Invoke-CMEndpointProtectionScan
---

# Invoke-CMEndpointProtectionScan

## SYNOPSIS
Invokes a scan to detect malware on one or more devices in the Configuration Manager hierarchy.

## SYNTAX

### SearchByValueMandatory (Default)
```
Invoke-CMEndpointProtectionScan -DeviceCollection <IResultObject> [-ScanType <ScanType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceValueMandatory
```
Invoke-CMEndpointProtectionScan -Device <IResultObject> [-ScanType <ScanType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Invoke-CMEndpointProtectionScan -DeviceCollectionId <String> [-ScanType <ScanType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMEndpointProtectionScan -DeviceCollectionName <String> [-ScanType <ScanType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceIdMandatory
```
Invoke-CMEndpointProtectionScan -DeviceId <String> [-ScanType <ScanType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeviceNameMandatory
```
Invoke-CMEndpointProtectionScan -DeviceName <String> [-ScanType <ScanType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Invoke-CMEndpointProtectionScan** cmdlet invokes a System Center 2016 Endpoint Protection scan that is outside of any scheduled scans.
You can specify the device or collection by using its name, ID, or by specifying an object that represents the device or collection.

For more information about how Configuration Manager supports Endpoint Protection, see [Endpoint Protection in Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Invoke a full Endpoint Protection scan
```
PS XYZ:\>Invoke-CMEndpointProtectionScan -DeviceName "CMCEN-DIST02" -ScanType Full
```

This command invokes a full Endpoint Protection scan of the device named CMCEN-DIST02.

## PARAMETERS

### -Device
Specifies the device that is scanned for malware.

```yaml
Type: IResultObject
Parameter Sets: SearchByDeviceValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DeviceCollection
Specifies an object that represents a device collection whose members are scanned for malware.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceCollectionId
Specifies the ID of a device collection whose members are scanned for malware.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceCollectionName
Specifies the name of a device collection whose members are scanned for malware.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceId
Specifies the ID of a device that is scanned for malware.

```yaml
Type: String
Parameter Sets: SearchByDeviceIdMandatory
Aliases: ResourceID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Specifies the name of a device that is scanned for malware.

```yaml
Type: String
Parameter Sets: SearchByDeviceNameMandatory
Aliases: Name

Required: True
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

### -ScanType
Specifies a full or a quick scan.
A full scan looks at every location on the device.
A quick scan looks at only those locations where malware is most likely to appear.
The acceptable values for this parameter are: Full and Quick.

```yaml
Type: ScanType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Quick

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Endpoint Protection in Configuration Manager](/mem/configmgr/protect/deploy-use/endpoint-protection)

[Get-CMEndpointProtectionPoint](Get-CMEndpointProtectionPoint.md)


