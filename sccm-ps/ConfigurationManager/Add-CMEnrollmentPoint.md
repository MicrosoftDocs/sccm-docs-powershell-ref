---
description: Adds an enrollment point to Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMEnrollmentPoint
---

# Add-CMEnrollmentPoint

## SYNOPSIS
Adds an enrollment point to Configuration Manager.

## SYNTAX

### EnrollmentPointByValue (Default)
```
Add-CMEnrollmentPoint -InputObject <IResultObject> [-PortNumber <Int32>] [-WebApplicationName <String>]
 [-WebsiteName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### EnrollmentPoint
```
Add-CMEnrollmentPoint [-PortNumber <Int32>] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-UserName <String>] [-WebApplicationName <String>] [-WebsiteName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMEnrollmentPoint** cmdlet adds an enrollment point to a Configuration Manager site.
An enrollment point is a site system role that manages enrollment requests from mobile devices.

When Configuration Manager enrolls a mobile device, it installs a Configuration Manager client.
The client provides management capabilities that include hardware inventory, software deployment, settings, and remote wipe.
To enroll mobile devices, use Microsoft Certificate Services with an enterprise certification authority.
You need a Configuration Manager enrollment point site system role, as well as an enrollment proxy point site system role.
For more information about site system roles, see [Install and Configure Site System Roles for Configuration Manager](/mem/configmgr/core/servers/deploy/configure/install-site-system-roles).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add an enrollment point
```
PS XYZ:\>Add-CMEnrollmentPoint -SiteCode "CM4" -SiteSystemServerName "Server04.Building02.Contoso.com" -IISWebsite "Intranet17" -PortNumber 80 -UserName "QADept\Admins" -WebApplicationName "Tracker"
```

This command adds an enrollment point for the site that has the site code CM4 to the server named Server04.Building02.Contoso.com.
The command specifies an IIS website and port number, and the user name that the enrollment point uses to connect to the Configuration Manager database.
This command also specifies the web application name.

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

### -InputObject
Specifies the input to this cmdlet.
You can use this parameter, or you can pipe the input to this cmdlet.

```yaml
Type: IResultObject
Parameter Sets: EnrollmentPointByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PortNumber
Specifies the port to use with an enrollment point.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: EnrollmentPoint
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
Parameter Sets: EnrollmentPoint
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies an account that the enrollment point uses to connect to the Configuration Manager database.

```yaml
Type: String
Parameter Sets: EnrollmentPoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApplicationName
Specifies the name of the web application used for enrollment.

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

### -WebsiteName
```yaml
Type: String
Parameter Sets: (All)
Aliases: IISWebsite

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

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Add-CMEnrollmentProxyPoint](Add-CMEnrollmentProxyPoint.md)

[Get-CMEnrollmentPoint](Get-CMEnrollmentPoint.md)

[Remove-CMEnrollmentPoint](Remove-CMEnrollmentPoint.md)


