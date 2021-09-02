---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# New-CMTSNetworkAdapterSetting

## SYNOPSIS

Create a settings object for a network adapter on the **Apply Network Settings** task sequence step.

## SYNTAX

```
New-CMTSNetworkAdapterSetting [-Dns <String[]>] [-EnableDnsRegistration] [-EnableFullDnsRegistration]
 [-EnableIpProtocolFiltering] [-EnableLmHosts] [-EnableTcpFiltering] [-EnableUdpFiltering]
 [-Gateway <String[]>] [-IpAddress <Hashtable[]>] [-IpProtocolFilterList <String[]>] [-Metric <Int32>]
 -Name <String> [-TcpFilterPortList <Int32[]>] [-TcpIpNetbiosOption <NetbiosOption>]
 [-UdpFilterPortList <Int32[]>] [-Wins <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a network adapter settings object. Use this object with the **AddAdapterSetting** parameter on the [New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md) or [Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md) cmdlets.

For more information, see [About task sequence steps: Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add network adapter settings for a connection with multiple addresses

This example first defines three array variables that define the multiple addresses. The **$dns** variable is an array with two DNS server addresses. The **$gw** variable is an array with two gateway addresses. The **$ip** variable is an array with two hashtables. Each hashtable defines an IP address and subnet mask pair.

The next line of the example uses the **New-CMTSNetworkAdapterSetting** cmdlet to create the network adapter settings object. It uses the defined variables, and sets several other options.

The final part of this example configures an existing **Apply Network Settings** step of a task sequence named **Default OS deployment**. It adds the network adapter settings to the step, and configures the DNS suffix.

```powershell
$dns = @("192.168.1.100","10.0.1.100")
$gw = @("192.168.1.1","10.0.1.1")

$ip = @(
    @{ IP = "192.168.1.42"; Mask = "255.255.255.0"; },
    @{ IP = "10.0.1.42"; Mask = "255.255.242.0"; }
)

$conn1 = New-CMTSNetworkAdapterSetting -Name "local connection" -Dns $dns -EnableDnsRegistration -EnableFullDnsRegistration -Gateway $gw -IpAddress $ip -TcpIpNetbiosOption DisableNetbiosOverTcpip

$tsNameOsd = "Default OS deployment"
$tsStepNameApplyNetSet = "Apply Network Settings"

Set-CMTSStepApplyNetworkSetting -TaskSequenceName $tsNameOsd -StepName $tsStepNameApplyNetSet -AddAdapterSetting $conn1 -DnsSuffix "corp.contoso.com"
```

## PARAMETERS

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

### -Dns

Specify one or more DNS server addresses in order of use.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DNSServerAddress, DNSServerAddresses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableDnsRegistration

Add this parameter to register this connection's addresses in DNS. This setting applies to all connections with TCP/IP enabled. To specify the DNS suffix, use the **DnsSuffix** parameter on the [New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md) or [Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md) cmdlets.

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

### -EnableFullDnsRegistration

Add this parameter to use the connection's DNS suffix in DNS registration. This setting applies to all connections with TCP/IP enabled. To specify the DNS suffix, use the **DnsSuffix** parameter on the [New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md) or [Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md) cmdlets.

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

### -EnableIpProtocolFiltering

Add this parameter to filter some IP protocols. To enable TCP/IP filtering, use the **EnableTcpIpFiltering** parameter on the [New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md) or [Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md) cmdlets.

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

### -EnableLmHosts

Add this parameter to enable LMHOSTS lookup.

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

### -EnableTcpFiltering

Add this parameter to filter some TCP ports. To enable TCP/IP filtering, use the **EnableTcpIpFiltering** parameter on the [New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md) or [Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md) cmdlets.

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

### -EnableUdpFiltering

Add this parameter to filter some UDP ports. To enable TCP/IP filtering, use the **EnableTcpIpFiltering** parameter on the [New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md) or [Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md) cmdlets.

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

### -Gateway

If this connection doesn't use DHCP, use this parameter to specify one or more gateway addresses.

If needed, use the **Metric** parameter. By default, the gateway uses an automatic metric.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: GatewayIpAddress, GatewayIpAddresses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpAddress

If this connection doesn't use DHCP, use this parameter to specify one or more IP addresses and corresponding subnet masks. The value is a hashtable. The first value is the `IP` and the second value is the `Mask`.

For example: `@{ IP = "192.168.1.42"; Mask = "255.255.255.0"; }`

If you need to specify more than one IP address and subnet mask combination, use an array of hashtables.

For example: `@( @{ IP = "192.168.1.42"; Mask = "255.255.255.0"; }, @{ IP = "10.0.1.42"; Mask = "255.255.242.0"; } )`

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: NetworkSettingIpAddress, NetworkSettingIpAddresses

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IpProtocolFilterList

When you use the **EnableIpProtocolFiltering** parameter, use this parameter to specify one or more IP protocols.

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

### -Metric

Specify the metric that indicates the cost of using the **Gateway**. If you don't specify this parameter, the gateway uses an automatic metric.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: GatewayCostMetric

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a unique name for this connection.

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

### -TcpFilterPortList

When you use the **EnableTcpFiltering** parameter, use this parameter to specify one or more TCP ports.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TcpIpNetbiosOption

Specify whether to enable or disable NetBIOS over TCP/IP.

```yaml
Type: NetbiosOption
Parameter Sets: (All)
Aliases:
Accepted values: Default, EnableNetbiosOverTcpip, DisableNetbiosOverTcpip

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UdpFilterPortList

When you use the **EnableUdpFiltering** parameter, use this parameter to specify one or more UDP ports.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Wins

Specify one or more WINS server addresses.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WinsServerAddress, WinsServerAddresses

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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_NetworkAdapterSettings

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_NetworkAdapterSettings server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_networkadaptersettings-server-wmi-class).

## RELATED LINKS

[New-CMTSStepApplyNetworkSetting](New-CMTSStepApplyNetworkSetting.md)
[Set-CMTSStepApplyNetworkSetting](Set-CMTSStepApplyNetworkSetting.md)

[About task sequence steps: Apply Network Settings](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_ApplyNetworkSettings)
