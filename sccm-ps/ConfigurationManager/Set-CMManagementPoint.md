---
description: Changes settings for a management point in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMManagementPoint
---

# Set-CMManagementPoint

## SYNOPSIS
Changes settings for a management point in Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMManagementPoint [-AllowDevice <Boolean>] [-ClientConnectionType <ClientConnectionTypes>]
 [-DatabaseName <String>] [-EnableCloudGateway <Boolean>] [-EnableSsl <Boolean>] [-GenerateAlert <Boolean>]
 -InputObject <IResultObject> [-PassThru] [-SqlServerFqdn <String>] [-SqlServerInstanceName <String>]
 [-UseComputerAccount] [-UserName <String>] [-UseSiteDatabase <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMManagementPoint [-AllowDevice <Boolean>] [-ClientConnectionType <ClientConnectionTypes>]
 [-DatabaseName <String>] [-EnableCloudGateway <Boolean>] [-EnableSsl <Boolean>] [-GenerateAlert <Boolean>]
 [-PassThru] [-SiteCode <String>] [-SiteSystemServerName] <String> [-SqlServerFqdn <String>]
 [-SqlServerInstanceName <String>] [-UseComputerAccount] [-UserName <String>] [-UseSiteDatabase <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMManagementPoint** cmdlet changes settings for a management point in Configuration Manager.
A management point is a Configuration Manager site that provides policy and service information to clients and receives configuration data from clients.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change management point settings for site system and site code
```
PS XYZ:\> Set-CMManagementPoint -SiteSystemServerName "CMDEV-TEST02.TSQA.CORP.CONTOSO.COM" -SiteCode "CM2" -EnableSSL $False -UseSiteDatabase $True
```

This command changes settings for a management point in a Configuration Manager installation.
The command specifies the following information about the management point:

- The new management point appears on the site system named CMDEV-TEST02.TSQA.CONTOSO.COM.
- The site has code CM2.
- The management point queries a site database for information.
- The command enables SSL for the management point.

### Example 2: Change management point settings for site system and site code, connection type, and database name
```
PS XYZ:\> Set-CMManagementPoint -SiteSystemServerName "CMDEV-TEST02.TSQA.CORP.CONTOSO.COM " -SiteCode "CM2" -ClientConnectionType InternetAndIntranet -AllowDevice $True -EnableSSL $True -GenerateAlert $False -UseSiteDatabase $False -SQLServerFqdnName "CMDEV-TEST02.TSQA.CORP.CONTOSO.COM" -SQLServerInstanceName "MSSQLServer" -DatabaseName "ContosoSQL01"
```

This command changes settings for a management point in a Configuration Manager installation.
The command specifies the following information about the management point:

- The new management point appears on the site system named CMDEV-TEST02.TSQA.CONTOSO.COM.
This name is also the fully qualified domain name for the SQL Server instance named MSSQLServer.
- The site has code CM2.
- The management point accepts connections from Internet and intranet clients and from portable devices.
- The management point has the associated database name ContosoSQL01.
- The command enables SSL for the management point.

## PARAMETERS

### -AllowDevice
Indicates whether the management point supports device clients.

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

### -ClientConnectionType
Specifies the type of the client connection.
The acceptable values for this parameter are:

- Internet
- InternetAndIntranet
- Intranet

```yaml
Type: ClientConnectionTypes
Parameter Sets: (All)
Aliases:
Accepted values: Internet, Intranet, InternetAndIntranet

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseName
Specifies the name of the site database or site database replica that the management point uses to query for site database information.

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

### -EnableCloudGateway
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

### -EnableSsl
Indicates whether to enable SSL.

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

### -GenerateAlert
Indicates whether the management point generates health alerts.

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

### -InputObject
Specifies the management point for which you change values by using a management point object.
To obtain a management point object, use the [Get-CMManagementPoint](Get-CMManagementPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: ManagementPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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
Specifies the site code of the Configuration Manager site that hosts the site system role.

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
Specifies the name of the server that hosts the site system role.

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

### -SqlServerFqdn
```yaml
Type: String
Parameter Sets: (All)
Aliases: SqlServerFqdnName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlServerInstanceName
Specifies the name of the SQL Server instance that clients use to communicate with the site system.

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

### -UseComputerAccount
Indicates that the management point uses its own computer account instead of a domain user account to access site database information.

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

### -UserName
Specifies a domain user account that the management point uses to access site information.

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

### -UseSiteDatabase
Indicates whether the management point queries a site database instead of a site database replica for information.

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

[Add-CMManagementPoint](Add-CMManagementPoint.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Remove-CMManagementPoint](Remove-CMManagementPoint.md)
