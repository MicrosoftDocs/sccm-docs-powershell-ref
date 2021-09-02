---
description: Adds a management point to Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Add-CMManagementPoint
---

# Add-CMManagementPoint

## SYNOPSIS
Adds a management point to Configuration Manager.

## SYNTAX

### ByValueNoReplica (Default)
```
Add-CMManagementPoint [-AllowDevice] [-ClientConnectionType <ClientConnectionTypes>]
 [-CommunicationType <ComputerCommunicationType>] [-ConnectionAccountUserName <String>] [-EnableCloudGateway]
 [-EnableSsl] [-GenerateAlert] [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameNoReplica
```
Add-CMManagementPoint [-AllowDevice] [-ClientConnectionType <ClientConnectionTypes>]
 [-CommunicationType <ComputerCommunicationType>] [-ConnectionAccountUserName <String>] [-EnableCloudGateway]
 [-EnableSsl] [-GenerateAlert] [-SiteCode <String>] [-SiteSystemServerName] <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameReplica
```
Add-CMManagementPoint [-AllowDevice] [-ClientConnectionType <ClientConnectionTypes>]
 [-CommunicationType <ComputerCommunicationType>] [-ConnectionAccountUserName <String>] -DatabaseName <String>
 [-EnableCloudGateway] [-EnableSsl] [-GenerateAlert] [-SiteCode <String>] [-SiteSystemServerName] <String>
 -SqlServerFqdn <String> [-SqlServerInstanceName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueReplica
```
Add-CMManagementPoint [-AllowDevice] [-ClientConnectionType <ClientConnectionTypes>]
 [-CommunicationType <ComputerCommunicationType>] [-ConnectionAccountUserName <String>] -DatabaseName <String>
 [-EnableCloudGateway] [-EnableSsl] [-GenerateAlert] [-InputObject] <IResultObject> -SqlServerFqdn <String>
 [-SqlServerInstanceName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMManagementPoint** cmdlet adds a management point to Configuration Manager.
A management point is a Configuration Manager site system role that provides policy and service information to clients and receives configuration data from clients.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a management point
```
PS XYZ:\>Add-CMManagementPoint -SiteSystemServerName "CMDEV-TEST02.TSQA.CONTOSO.COM" -SiteCode "CM2" -ClientConnectionType InternetAndIntranet -AllowDevice $True -GenerateAlert -SQLServerFqdnName "CMDEV-TEST02.TSQA.CONTOSO.COM" -SQLServerInstanceName "MSSQLServer" -DatabaseName "test" -UserName "TSQA\MPAdmin" -Verbose
```

This command adds a management point to a Configuration Manager installation.
The command specifies the following information about the management point:

- The new management point appears on the site system named CMDEV-TEST02.TSQA.CONTOSO.COM.
This name is also the fully qualified domain name for the SQL Server instance named MSSQLServer.
- The site has code CM2.
- The management point accepts connections from internet and intranet clients and from portable devices.
- The management point has the associated database name Test.
- The management point uses the domain user account for the user named TSQA\MPAdmin.
- The cmdlet displays all messages that the addition operation generates.

## PARAMETERS

### -AllowDevice
Indicates that the management point supports device clients.

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

### -ClientConnectionType
Specifies the type of the client connection.
Valid values are:

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

### -CommunicationType
```yaml
Type: ComputerCommunicationType
Parameter Sets: (All)
Aliases: ClientCommunicationType
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionAccountUserName
```yaml
Type: String
Parameter Sets: (All)
Aliases: UserName

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
Parameter Sets: ByNameReplica, ByValueReplica
Aliases:

Required: True
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSsl
Indicates that the cmdlet enables SSL for the management point.

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

### -GenerateAlert
Indicates that Configuration Manager generates an alert when the management point is not healthy.

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
Parameter Sets: ByValueNoReplica, ByValueReplica
Aliases: SiteServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code of the Configuration Manager site that hosts the site system role.

```yaml
Type: String
Parameter Sets: ByNameNoReplica, ByNameReplica
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
Parameter Sets: ByNameNoReplica, ByNameReplica
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
Parameter Sets: ByNameReplica, ByValueReplica
Aliases: SqlServerFqdnName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SqlServerInstanceName
Specifies the name of the SQL Server instance that clients use to communicate with the site system.

```yaml
Type: String
Parameter Sets: ByNameReplica, ByValueReplica
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

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Remove-CMManagementPoint](Remove-CMManagementPoint.md)

[Set-CMManagementPoint](Set-CMManagementPoint.md)
