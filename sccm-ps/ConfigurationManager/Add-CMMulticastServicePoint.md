---
description: Adds a multicast service point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMMulticastServicePoint
---

# Add-CMMulticastServicePoint

## SYNOPSIS
Adds a multicast service point.

## SYNTAX

### ByValue (Default)
```
Add-CMMulticastServicePoint [-ClientTransferRate <NetworkProfile>] [-EndIPAddress <String>]
 [-EndUdpPort <Int32>] -InputObject <IResultObject> [-MaximumClientCount <Int32>] [-MinimumClientCount <Int32>]
 [-SessionStartDelayMins <Int32>] [-StartIPAddress <String>] [-StartUdpPort <Int32>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Add-CMMulticastServicePoint [-ClientTransferRate <NetworkProfile>] [-EndIPAddress <String>]
 [-EndUdpPort <Int32>] [-MaximumClientCount <Int32>] [-MinimumClientCount <Int32>]
 [-SessionStartDelayMins <Int32>] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-StartIPAddress <String>] [-StartUdpPort <Int32>] [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMMulticastServicePoint** cmdlet enables multicast to simultaneously send data to multiple clients on the distribution point.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a multicast service point by using the pipeline
```
PS XYZ:\> Get-CMDistributionPoint -SiteSystemServerName "server01.contoso.com" | Add-CMMulticastServicePoint -UserName "contoso\administrator" -StartIPAddress "224.0.1.0" -EndIPAddress "239.255.255.255" -StartUdpPort 64001 -EndUdpPort 65000 -ClientTransferRate "Profile100Mbps" -MaximumClientCount 100 -SessionStartDelayMins 15 -MinimumClientCount 20
```

This command gets the distribution point object with the site system server name server1.contoso.com and uses the pipeline operator to pass the object to **Add-CMMulticastServicePoint**.
**Add-CMMulticastServicePoint** enables multicast on the distribution point object using the administrator account, creating an IP address range of 224.0.1.0 to 239.255.255.255, and a UDP port range of 64001 to 65000.
The command also sets the minimum and maximum client count, and sets a start delay of 15 minutes.

### Example 2: Add a multicast service point
```
PS XYZ:\>Add-CMMulticastServicePoint -SiteSystemServerName "server02.contoso.com" -UserName "contoso\administrator" -StartIPAddress "224.0.1.0" -EndIPAddress "239.255.255.255" -StartUdpPort 64001 -EndUdpPort 65000 -ClientTransferRate "Profile100Mbps" -MaximumClientCount 100 -SessionStartDelayMins 15 -MinimumClientCount 20
```

This command enables multicast on the distribution point with the site system server name of server1.contoso.com using the administrator account.
The command creates an IP address range of 224.0.1.0 to 239.255.255.255, and a UDP port range of 64001 to 65000.
The command also sets the minimum and maximum client count, and sets a start delay of 15 minutes.

## PARAMETERS

### -ClientTransferRate
No longer used.
Transfer speed is dynamic.

Specifies the client transfer rate.
Valid values are:

- None
- Profile100Mbps
- Profile10Mbps
- Profile1Gbps
- ProfileCustom

```yaml
Type: NetworkProfile
Parameter Sets: (All)
Aliases:
Accepted values: None, ProfileCustom, Profile10Mbps, Profile100Mbps, Profile1Gbps

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

### -EndIPAddress
Specifies the ending IP address in the range of IP addresses that Configuration Manager uses to send data to the destination computers.

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

### -EndUdpPort
Specifies the ending port in the range of user datagram protocol (UDP) ports that Configuration Manager uses to send data to the destination computers.

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
Specifies a multicast service point object.
To obtain a multicast service point object, use the Get-CMMulticastServicePoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaximumClientCount
Specifies the maximum number of destination computers that can download the operating system from this distribution point.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MulticastMaximumClientCount

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinimumClientCount
Specifies the minimum number of requests that must be received before Configuration Manager starts to deploy the operating system.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MinimumSessionSize

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SessionStartDelayMins
Specifies the number of minutes that Configuration Manager waits before it responds to the first deployment request.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SessionStartDelayMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of the server that hosts a site system role.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartIPAddress
Specifies the starting IP address in the range of IP addresses that Configuration Manager uses to send data to the destination computers.

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

### -StartUdpPort
Specifies the starting port in the range of UDP ports that Configuration Manager uses to send data to the destination computers.

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

### -UserName
Specifies the name of the user that the distribution site system components use to connect to the primary site database.
If UserName is not specified, the cmdlet uses the computer account of the distribution point to the primary site database.

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

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMMulticastServicePoint](Get-CMMulticastServicePoint.md)

[Remove-CMMulticastServicePoint](Remove-CMMulticastServicePoint.md)

[Set-CMMulticastServicePoint](Set-CMMulticastServicePoint.md)


