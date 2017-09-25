---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 51F673B9-5558-4865-8AF8-B0B67296F729
online version: https://go.microsoft.com/fwlink/?linkid=833690
schema: 2.0.0
---

# Set-CMBoundaryGroup

## SYNOPSIS
Modifies the properties of a boundary group.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMBoundaryGroup -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-DefaultSiteCode <String>] [-AddSiteSystemServer <IResultObject[]>] [-AddSiteSystemServerName <String[]>]
 [-RemoveSiteSystemServer <IResultObject[]>] [-RemoveSiteSystemServerName <String[]>] [-ClearSiteSystemServer]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMBoundaryGroup -Id <String> [-NewName <String>] [-Description <String>] [-DefaultSiteCode <String>]
 [-AddSiteSystemServer <IResultObject[]>] [-AddSiteSystemServerName <String[]>]
 [-RemoveSiteSystemServer <IResultObject[]>] [-RemoveSiteSystemServerName <String[]>] [-ClearSiteSystemServer]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMBoundaryGroup -Name <String> [-NewName <String>] [-Description <String>] [-DefaultSiteCode <String>]
 [-AddSiteSystemServer <IResultObject[]>] [-AddSiteSystemServerName <String[]>]
 [-RemoveSiteSystemServer <IResultObject[]>] [-RemoveSiteSystemServerName <String[]>] [-ClearSiteSystemServer]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBoundaryGroup** cmdlet modifies the properties of a boundary group.
A boundary group is a collection of boundaries.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266225) on TechNet and the [New-CMBoundary](New-CMBoundary.md) cmdlet.

## EXAMPLES

### Example 1: Rename a boundary group
```
PS C:\> Set-CMBoundaryGroup -Name "BGroup01" -NewName "BGroup00"
```

This command renames a boundary group.

### Example 2: Add a security scope to a boundary group
```
PS C:\> Set-CMBoundaryGroup -SecurityScopeAction AddMembership -SecurityScopeName "OSDeploymentScope" -Name "BGroup02"
```

This command adds the security scope OSDeploymentScope to the boundary group BGroup02.

## PARAMETERS

### -AddSiteSystemServer
Specifies the site system server and link speed as the key/value pair in a hash table.
Valid values are:

- FastLink
- Slowlink

For example: @{"Server01.contoso.com" = "FastLink"}

**Important**: Starting in version 1610, FastLink is the only supported value for the hash table.

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
{{Fill AddSiteSystemServerName Description}}

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

### -ClearSiteSystemServer
Indicates that the site system server is removed from the boundary group.

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

### -DefaultSiteCode
Specifies the default site code of a boundary group.

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
Specifies a description for a boundary group.

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

### -Id
Specifies an array of identifiers for one or more boundary groups.

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
Specifies a boundary group object.
To obtain a boundary group object, use the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

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
Specifies a name for a boundary group.

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
Specifies a new name for a boundary group.

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
Returns the current working object.
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

### -RemoveSiteSystemServer
Specifies a site system server object to remove from the boundary group.
To obtain a site system server, use the [Get-CMSiteSystemServer](Get-CMSiteSystemServer.md) cmdlet.

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
Specifies the name of a site system server to remove from the boundary group.

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

[Define site boundaries and boundary groups for System Center Configuration Manager](https://docs.microsoft.com/en-us/sccm/core/servers/deploy/configure/define-site-boundaries-and-boundary-groups#a-namebkmkboundarygroupsa-boundary-group/)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[New-CMBoundaryGroup](New-CMBoundaryGroup.md)

[Remove-CMBoundaryGroup](Remove-CMBoundaryGroup.md)

[Set-CMSecurityScope](Set-CMSecurityScope.md)

[New-CMBoundary](New-CMBoundary.md)
