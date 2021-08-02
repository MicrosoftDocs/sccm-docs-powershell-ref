---
description: Gets an object that installs a Configuration Manager client by using client push.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMClientPushInstallation
---

# Get-CMClientPushInstallation

## SYNOPSIS
Gets an object that installs a Configuration Manager client by using client push.

## SYNTAX

```
Get-CMClientPushInstallation [-SiteCode <String>] [-SiteSystemServerName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMClientPushInstallation** cmdlet gets an object that installs a Configuration Manager client by using client push.
A client push installation installs client software on computers that Configuration Manager discovered.
When you configure client push installation for a site, the client installation automatically runs on the computers that Configuration Manager discovered within the site's configured boundaries when those boundaries are part of a boundary group.
You can also start a client push installation by running the Client Push Installation Wizard for a specific collection or resource within a collection.

For more information about how to install clients, see [How to Install Clients on Windows Computers in Configuration Manager](/mem/configmgr/core/clients/deploy/deploy-clients-to-windows-computers).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a client push installation
```
PS XYZ:\> Get-CMClientPushInstallation -SiteSystemServerName "CMClientPushInstallationPoint.Western.Contoso.com"
```

This command gets the client push installation for the site system server named CMClientPushInstallationPoint.Western.Contoso.com.

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
Specifies an array of site codes that identify sites on which Configuration Manager installs the client.

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
Specifies an array of names of site system servers.
Site system servers contain roles that define the operations that each site can perform.

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

### IResultObject[]#SMS_SCI_Component
### IResultObject#SMS_SCI_Component
## NOTES

## RELATED LINKS

[How to Install Clients on Windows Computers in Configuration Manager](/mem/configmgr/core/clients/deploy/deploy-clients-to-windows-computers)

[Set-CMClientPushInstallation](Set-CMClientPushInstallation.md)


