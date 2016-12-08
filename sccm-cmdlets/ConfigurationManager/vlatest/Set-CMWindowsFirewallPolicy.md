---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834164
schema: 2.0.0
ms.assetid: 4B32EE03-FD8B-4F78-9F32-258A1C20EB0A
---

# Set-CMWindowsFirewallPolicy

## SYNOPSIS
Changes settings of a Windows Firewall policy.

## SYNTAX

### SetByValue (Default)
```
Set-CMWindowsFirewallPolicy [-InputObject] <IResultObject> [-Priority <PriorityChangeType>]
 [-DomainTurnOnFirewall <SettingType>] [-PrivateTurnOnFirewall <SettingType>]
 [-PublicTurnOnFirewall <SettingType>] [-DomainBlockAllInboundTraffic <SettingType>]
 [-PrivateBlockAllInboundTraffic <SettingType>] [-PublicBlockAllInboundTraffic <SettingType>]
 [-DomainNotification <SettingType>] [-PrivateNotification <SettingType>] [-PublicNotification <SettingType>]
 [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>] [-DigestXml <String>]
 [-NewName <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMWindowsFirewallPolicy [-Priority <PriorityChangeType>] [-DomainTurnOnFirewall <SettingType>]
 [-PrivateTurnOnFirewall <SettingType>] [-PublicTurnOnFirewall <SettingType>]
 [-DomainBlockAllInboundTraffic <SettingType>] [-PrivateBlockAllInboundTraffic <SettingType>]
 [-PublicBlockAllInboundTraffic <SettingType>] [-DomainNotification <SettingType>]
 [-PrivateNotification <SettingType>] [-PublicNotification <SettingType>] [-Description <String>]
 [-Digest <ConfigurationItem>] [-DigestPath <String>] [-DigestXml <String>] [-Id] <Int32> [-NewName <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMWindowsFirewallPolicy [-Priority <PriorityChangeType>] [-DomainTurnOnFirewall <SettingType>]
 [-PrivateTurnOnFirewall <SettingType>] [-PublicTurnOnFirewall <SettingType>]
 [-DomainBlockAllInboundTraffic <SettingType>] [-PrivateBlockAllInboundTraffic <SettingType>]
 [-PublicBlockAllInboundTraffic <SettingType>] [-DomainNotification <SettingType>]
 [-PrivateNotification <SettingType>] [-PublicNotification <SettingType>] [-Description <String>]
 [-Digest <ConfigurationItem>] [-DigestPath <String>] [-DigestXml <String>] [-Name] <String>
 [-NewName <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMWindowsFirewallPolicy** cmdlet changes settings of one or more Windows Firewall policies for System Center 2016 Endpoint Protection in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Decrease the priority of a Windows Firewall policy by using a name
```
PS C:\> Set-CMWindowsFirewallPolicy -Priority Decrease -Name "WFPContoso01"
```

This command decreases the priority of the Windows Firewall policy named WFPContoso01.

### Example 2: Decrease the priority of a Windows Firewall policy by using an ID
```
PS C:\> Set-CMWindowsFirewallPolicy -Priority Decrease -Id "16777568"
```

This command decreases the priority of the Windows Firewall policy that has the ID 16777568.

### Example 3: Increase the priority of a Windows Firewall policy by using an object variable
```
PS C:\> $WFPobj=Get-CMWindowsFirewallPolicy -Id "16777568"
PS C:\> Set-CMWindowsFirewallPolicy -Priority Increase -InputObject $WFPobj
```

The first command gets the **CMWindowsFirewallPolicy** object that has the ID 16777568 and stores it in the $WFPobj variable.

The second command increases the priority of the Windows Firewall policy stored in the $WFPobj variable.

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
Specifies a description for the Windows Firewall policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digest


```yaml
Type: ConfigurationItem
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DigestPath


```yaml
Type: String
Parameter Sets: (All)
Aliases: DesiredConfigurationDigestPath
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DigestXml


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
Indicates that wildcard handling is disabled.

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

### -DomainBlockAllInboundTraffic
Specifies whether the firewall blocks all incoming traffic for a domain type network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainNotification


```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: DomainNotifications
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainTurnOnFirewall
Specifies whether to enable Windows Firewall for domain network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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
Specifies an array of IDs of firewall policies.

```yaml
Type: Int32
Parameter Sets: SetById
Aliases: CIId, CI_ID
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a CMWindowsFirewallPolicy object.
To obtain a CMWindowsFirewallPolicy object, use the [Get-CMWindowsFirewallPolicy](./Get-CMWindowsFirewallPolicy.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of firewall policy names.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the firewall policy.

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

### -PassThru
Returns an object representing the item with which you are working.
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

### -Priority
Specifies the priority of a firewall policy.
Valid values are: Increase and Decrease.

```yaml
Type: PriorityChangeType
Parameter Sets: (All)
Aliases:
Accepted values: Increase, Decrease
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateBlockAllInboundTraffic
Specifies whether the firewall blocks all incoming traffic for a private network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateNotification


```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: PrivateNotifications
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrivateTurnOnFirewall
Specifies whether to enable Windows Firewall for a private network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicBlockAllInboundTraffic
Specifies whether the firewall blocks all incoming traffic for a public network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNotification


```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: PublicNotifications
Accepted values: Yes, No, NotConfigured
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicTurnOnFirewall
Specifies whether to enable Windows Firewall for a public network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases:
Accepted values: Yes, No, NotConfigured
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

[New-CMWindowsFirewallPolicy](./New-CMWindowsFirewallPolicy.md)
