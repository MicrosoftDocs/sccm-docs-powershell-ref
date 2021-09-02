---
description: Changes configuration settings of a discovery method.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMDiscoveryMethod
---

# Set-CMDiscoveryMethod

## SYNOPSIS
Changes configuration settings of a discovery method.

## SYNTAX

### SearchByActiveDirectoryForestDiscovery (Default)
```
Set-CMDiscoveryMethod [-ActiveDirectoryForestDiscovery] [-EnableActiveDirectorySiteBoundaryCreation <Boolean>]
 [-Enabled <Boolean>] [-EnableSubnetBoundaryCreation <Boolean>] [-PassThru] [-PollingSchedule <IResultObject>]
 [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByActiveDirectorySystemDiscovery
```
Set-CMDiscoveryMethod [-ActiveDirectoryContainer <String[]>] [-ActiveDirectorySystemDiscovery]
 [-AddActiveDirectoryContainer <String[]>] [-AddAdditionalAttribute <String[]>]
 [-ClearActiveDirectoryContainer] [-DeltaDiscoveryMins <Int32>] [-Enabled <Boolean>]
 [-EnableDeltaDiscovery <Boolean>] [-EnableFilteringExpiredLogon <Boolean>]
 [-EnableFilteringExpiredPassword <Boolean>] [-EnableIncludeGroup <Boolean>] [-EnableRecursive <Boolean>]
 [-IncludeGroup] [-PassThru] [-PollingSchedule <IResultObject>] [-Recursive]
 [-RemoveActiveDirectoryContainer <String[]>] [-RemoveAdditionalAttribute <String[]>] [-SiteCode <String>]
 [-TimeSinceLastLogonDays <Int32>] [-TimeSinceLastPasswordUpdateDays <Int32>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByActiveDirectoryUserDiscovery
```
Set-CMDiscoveryMethod [-ActiveDirectoryContainer <String[]>] [-ActiveDirectoryUserDiscovery]
 [-AddActiveDirectoryContainer <String[]>] [-AddAdditionalAttribute <String[]>]
 [-ClearActiveDirectoryContainer] [-DeltaDiscoveryMins <Int32>] [-Enabled <Boolean>]
 [-EnableDeltaDiscovery <Boolean>] [-EnableIncludeGroup <Boolean>] [-EnableRecursive <Boolean>] [-IncludeGroup]
 [-PassThru] [-PollingSchedule <IResultObject>] [-Recursive] [-RemoveActiveDirectoryContainer <String[]>]
 [-RemoveAdditionalAttribute <String[]>] [-SiteCode <String>] [-UserName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByActiveDirectoryGroupDiscovery
```
Set-CMDiscoveryMethod [-ActiveDirectoryGroupDiscovery] [-AddGroupDiscoveryScope <ADGroupDiscoveryScope[]>]
 [-ClearActiveDirectoryContainer] [-DeltaDiscoveryMins <Int32>]
 [-DiscoverDistributionGroupMembership <Boolean>] [-Enabled <Boolean>] [-EnableDeltaDiscovery <Boolean>]
 [-EnableFilteringExpiredLogon <Boolean>] [-EnableFilteringExpiredPassword <Boolean>] [-PassThru]
 [-PollingSchedule <IResultObject>] [-RemoveGroupDiscoveryScope <String[]>] [-SiteCode <String>]
 [-TimeSinceLastLogonDays <Int32>] [-TimeSinceLastPasswordUpdateDays <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNetworkDiscovery
```
Set-CMDiscoveryMethod [-Enabled <Boolean>] [-NetworkDiscovery] [-NetworkDiscoveryType <NetworkDiscoveryType>]
 [-PassThru] [-SiteCode <String>] [-SlowNetworkSpeed <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByHeartbeat
```
Set-CMDiscoveryMethod [-Enabled <Boolean>] [-Heartbeat] [-PassThru] [-PollingSchedule <IResultObject>]
 [-SiteCode <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDiscoveryMethod** cmdlet changes configuration settings of a discovery method.
Discovery identifies computer and user resources that Configuration Manager can manage.
When Configuration Manager discovers a resource, Configuration Manager creates a record in the Configuration Manager database for the resource and its associated information.
You can then use the discovery information to help you to install the Configuration Manager client and create custom queries and collections to logically group resources for related management tasks.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify network discovery
```
PS XYZ:\> Set-CMDiscoveryMethod -NetworkDiscovery -SiteCode "CM4" -Enabled $True -NetworkDiscoveryType ToplogyAndClient -SlowNetworkSpeed $True
```

This command modifies network discovery for the site that has the site code CM4.
The command specifies topology and client network discovery and the slow network speed option.
The command also enables discovery.

### Example 2: Modify Active Directory system discovery
```
PS XYZ:\> $Schedule = New-CMSchedule -RecurInterval Minutes -Start "2012/10/20 00:00:00" -End "2013/10/20 00:00:00" -RecurCount 10
PS XYZ:\> Set-CMDiscoveryMethod -ActiveDirectorySystemDiscovery -SiteCode "CM4" -AddAdditionalAttribute "331", "431", "134" -DeltaDiscoveryIntervalMinutes 8 -Enabled $True -EnableDeltaDiscovery $True -EnableFilteringExpiredLogon $True -PollingSchedule $Schedule -RemoveAdditionalAttribute "123","cn" -TimeSinceLastLogonDays 80
```

The first command creates a schedule object by using the **New-CMSchedule** cmdlet and stores it in the $Schedule variable.

The second command enables the computer discovery for the site that has the site code CM4.
The command specifies the schedule object stored in the $Schedule variable as the polling schedule and enables delta discovery to find new and modified computers since the last discovery.
The command specifies that delta discovery takes place every 8 minutes.

The second command also limits the computers found to those that a user has logged onto in the last 80 days.
Also, the command adds and removes specified attributes from the attributes used to limit computers.

### Example 3: Modify forest discovery
```
PS XYZ:\> $Schedule = New-CMSchedule -RecurInterval Minutes -Start "2012/10/20 00:00:00" -End "2013/10/20 00:00:00" -RecurCount 10
PS XYZ:\> Set-CMDiscoveryMethod -ActiveDirectoryForestDiscovery -SiteCode "CM4" -EnableActiveDirectorySiteBoundaryCreation $True -Enabled $True  -EnableSubnetBoundaryCreation $True -PollingSchedule $Schedule
```

The first command creates a schedule object by using the **New-CMSchedule** cmdlet, and then stores it in the $Schedule variable.

The second command enables this discovery site that has the site code CM4.
The command specifies the schedule object stored in the $Schedule variable as the polling interval and enables Active Directory boundary creation and subnet boundary creation.

### Example 4: Enable heartbeat discovery
```
PS XYZ:\> $Schedule = New-CMSchedule -RecurInterval Minutes -Start "2012/10/20 00:00:00" -End "2013/10/20 00:00:00" -RecurCount 10
PS XYZ:\> Set-CMDiscoveryMethod -Heartbeat -SiteCode "CM4" -Enabled $True -PollingSchedule $Schedule
```

The first command creates a schedule object by using the **New-CMSchedule** cmdlet and stores it in the $Schedule variable.

The second command enables heartbeat discovery and specifies the object stored in the $Schedule variable as the polling schedule for the site that has the site code CM4.

## PARAMETERS

### -ActiveDirectoryContainer
Specifies an array of names of Active Directory containers.

```yaml
Type: String[]
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryForestDiscovery
Indicates that the discovery method discovers security groups, including local, global, and universal groups from specified locations in Active Directory Domain Services (AD DS).

```yaml
Type: SwitchParameter
Parameter Sets: SearchByActiveDirectoryForestDiscovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryGroupDiscovery
Indicates that the discovery method discovers additional information, including the computer organizational unit (OU) and group membership, about previously discovered computers from specified locations in AD DS.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectorySystemDiscovery
Indicates that the discovery method discovers computers from specified locations in AD DS.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByActiveDirectorySystemDiscovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ActiveDirectoryUserDiscovery
Indicates that the discovery method discovers users from specified locations in AD DS.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByActiveDirectoryUserDiscovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddActiveDirectoryContainer
```yaml
Type: String[]
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases: AddActiveDirectoryContainers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddAdditionalAttribute
Specifies an array of Active Directory object attributes.
The cmdlet adds these attributes to the list of attributes that Configuration Manager discovers.

```yaml
Type: String[]
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddGroupDiscoveryScope
```yaml
Type: ADGroupDiscoveryScope[]
Parameter Sets: SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearActiveDirectoryContainer
```yaml
Type: SwitchParameter
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery, SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeltaDiscoveryMins
```yaml
Type: Int32
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery, SearchByActiveDirectoryGroupDiscovery
Aliases: DeltaDiscoveryIntervalMinutes, DeltaDiscoveryIntervalMins

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

### -DiscoverDistributionGroupMembership
```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectoryGroupDiscovery
Aliases: DiscoverDistributionGroupsMembership

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableActiveDirectorySiteBoundaryCreation
Indicates whether Configuration Manager creates Active Directory boundaries from AD DS discovery information.

```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectoryForestDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enabled
Indicates whether to enable the Configuration Manager discovery.
If you specify a value of $False, Configuration Manager does not discover resources by using this discovery.

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

### -EnableDeltaDiscovery
Indicates whether Configuration Manager discovers resources created or modified in AD DS since the last discovery cycle.
If you specify a value of $True for this parameter, specify a value for the *DeltaDiscoveryIntervalMinutes* parameter.

```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery, SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableFilteringExpiredLogon
Indicates whether Configuration Manager discovers only computers that have logged onto a domain within a specified number of days.
Specify the number of days by using the *TimeSinceLastLogonDays* parameter.

```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableFilteringExpiredPassword
Indicates whether Configuration Manager discovers only computers that have updated their computer account password within a specified number of days.
Specify the number of days by using the *TimeSinceLastPasswordUpdateDays* parameter.

```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableIncludeGroup
{{ Fill EnableIncludeGroup Description }}

```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases: EnableIncludeGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableRecursive
{{ Fill EnableRecursive Description }}

```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSubnetBoundaryCreation
Indicates whether Configuration Manager creates IP address range boundaries from AD DS discovery information.

```yaml
Type: Boolean
Parameter Sets: SearchByActiveDirectoryForestDiscovery
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

### -Heartbeat
Indicates that the discovery method updates discovery records for Configuration Manager clients in the Configuration Manager database without discovering new resources.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByHeartbeat
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IncludeGroup
```yaml
Type: SwitchParameter
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases: IncludeGroups

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkDiscovery
Indicates that the discovery method searches the network infrastructure for network devices, such as printers, routers, and bridges, that have IP addresses.

```yaml
Type: SwitchParameter
Parameter Sets: SearchByNetworkDiscovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkDiscoveryType
Specifies the network discovery type.
If you specify the *NetworkDiscovery* parameter, specify one of the following types:

- ToplogyAndClient.
The discovery finds the topology of your network and potential client devices.
- ToplogyClientAndClientOperatingSystem.
The discovery finds the topology of your network.
The discovery finds potential client devices and their operating systems and versions.
- Topology.
The discovery finds the topology of your network by discovering IP subnets and routers.

```yaml
Type: NetworkDiscoveryType
Parameter Sets: SearchByNetworkDiscovery
Aliases:
Accepted values: Topology, TopologyAndClient, ToplogyAndClient, TopologyClientAndClientOperatingSystem, ToplogyClientAndClientOperatingSystem

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

### -PollingSchedule
Specifies a schedule object.
To obtain a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.
The polling schedule determines how often Configuration Manager attempts to discover groups, systems, or user data.

```yaml
Type: IResultObject
Parameter Sets: SearchByActiveDirectoryForestDiscovery, SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery, SearchByActiveDirectoryGroupDiscovery, SearchByHeartbeat
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Recursive
```yaml
Type: SwitchParameter
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveActiveDirectoryContainer
```yaml
Type: String[]
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases: RemoveActiveDirectoryContainers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveAdditionalAttribute
Specifies an array of Active Directory object attributes.
The cmdlet removes these attributes from the list of attributes that Configuration Manager discovers.

```yaml
Type: String[]
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveGroupDiscoveryScope
```yaml
Type: String[]
Parameter Sets: SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

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

### -SlowNetworkSpeed
Indicates whether Configuration Manager makes adjustments to its discovery settings for networks that have low bandwidth.

```yaml
Type: Boolean
Parameter Sets: SearchByNetworkDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeSinceLastLogonDays
Specifies the number of days since the last logon when the *EnableFilteringExpiredLogon* parameter had a value of $True.

```yaml
Type: Int32
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeSinceLastPasswordUpdateDays
Specifies the number of days since that last password updated when the *EnableFilteringExpiredPassword* parameter had a value of $True.

```yaml
Type: Int32
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryGroupDiscovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
{{ Fill UserName Description }}

```yaml
Type: String
Parameter Sets: SearchByActiveDirectorySystemDiscovery, SearchByActiveDirectoryUserDiscovery
Aliases: DiscoveryAccountUserName

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

### None
## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDiscoveryMethod](Get-CMDiscoveryMethod.md)

[New-CMSchedule](New-CMSchedule.md)
