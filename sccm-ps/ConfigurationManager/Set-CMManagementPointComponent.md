---
description: Sets a component for a management point in Configuration Manager.
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMManagementPointComponent
---

# Set-CMManagementPointComponent

## SYNOPSIS
Sets a component for a management point in Configuration Manager.

## SYNTAX

### SearchBySiteCodeMandatory (Default)
```
Set-CMManagementPointComponent [-SiteCode <String>] [-PublishDns <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMManagementPointComponent -Name <String> [-PublishDns <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Set-CMManagementPointComponent [-PublishDns <Boolean>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMManagementPointComponent** cmdlet sets a component for a management point in Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Set a management point component
```
PS XYZ:\> Set-CMManagementPointComponent -SiteCode "CM1" -PublishDNS $True
```

The command sets a management point component by using the *SiteCode* parameter.
The command also sets the *PublishDNS* parameter to $True to publish the management point component in DNS.

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
To obtain an input object, use the [Get-CMManagementPointComponent](Get-CMManagementPointComponent.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublishDns
Indicates whether to publish  resource records for the management point component in the Domain Name System (DNS).
Configuration Manager clients use DNS service location resource records (SRV RR) to find a management point in a site.

For Configuration Manager to publish management points to DNS, your DNS servers must have version 8.1.2 of BIND, or later.
Your DNS servers must be configured for automatic updates and support service location resource records.
The fully qualified domain names (FQDNs) of management points must have host entries in DNS.

You must assign clients to a specific site and configure the clients to use the site code with the domain suffix of their management point.

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

### -SiteCode
Specifies a site code in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases:

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

###  

## NOTES

## RELATED LINKS

[Get-CMManagementPointComponent](Get-CMManagementPointComponent.md)
