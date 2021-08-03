---
description: Gets a component for a Configuration Manager management point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMManagementPointComponent
---

# Get-CMManagementPointComponent

## SYNOPSIS
Gets a component for a Configuration Manager management point.

## SYNTAX

```
Get-CMManagementPointComponent [-SiteCode <String>] [-SiteSystemServerName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMManagementPointComponent** cmdlet gets a component of a management point for Configuration Manager.
A management point is a Configuration Manager site that provides policy and service information to clients and receives configuration data from clients.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a management point component
```
PS XYZ:\> Get-CMManagementPointComponent -SiteCode "CM1" >>\1\Get-CMManagementPointComponent_data.txt
```

This command gets a component that is associated with the site that has the code CM1.
The command directs the output to the file Get-CMManagementPointComponent_data.txt.

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

### -SiteCode
Specifies the site code for the management point.

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

### -SiteSystemServerName
Specifies a fully qualified domain name (FQDN) of the server that hosts the site system role.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### IResultObject[]#SMS_SCI_SysResUse
### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Set-CMManagementPointComponent](Set-CMManagementPointComponent.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Remove-CMManagementPoint](Remove-CMManagementPoint.md)


