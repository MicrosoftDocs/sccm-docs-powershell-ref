---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 7CBBD8FA-3534-46FC-829C-14A7C95BAB47
online version: https://go.microsoft.com/fwlink/?linkid=833648
schema: 2.0.0
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
The **Get-CMDiscoveryMethod** cmdlet gets a discovery method for Microsoft System Center Configuration Manager.
Discovery identifies computer and user resources that System Center Configuration Manager can manage.
If it discovers a resource, Configuration Manager creates a record in the System Center Configuration Manager database for the resource and its associated information.
You can then use the discovery information to help you to install the System Center Configuration Manager client and create custom queries and collections to logically group resources for related management tasks.

For more information about discovery in System Center Configuration Manager, see [About Configuration Manager Discovery](http://go.microsoft.com/fwlink/?linkid=107444) on TechNet.

## EXAMPLES

### Example 1: Get a user discovery method
```
PS C:\> Get-CMDiscoveryMethod -Name "ActiveDirectoryUserDiscovery"
```

This command gets a System Center Configuration Manager method that discovers users in the installation.

## PARAMETERS

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
Specifies the type of discovery method that the cmdlet gets.
The acceptable values for this parameter are:

- ActiveDirectoryForestDiscovery: Discovers security groups, including local, global, and universal groups from specified locations in Active Directory Domain Services.
- ActiveDirectoryGroupDiscovery: Discovers additional information, including the OU and group membership of the computer, about previously discovered computers from specified locations in Active Directory Domain Services. 
- ActiveDirectorySystemDiscovery: Discovers computers from specified locations in Active Directory Domain Services.
- ActiveDirectoryUserDiscovery: Discovers users from specified locations in Active Directory Domain Services.
- HeartbeatDiscovery: Updates discovery records for Microsoft System Center Configuration Manager clients in the System Center Configuration Manager database without discovering new resources.
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[About Configuration Manager Discovery](http://go.microsoft.com/fwlink/?linkid=107444)

[Set-CMDiscoveryMethod](Set-CMDiscoveryMethod.md)
