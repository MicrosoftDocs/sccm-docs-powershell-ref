---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMTSNetworkAdapterSetting

## SYNOPSIS
{{ Fill in the Synopsis }}

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
{{ Fill in the Description }}

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

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
{{ Fill Dns Description }}

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
{{ Fill EnableDnsRegistration Description }}

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
{{ Fill EnableFullDnsRegistration Description }}

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
{{ Fill EnableIpProtocolFiltering Description }}

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
{{ Fill EnableLmHosts Description }}

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
{{ Fill EnableTcpFiltering Description }}

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
{{ Fill EnableUdpFiltering Description }}

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
{{ Fill Gateway Description }}

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
{{ Fill IpAddress Description }}

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
{{ Fill IpProtocolFilterList Description }}

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
{{ Fill Metric Description }}

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
{{ Fill Name Description }}

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
{{ Fill TcpFilterPortList Description }}

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
{{ Fill TcpIpNetbiosOption Description }}

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
{{ Fill UdpFilterPortList Description }}

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
{{ Fill Wins Description }}

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

## RELATED LINKS
