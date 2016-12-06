---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834281
schema: 2.0.0
ms.assetid: 8AF3746E-A031-432B-91E1-C9B579FE7D55
---

# New-CMBoundaryGroup

## SYNOPSIS
Creates a new boundary group.

## SYNTAX

```
New-CMBoundaryGroup -Name <String> [-Description <String>] [-DefaultSiteCode <String>]
 [-AddSiteSystemServer <Hashtable>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMBoundaryGroup** cmdlet creates a new boundary group.
A boundary group is a collection of boundaries.

You can use boundary groups to manage network locations.
You must assign boundaries to boundary groups before you can use the boundary group.
Boundary groups enable client computers to find a primary site for client assignment, which is referred to as automatic site assignment, and a list of available site systems that have content.
For more information about boundaries, see [Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266225) on TechNet and the New-CMBoundary cmdlet.

## EXAMPLES

### Example 1: Create a new boundary group
```
PS C:\>New-BoundaryGroup -Name "BGroup05"
CreatedBy:          
CreatedOn           
DefaultSiteCode: 
Description: 
GroupID:            
MemberCount:        0
ModifiedBy:         
ModifiedOn:         
Name:               BGroup05 
SiteSystemCount:
```

This command creates a new boundary group.
After the new boundary group is created, the command displays an unpopulated list of boundary properties.
To refresh and see a populated list, use the **Get-CMBoundaryGroup** cmdlet.
The output shown for this example is the latter.

## PARAMETERS

### -AddSiteSystemServer


```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: AddSiteSystemServers

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
Specifies the default site code for the boundary group.

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
Specifies a description for the new boundary.

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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
Specifies a name for the new boundary.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

[Planning for Boundaries and Boundary Groups in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=266225)

[Get-CMBoundaryGroup](./Get-CMBoundaryGroup.md)

[Remove-CMBoundaryGroup](./Remove-CMBoundaryGroup.md)

[Set-CMBoundaryGroup](./Set-CMBoundaryGroup.md)

[New-CMBoundary](./New-CMBoundary.md)


