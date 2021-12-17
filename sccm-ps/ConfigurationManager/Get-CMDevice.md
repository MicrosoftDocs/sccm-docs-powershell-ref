---
description: Get a Configuration Manager device.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
schema: 2.0.0
title: Get-CMDevice
---

# Get-CMDevice

## SYNOPSIS

Get a Configuration Manager device.

## SYNTAX

### ByName (Default)
```
Get-CMDevice [-CollectionMember] [-Fast] [-Name <String>] [-Resource] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMDevice -Collection <IResultObject> [-CollectionMember] [-Fast] [-Name <String>] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDevice -CollectionId <String> [-CollectionMember] [-Fast] [-Name <String>] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] [-CollectionMember] [-Fast] [-Resource] -ThreatId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] [-CollectionMember] [-Fast] [-Resource] -ThreatName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatoryForViewInfectedClients
```
Get-CMDevice [-CollectionId <String>] [-CollectionMember] [-Fast] -InputObject <IResultObject> [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByNameMandatory
```
Get-CMDevice [-CollectionMember] -CollectionName <String> [-Fast] [-Name <String>] [-Resource]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMDevice [-CollectionMember] [-Fast] [-Resource] -ResourceId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMDevice** cmdlet gets a Configuration Manager device. By default it queries the **SMS_CM_RES_COLL_SMS00001** class. You can use the **Resource** or **CollectionMember** parameters to change the query class. Depending upon your role-based access in the site, you may need to use one of these other parameters. For example, if you don't have access to SMS00001, then by default this cmdlet returns zero results.<!-- 12549811 -->

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get devices by collection ID

This command gets all the device objects in the device collection with the ID of **XYZ0004B**. It uses the **Select-Object** cmdlet to only display specific properties.

```powershell
Get-CMDevice -CollectionID "XYZ0004B" | Select-Object Name, ClientVersion, DeviceOS, IsActive, LastActiveTime, LastClientCheckTime, LastDDR, LastHardwareScan, LastPolicyRequest
```

```output
Name                : DEVICE-LT3
ClientVersion       : 5.00.9012.1020
DeviceOS            : Microsoft Windows NT Workstation 10.0 (Tablet Edition)
IsActive            : True
LastActiveTime      : 10/1/2020 23:29:34
LastClientCheckTime : 9/8/2020 18:38:10
LastDDR             : 9/30/2020 20:29:33
LastHardwareScan    : 9/30/2020 22:24:22
LastPolicyRequest   : 10/1/2020 23:29:34

Name                : DEVICE-LT2
ClientVersion       : 5.00.9030.1011
DeviceOS            : Microsoft Windows NT Workstation 10.0 (Tablet Edition)
IsActive            : True
LastActiveTime      : 10/2/2020 00:31:54
LastClientCheckTime : 9/30/2020 23:06:10
LastDDR             : 9/30/2020 19:44:46
LastHardwareScan    : 9/30/2020 01:15:52
LastPolicyRequest   : 10/2/2020 00:31:54
```

### Example 2: Get device resources by collection ID

This command is similar to the first example, but uses the **-Resource** parameter. When it queries a different class, it returns different properties for similar data.

```powershell
Get-CMDevice -CollectionID "XYZ0004B" -Resource | Select-Object Name, ClientVersion, OperatingSystemNameandVersion, Active, AgentName, AgentTime
```

```output
Name                          : DEVICE-LT3
ClientVersion                 : 5.00.9012.1020
OperatingSystemNameandVersion : Microsoft Windows NT Workstation 10.0 (Tablet Edition)
Active                        : 1
AgentName                     : {SMS_AD_SYSTEM_DISCOVERY_AGENT, SMS_AD_SECURITY_GROUP_DISCOVERY_AGENT,
                                MP_ClientRegistration, Heartbeat Discovery}
AgentTime                     : {2/28/2020 09:45:01, 10/2/2020 01:00:01, 9/21/2020 15:53:47, 9/30/2020 13:29:33}

Name                          : DEVICE-LT2
ClientVersion                 : 5.00.9030.1011
OperatingSystemNameandVersion : Microsoft Windows NT Workstation 10.0 (Tablet Edition)
Active                        : 1
AgentName                     : {SMS_AD_SYSTEM_DISCOVERY_AGENT, SMS_AD_SECURITY_GROUP_DISCOVERY_AGENT,
                                MP_ClientRegistration, Heartbeat Discovery}
AgentTime                     : {2/28/2020 09:45:01, 10/2/2020 01:00:01, 10/1/2020 14:03:56, 9/30/2020 12:44:46}
```

### Example 3: Get properties for a specific device

This command gets a specific device, and pipes the output through the **Select-Object** cmdlet to show only specific properties. Since it uses the **-Resource** parameter, the properties are specific to that class.

```powershell
Get-CMDevice -Name "DEVICE-LT2" -Resource | Select-Object Name, CPUType, DistinguishedName, HardwareID, IPAddresses
```

### Example 4: Get devices that aren't clients

This command uses the **-Fast** parameter to get all devices without lazy properties. It filters the list to only devices that aren't clients. It only displays the device name in the final list.

```powershell
Get-CMDevice -Fast | Where-Object { $_.IsClient -eq $false } | Select-Object Name
```

### Example 5: Get devices for a specific threat name

This command shows all devices on which Microsoft Defender has detected a specific threat. It only displays the name of the device.

```powershell
Get-CMDevice -ThreatName "Trojan:Win32/Wacatac.B!ml" | Select-Object Name
```

### Example 6: Get all devices with any detected malware

This command first uses the **Get-CMDetectedMalware** cmdlet to get all threats. It then parses through that list, and displays the name of devices with malware.

```powershell
$allMalware = Get-CMDetectedMalware
foreach ( $malware in $allMalware ) { Get-CMDevice -InputObject $malware | Select-Object Name }
```

## PARAMETERS

### -Collection

Use this parameter to get all devices from a device collection object. To get this object, use the [Get-CMDeviceCollection](Get-CMDeviceCollection.md) cmdlet.

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

### -CollectionId

Specify an ID for a device collection. For example, `XYZ0004B`.

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

```yaml
Type: String
Parameter Sets: SearchByIdMandatoryForViewInfectedClients, SearchByNameMandatoryForViewInfectedClients, SearchByValueMandatoryForViewInfectedClients
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionMember

Add this parameter to query the **SMS_R_UnknownSystem** and **SMS_R_System** classes for device information. These classes may be restricted by role-based access. These classes contain more detailed machine information.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CollectionMemberInstance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a device collection.

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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -InputObject

Specify a detected malware object. To get this object, use the [Get-CMDetectedMalware](Get-CMDetectedMalware.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatoryForViewInfectedClients
Aliases: Threat

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a device.

```yaml
Type: String
Parameter Sets: ByName, SearchByValueMandatory, SearchByIdMandatory, SearchByNameMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Resource

Add this parameter to query the **SMS_Resource** class for device information. This class shouldn't be restricted by role-based access. The output is the same as with the **Get-CMResource** cmdlet. This output has minimal properties for the device. For more detailed properties, don't add this parameter, or use the **CollectionMember** parameter.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ResourceInstance

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId

Specify the resource ID of a device. For example, `16780010`.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: Id, DeviceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreatId

Use this parameter to filter the devices that it returns to those devices with specific malware by ID. For example, `2147735505`. To get this threat ID, use the [Get-CMDetectedMalware](Get-CMDetectedMalware.md) cmdlet.

```yaml
Type: String
Parameter Sets: SearchByIdMandatoryForViewInfectedClients
Aliases: ThreatNameId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThreatName

Use this parameter to filter the devices that it returns to those devices with specific malware by name. For example, `Trojan:Win32/Wacatac.B!ml`. To get this threat name, use the [Get-CMDetectedMalware](Get-CMDetectedMalware.md) cmdlet.

```yaml
Type: String
Parameter Sets: SearchByNameMandatoryForViewInfectedClients
Aliases:

Required: True
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

### IResultObject[]#SMS_CombinedDeviceResources

### IResultObject#SMS_CombinedDeviceResources

## NOTES

For more information on this return object and its properties, see [SMS_CombinedDeviceResources server WMI class](/mem/configmgr/develop/reference/core/clients/collections/sms_combineddeviceresources-server-wmi-class).

## RELATED LINKS

[Get-CMResource](Get-CMResource.md)

[Approve-CMDevice](Approve-CMDevice.md)

[Block-CMDevice](Block-CMDevice.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Remove-CMDevice](Remove-CMDevice.md)

[Unblock-CMDevice](Unblock-CMDevice.md)
