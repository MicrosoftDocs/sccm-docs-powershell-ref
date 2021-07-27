---
description: Gets a discovery method for Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDiscoveryMethod
---

# Get-CMDiscoveryMethod

## SYNOPSIS
Gets a discovery method for Configuration Manager.

## SYNTAX

```
Get-CMDiscoveryMethod [-Name <DiscoveryType>] [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDiscoveryMethod** cmdlet gets a discovery method for Configuration Manager.
Discovery identifies computer and user resources that Configuration Manager can manage.
If it discovers a resource, Configuration Manager creates a record in the Configuration Manager database for the resource and its associated information.
You can then use the discovery information to help you to install the Configuration Manager client and create custom queries and collections to logically group resources for related management tasks.

For more information about discovery in Configuration Manager, see [About Configuration Manager Discovery](/mem/configmgr/core/servers/deploy/configure/run-discovery).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a user discovery method
```
PS XYZ:\> Get-CMDiscoveryMethod -Name "ActiveDirectoryUserDiscovery"
```

This command gets a Configuration Manager method that discovers users in the installation.

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
Specifies the type of discovery method that the cmdlet gets.
The acceptable values for this parameter are:

- ActiveDirectoryForestDiscovery: Discovers security groups, including local, global, and universal groups from specified locations in Active Directory Domain Services.
- ActiveDirectoryGroupDiscovery: Discovers additional information, including the OU and group membership of the computer, about previously discovered computers from specified locations in Active Directory Domain Services.
- ActiveDirectorySystemDiscovery: Discovers computers from specified locations in Active Directory Domain Services.
- ActiveDirectoryUserDiscovery: Discovers users from specified locations in Active Directory Domain Services.
- HeartbeatDiscovery: Updates discovery records for Configuration Manager clients in the Configuration Manager database without discovering new resources.
- NetworkForestDiscovery: Searches the network infrastructure for network devices (such as printers, routers, and bridges) that have an IP address.

```yaml
Type: DiscoveryType
Parameter Sets: (All)
Aliases:
Accepted values: ActiveDirectoryForestDiscovery, ActiveDirectoryGroupDiscovery, ActiveDirectorySystemDiscovery, ActiveDirectoryUserDiscovery, NetworkDiscovery, HeartbeatDiscovery

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_SCI_Component
### IResultObject#SMS_SCI_Component
### IResultObject[]#SMS_SCI_ClientConfig
### IResultObject#SMS_SCI_ClientConfig
## NOTES

## RELATED LINKS

[About Configuration Manager Discovery](/mem/configmgr/core/servers/deploy/configure/run-discovery)

[Set-CMDiscoveryMethod](Set-CMDiscoveryMethod.md)
