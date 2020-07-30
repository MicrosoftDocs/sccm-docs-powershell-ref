---
description: Adds a site system role for Endpoint Protection.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMEndpointProtectionPoint
---

# Add-CMEndpointProtectionPoint

## SYNOPSIS
Adds a site system role for Endpoint Protection.

## SYNTAX

### ByValue (Default)
```
Add-CMEndpointProtectionPoint [-LicenseAgreed <Boolean>] -ProtectionService <MapsMembershipType>
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Add-CMEndpointProtectionPoint [-SiteSystemServerName] <String> [-SiteCode <String>] [-LicenseAgreed <Boolean>]
 -ProtectionService <MapsMembershipType> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMEndpointProtectionPoint** cmdlet adds a site system role for System Center 2016 Endpoint Protection to a Microsoft System Center Configuration Manager site.

Endpoint Protection lets you manage antimalware policies and Windows Firewall security for client computers in System Center Configuration Manager.
In order to use Endpoint Protection with System Center Configuration Manager, you must install a single site system role for Endpoint Protection, either in the central site or in a stand-alone primary site.
For more information about Endpoint Protection in System Center Configuration Manager, see [Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508760(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a site system role
```
PS XYZ:\>Add-CMEndpointProtectionPoint -LicenseAgreed $True -ProtectionService BasicMembership -SiteCode "CM1" -SiteSystemServerName "CMEPPoint.Western.Contoso.com"
```

This command adds an Endpoint Protection point for the site that has the site code CM1.
The specified computer hosts the role.
The command also specifies that you accept the terms of the license agreement and have a basic membership for Endpoint Protection.

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

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LicenseAgreed
Specifies whether you agree to the Endpoint Protection software licensing terms.

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

### -ProtectionService
Specifies the type of membership you have for Microsoft Active Protection Service (MAPS).
Valid values are:

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
Parameter Sets: ByName
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
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_SCI_SysResUse

## NOTES

## RELATED LINKS

[Endpoint Protection in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/hh508760(v=technet.10))

[Get-CMEndpointProtectionPoint](Get-CMEndpointProtectionPoint.md)

[Remove-CMEndpointProtectionPoint](Remove-CMEndpointProtectionPoint.md)

[Set-CMEndpointProtectionPoint](Set-CMEndpointProtectionPoint.md)
