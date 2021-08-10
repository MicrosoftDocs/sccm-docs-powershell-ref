---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# Get-CMBoundaryGroupSiteSystem

## SYNOPSIS

Get site systems in the specified boundary group

## SYNTAX

### SearchByName (Default)
```
Get-CMBoundaryGroupSiteSystem [-GroupName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBoundaryGroupSiteSystem -Id <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByValue
```
Get-CMBoundaryGroupSiteSystem [-InputObject <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get site systems in the specified boundary group. For more information, see [About boundary groups in Configuration Manager](/mem/configmgr/core/servers/deploy/configure/boundary-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Display FQDNs of site systems in a boundary group

This example first gets a boundary group by name and saves that object in a variable **$boundaryGroup**. It then queries for the site systems in that boundary group by passing the boundary group object, and saves the results in a variable **$bgSiteSystems**.

The **foreach** loop then goes through each site system object and extracts the FQDN from the NAL path.

```powershell
$bgName = "Contoso HQ BG"
$boundaryGroup = Get-CMBoundaryGroup -Name $bgName

$bgSiteSystems = Get-CMBoundaryGroupSiteSystem -InputObject $boundaryGroup

foreach ($system in $bgSiteSystems) {
  Write-Host $system.ServerNalPath.TrimEnd('\').Split('\')[-1]
}
```

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

### -GroupName

Specify a boundary group name to get the associated site systems.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Id

Specify an array of boundary group IDs to get the associated site systems. This value is an integer, for example `5`.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a boundary group object to get the associated site systems. To get this object, use the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: BoundaryGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_BoundaryGroupSiteSystems
### IResultObject#SMS_BoundaryGroupSiteSystems
## NOTES

For more information on this return object and its properties, see [SMS_BoundaryGroupSiteSystems server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_boundarygroupsitesystems-server-wmi-class).

## RELATED LINKS

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)

[Get-CMBoundaryGroupRelationship](Get-CMBoundaryGroupRelationship.md)
