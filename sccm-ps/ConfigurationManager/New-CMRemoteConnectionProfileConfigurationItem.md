---
description: Creates a remote connection profile.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMRemoteConnectionProfileConfigurationItem
---

# New-CMRemoteConnectionProfileConfigurationItem

## SYNOPSIS
Creates a remote connection profile.

## SYNTAX

```
New-CMRemoteConnectionProfileConfigurationItem [-Description <String>] [-Enable <Boolean>]
 [-EnableNla <Boolean>] [-EnablePrimaryUser <Boolean>] [-EnableTSConnection <Boolean>]
 [-EnableTSFirewallRule <Boolean>] -Name <String> [-RDGatewayServer <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMRemoteConnectionProfileConfigurationItem** cmdlet creates a remote connection profile.
Client computers use remote connection profiles to remotely connect to computers from outside the domain or over the Internet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a remote connection profile configuration item
```
PS XYZ:\> New-CMRemoteConnectionProfileConfigurationItem -Name "EuropeanRemoteConnections" -EnablePrimaryUsers $True -EnableTSConnection $True -EnableTSFirewallRule $True
```

This command creates a remote connection profile configuration item named EuropeanRemoteConnections.
For this item the *EnablePrimaryUsers*, *EnableTSConnection*, and *EnableTSFirewall* properties are all set to $True.

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
Specifies a description for a remote connection profile.

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

### -Enable
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableConnectionSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableNla
Indicates whether to allow connections only from computers that run Remote Desktop by using Network Level Authentication.

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

### -EnablePrimaryUser
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnablePrimaryUsers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableTSConnection
Indicates whether to allow remote connections to client computers.
If you specify a value for this parameter, you must specify values for the *EnablePrimaryUsers* and *EnableTSFirewallRule* parameters.

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

### -EnableTSFirewallRule
Indicates whether to allow Windows Firewall exceptions for connections in Windows domains and on private networks.
If you specify a value for this parameter, you must specify values for the *EnablePrimaryUsers* and *EnableTSConnections* parameters.

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

### -Name
Specifies a name for a remote connection profile.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RDGatewayServer
Specifies the host name and port of the Remote Desktop gateway server, for example, Boston.gateway.Contoso.com:8080.

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

### None

## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy

## NOTES

## RELATED LINKS

[Set-CMRemoteConnectionProfileConfigurationItem](Set-CMRemoteConnectionProfileConfigurationItem.md)


