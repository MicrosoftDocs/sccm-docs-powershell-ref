---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: B2A455ED-6B5A-403B-B34F-63958235F370
online version: https://go.microsoft.com/fwlink/?linkid=833738
schema: 2.0.0
---

# New-CMRemoteConnectionProfileConfigurationItem

## SYNOPSIS
Creates a remote connection profile.

## SYNTAX

```
New-CMRemoteConnectionProfileConfigurationItem -Name <String> [-Description <String>]
 [-EnableTSConnection <Boolean>] [-EnableNla <Boolean>] [-EnablePrimaryUser <Boolean>]
 [-EnableTSFirewallRule <Boolean>] [-Enable <Boolean>] [-RDGatewayServer <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMRemoteConnectionProfileConfigurationItem** cmdlet creates a remote connection profile.
Client computers use remote connection profiles to remotely connect to computers from outside the domain or over the Internet.

## EXAMPLES

### Example 1: Create a remote connection profile configuration item
```
PS C:\> New-CMRemoteConnectionProfileConfigurationItem -Name "EuropeanRemoteConnections" -EnablePrimaryUsers $True -EnableTSConnection $True -EnableTSFirewallRule $True
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

[Set-CMRemoteConnectionProfileConfigurationItem](Set-CMRemoteConnectionProfileConfigurationItem.md)


