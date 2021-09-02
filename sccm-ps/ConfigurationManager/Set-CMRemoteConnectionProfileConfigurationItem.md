---
description: Modifies a remote connection profile.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMRemoteConnectionProfileConfigurationItem
---

# Set-CMRemoteConnectionProfileConfigurationItem

## SYNOPSIS
Modifies a remote connection profile.

## SYNTAX

### SetByValue (Default)
```
Set-CMRemoteConnectionProfileConfigurationItem [-Enable <Boolean>] [-EnableNla <Boolean>]
 [-EnablePrimaryUser <Boolean>] [-EnableTSConnection <Boolean>] [-EnableTSFirewallRule <Boolean>]
 [-InputObject] <IResultObject> [-RDGatewayServer <String>] [-Description <String>]
 [-Digest <ConfigurationItem>] [-DigestPath <String>] [-DigestXml <String>] [-NewName <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMRemoteConnectionProfileConfigurationItem [-Enable <Boolean>] [-EnableNla <Boolean>]
 [-EnablePrimaryUser <Boolean>] [-EnableTSConnection <Boolean>] [-EnableTSFirewallRule <Boolean>]
 [-RDGatewayServer <String>] [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-Id] <Int32> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMRemoteConnectionProfileConfigurationItem [-Enable <Boolean>] [-EnableNla <Boolean>]
 [-EnablePrimaryUser <Boolean>] [-EnableTSConnection <Boolean>] [-EnableTSFirewallRule <Boolean>]
 [-RDGatewayServer <String>] [-Description <String>] [-Digest <ConfigurationItem>] [-DigestPath <String>]
 [-DigestXml <String>] [-Name] <String> [-NewName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMRemoteConnectionProfileConfigurationItem** cmdlet modifies a remote connection profile.
Client computers use remote connection profiles to remotely connect to computers from outside the domain or over the Internet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a remote connection profile configuration item
```
PS XYZ:\> Set-CMRemoteConnectionProfileConfigurationItem -ID "AAA0004D" -EnablePrimaryUsers $False -EnableTSConnection $False -EnableTSFirewallRule $False
```

This command modifies the remote connection profile configuration item with the ID AAA0004D.
In this case, the *EnablePrimaryUsers*, *EnableTSConnection*, and *EnableTSFirewallRule* properties are all set to $False.

## PARAMETERS

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

### -Id
Specifies an array of IDs for remote connection profiles.

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
Specifies a remote connection profile object.
To obtain a remote connection profile, use the Get-CMRemoteConnectionProfileConfigurationItem cmdlet.

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
Specifies an array of names of remote connection profiles.

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
Specifies the new name for the remote connection profile.

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
### Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItem
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMRemoteConnectionProfileConfigurationItem](New-CMRemoteConnectionProfileConfigurationItem.md)
