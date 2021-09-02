---
description: Modify the properties of a boundary group.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/26/2020
schema: 2.0.0
title: Set-CMBoundaryGroup
---

# Set-CMBoundaryGroup

## SYNOPSIS

Modify the properties of a boundary group.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMBoundaryGroup [-AddSiteSystemServer <IResultObject[]>] [-AddSiteSystemServerName <String[]>]
 [-AllowPeerDownload <Boolean>] [-ClearSiteSystemServer] [-DefaultSiteCode <String>] [-Description <String>]
 -InputObject <IResultObject> [-NewName <String>] [-PassThru] [-PreferCloudDPOverDP <Boolean>]
 [-PreferDPOverPeer <Boolean>] [-RemoveSiteSystemServer <IResultObject[]>]
 [-RemoveSiteSystemServerName <String[]>] [-SubnetPeerDownloadOnly <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMBoundaryGroup [-AddSiteSystemServer <IResultObject[]>] [-AddSiteSystemServerName <String[]>]
 [-AllowPeerDownload <Boolean>] [-ClearSiteSystemServer] [-DefaultSiteCode <String>] [-Description <String>]
 -Id <String> [-NewName <String>] [-PassThru] [-PreferCloudDPOverDP <Boolean>] [-PreferDPOverPeer <Boolean>]
 [-RemoveSiteSystemServer <IResultObject[]>] [-RemoveSiteSystemServerName <String[]>]
 [-SubnetPeerDownloadOnly <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMBoundaryGroup [-AddSiteSystemServer <IResultObject[]>] [-AddSiteSystemServerName <String[]>]
 [-AllowPeerDownload <Boolean>] [-ClearSiteSystemServer] [-DefaultSiteCode <String>] [-Description <String>]
 -Name <String> [-NewName <String>] [-PassThru] [-PreferCloudDPOverDP <Boolean>] [-PreferDPOverPeer <Boolean>]
 [-RemoveSiteSystemServer <IResultObject[]>] [-RemoveSiteSystemServerName <String[]>]
 [-SubnetPeerDownloadOnly <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMBoundaryGroup** cmdlet modifies the properties of a boundary group.
A boundary group is a collection of boundaries.
For more information, see [Define site boundaries and boundary groups](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups) and the [New-CMBoundary](New-CMBoundary.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a boundary group

This command renames a boundary group. It uses the Get-CMBoundaryGroup cmdlet to get the boundary group object, and then passes it using the pipeline operator.

```powershell
Get-CMBoundaryGroup -Name "BGroup01" | Set-CMBoundaryGroup -NewName "BGroup00"
```

### Example 2: Add a security scope to a boundary group

This command adds the security scope **OSDeploymentScope** to the boundary group **BGroup02**.

```powershell
Set-CMBoundaryGroup -SecurityScopeAction AddMembership -SecurityScopeName "OSDeploymentScope" -Name "BGroup02"
```

### Example 3: Add a site system server

This command uses the **Get-CMSiteSystemServer** cmdlet to get a server object, and then adds it to the boundary group.

```powershell
$server = Get-CMSiteSystemServer -Name "granitefalls.cloudapp.net"
Set-CMBoundaryGroup -Name "Remote BG" -AddSiteSystemServer $server
```

## PARAMETERS

### -AddSiteSystemServer

Specify a site system server object to add to this boundary group. Clients on the boundary group use these servers for policy and content. You can add management points, distribution points, state migration points, software update points, and cloud management gateways. To get a site system server object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSiteSystemServers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSiteSystemServerName

Specify the fully qualified domain name of a site system server to add to this boundary group. Clients on the boundary group use these servers for policy and content. You can add management points, distribution points, state migration points, software update points, and cloud management gateways.

> [!Important]
> This parameter requires the fully qualified domain name of the site server.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddSiteSystemServerNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowPeerDownload

Configure the boundary group option to allow peer downloads in this boundary group. For more information, see [Boundary group options for peer downloads](/mem/configmgr/core/servers/deploy/configure/boundary-groups#bkmk_bgoptions).

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

### -ClearSiteSystemServer

Add this parameter to remove all referenced site system servers from the boundary group.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearSiteSystemServers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSiteCode

Specify the site code to set as the assigned site, and enable the boundary group for site assignment.

To disable site assignment for the boundary group, set this value to `$null`.

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

### -Description

Specify an optional description for this boundary group.

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

Specify the ID of a boundary group to configure. This ID is the **GroupID** property on the [SMS_BoundaryGroup](/mem/configmgr/develop/reference/core/servers/configure/sms_boundarygroup-server-wmi-class) object. For example, `33`.

```yaml
Type: String
Parameter Sets: SetById
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for a boundary group to configure. To get a boundary group object, use the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name for a boundary group to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename a boundary group.

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

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -PreferCloudDPOverDP

Configure the boundary group option to prefer cloud-based sources over on-premises sources. For more information, see [Boundary group options for peer downloads](/mem/configmgr/core/servers/deploy/configure/boundary-groups#bkmk_bgoptions).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: PreferCloudDistributionPointOverDistributionPoint

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreferDPOverPeer

Configure the boundary group option to prefer distribution points over peers within the same subnet. To enable this setting, also enable **-AllowPeerDownload**. For more information, see [Boundary group options for peer downloads](/mem/configmgr/core/servers/deploy/configure/boundary-groups#bkmk_bgoptions).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: PreferDistributionPointOverPeerInSubnet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSiteSystemServer

Specifies a site system server object to remove from the boundary group. To get this object, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

To remove all site system servers, use the **-ClearSiteSystemServer** parameter.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSiteSystemServers

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSiteSystemServerName

Specifies the name of one or more site system servers to remove from the boundary group. To remove all site system servers, use the **-ClearSiteSystemServer** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveSiteSystemServerNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetPeerDownloadOnly

Configure the boundary group option to only use peers within the same subnet during peer downloads. To enable this setting, also enable **-AllowPeerDownload**. For more information, see [Boundary group options for peer downloads](/mem/configmgr/core/servers/deploy/configure/boundary-groups#bkmk_bgoptions).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: PeerWithinSameSubnetOnly

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

### IResultObject#SMS_BoundaryGroup
## NOTES

## RELATED LINKS

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[New-CMBoundaryGroup](New-CMBoundaryGroup.md)

[Remove-CMBoundaryGroup](Remove-CMBoundaryGroup.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)

[New-CMBoundary](New-CMBoundary.md)

[Define site boundaries and boundary groups](/mem/configmgr/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups)
