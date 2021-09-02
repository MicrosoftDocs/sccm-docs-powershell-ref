---
description: Changes settings of a Windows Firewall policy.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMWindowsFirewallPolicy
---

# Set-CMWindowsFirewallPolicy

## SYNOPSIS
Changes settings of a Windows Firewall policy.

## SYNTAX

### SetByValue (Default)
```
Set-CMWindowsFirewallPolicy [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-DomainBlockAllInboundTraffic <SettingType>] [-DomainNotification <SettingType>]
 [-DomainTurnOnFirewall <SettingType>] [-InputObject] <IResultObject> [-NewName <String>]
 [-PrivateBlockAllInboundTraffic <SettingType>] [-PrivateNotification <SettingType>]
 [-PrivateTurnOnFirewall <SettingType>] [-PublicBlockAllInboundTraffic <SettingType>]
 [-PublicNotification <SettingType>] [-PublicTurnOnFirewall <SettingType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMWindowsFirewallPolicy [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-DomainBlockAllInboundTraffic <SettingType>] [-DomainNotification <SettingType>]
 [-DomainTurnOnFirewall <SettingType>] [-Id] <Int32> [-NewName <String>]
 [-PrivateBlockAllInboundTraffic <SettingType>] [-PrivateNotification <SettingType>]
 [-PrivateTurnOnFirewall <SettingType>] [-PublicBlockAllInboundTraffic <SettingType>]
 [-PublicNotification <SettingType>] [-PublicTurnOnFirewall <SettingType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMWindowsFirewallPolicy [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-DomainBlockAllInboundTraffic <SettingType>] [-DomainNotification <SettingType>]
 [-DomainTurnOnFirewall <SettingType>] [-Name] <String> [-NewName <String>]
 [-PrivateBlockAllInboundTraffic <SettingType>] [-PrivateNotification <SettingType>]
 [-PrivateTurnOnFirewall <SettingType>] [-PublicBlockAllInboundTraffic <SettingType>]
 [-PublicNotification <SettingType>] [-PublicTurnOnFirewall <SettingType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetOrderById
```
Set-CMWindowsFirewallPolicy [-Id] <Int32> -Order <PriorityChangeType> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetOrderByValue
```
Set-CMWindowsFirewallPolicy [-InputObject] <IResultObject> -Order <PriorityChangeType> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetOrderByName
```
Set-CMWindowsFirewallPolicy [-Name] <String> -Order <PriorityChangeType> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMWindowsFirewallPolicy** cmdlet changes settings of one or more Windows Firewall policies for System Center 2016 Endpoint Protection in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Decrease the priority of a Windows Firewall policy by using a name
```
PS XYZ:\> Set-CMWindowsFirewallPolicy -Priority Decrease -Name "WFPContoso01"
```

This command decreases the priority of the Windows Firewall policy named WFPContoso01.

### Example 2: Decrease the priority of a Windows Firewall policy by using an ID
```
PS XYZ:\> Set-CMWindowsFirewallPolicy -Priority Decrease -Id "16777568"
```

This command decreases the priority of the Windows Firewall policy that has the ID 16777568.

### Example 3: Increase the priority of a Windows Firewall policy by using an object variable
```
PS XYZ:\> $WFPobj=Get-CMWindowsFirewallPolicy -Id "16777568"
PS XYZ:\> Set-CMWindowsFirewallPolicy -Priority Increase -InputObject $WFPobj
```

The first command gets the **CMWindowsFirewallPolicy** object that has the ID 16777568 and stores it in the $WFPobj variable.

The second command increases the priority of the Windows Firewall policy stored in the $WFPobj variable.

## PARAMETERS

### -Description
Specifies a description for the Windows Firewall policy.

```yaml
Type: String
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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

### -DomainBlockAllInboundTraffic
Specifies whether the firewall blocks all incoming traffic for a domain type network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
Aliases:
Accepted values: Yes, No, NotConfigured

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
Specifies an array of IDs of firewall policies.

```yaml
Type: Int32
Parameter Sets: SetById, SetOrderById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a CMWindowsFirewallPolicy object.
To obtain a CMWindowsFirewallPolicy object, use the [Get-CMWindowsFirewallPolicy](Get-CMWindowsFirewallPolicy.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue, SetOrderByValue
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
Parameter Sets: SetByName, SetOrderByName
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
Parameter Sets: SetByValue, SetById, SetByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Order
{{ Fill Order Description }}

```yaml
Type: PriorityChangeType
Parameter Sets: SetOrderById, SetOrderByValue, SetOrderByName
Aliases: Priority
Accepted values: Increase, Decrease

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -PrivateBlockAllInboundTraffic
Specifies whether the firewall blocks all incoming traffic for a private network location.
Valid values are:

- No
- Not Configured
- Yes

```yaml
Type: SettingType
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
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
Parameter Sets: SetByValue, SetById, SetByName
Aliases:
Accepted values: Yes, No, NotConfigured

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

### Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItem
### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMWindowsFirewallPolicy](New-CMWindowsFirewallPolicy.md)
