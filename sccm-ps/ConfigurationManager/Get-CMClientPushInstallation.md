---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 93625B5F-18C6-48F8-9BB2-6CF6BC0E4590
online version: https://go.microsoft.com/fwlink/?linkid=834188
schema: 2.0.0
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
The **Get-CMClientPushInstallation** cmdlet gets an object that installs a Microsoft System Center Configuration Manager client by using client push.
A client push installation installs client software on computers that System Center Configuration Manager discovered.
When you configure client push installation for a site, the client installation automatically runs on the computers that System Center Configuration Manager discovered within the site's configured boundaries when those boundaries are part of a boundary group.
You can also start a client push installation by running the Client Push Installation Wizard for a specific collection or resource within a collection.

For more information about how to install clients, see [How to Install Clients on Windows Computers in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=247203) on TechNet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get a client push installation
```
PS XYZ:\> Get-CMClientPushInstallation -SiteSystemServerName "CMClientPushInstallationPoint.Western.Contoso.com"
```

This command gets the client push installation for the site system server named CMClientPushInstallationPoint.Western.Contoso.com.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[How to Install Clients on Windows Computers in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=247203)

[Set-CMClientPushInstallation](Set-CMClientPushInstallation.md)


