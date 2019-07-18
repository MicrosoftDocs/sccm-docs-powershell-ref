---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 7BEF1089-8E5C-4719-96E0-57443F90E8AA
online version: https://go.microsoft.com/fwlink/?linkid=833841
schema: 2.0.0
---

# Set-CMEndpointProtectionPoint

## SYNOPSIS
Modifies a site system role for Endpoint Protection.

## SYNTAX

### SetByValue (Default)
```
Set-CMEndpointProtectionPoint -ProtectionService <MapsMembershipType> -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMEndpointProtectionPoint [-SiteCode <String>] [-SiteSystemServerName] <String>
 -ProtectionService <MapsMembershipType> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMEndpointProtectionPoint** cmdlet modifies a site system role for System Center 2016 Endpoint Protection in Microsoft System Center Configuration Manager.

Endpoint Protection lets you manage antimalware policies and Windows Firewall security for client computers in System Center Configuration Manager.
In order to use Endpoint Protection with System Center Configuration Manager, you must install a single site system role for Endpoint Protection, either in the central site or in a stand-alone primary site.
For more information about Endpoint Protection in System Center Configuration Manager, see the [Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427) on TechNet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Set an endpoint protection point
```
PS XYZ:\> Set-CMEndpointProtectionPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2" -ProtectionService AdvancedMembership
```

The command sets the endpoint protection point for the server, and specifies the membership type for the *ProtectionService* parameter.

### Example 2: Set an endpoint protection point by using an input object
```
PS XYZ:\> $Epp = Get-CMEndpointProtectionPoint -SiteSystemServerName "CM-Contoso.Contoso.Com" -SiteCode "CM2" 
PS XYZ:\> Set-CMEndpointProtectionPoint -InputObject $Epp -ProtectionService BasicMembership
```

The first command uses the **Get-CMEndpointProtectionPoint** cmdlet to get an endpoint protection point, and stores the result in the $Epp variable.

The second command sets the endpoint protection point for the server by using the input object from the previous command.

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

### -InputObject
Specifies an input object.
To obtain an input object, use the [Get-CMEndpointProtectionPoint](Get-CMEndpointProtectionPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: EndpointProtectionPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -ProtectionService
Specifies the type of membership to set for Microsoft Active Protection Service (MAPS).
The acceptable values for this parameter are:

- AdvancedMembership
- BasicMembership
- DoNotJoinMaps

```yaml
Type: MapsMembershipType
Parameter Sets: (All)
Aliases: 
Accepted values: DoNotJoinMaps, BasicMembership, AdvancedMembership

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a server that hosts a site system role.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
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

[Endpoint Protection in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=268427)

[Add-CMEndpointProtectionPoint](Add-CMEndpointProtectionPoint.md)

[Get-CMEndpointProtectionPoint](Get-CMEndpointProtectionPoint.md)

[Remove-CMEndpointProtectionPoint](Remove-CMEndpointProtectionPoint.md)
