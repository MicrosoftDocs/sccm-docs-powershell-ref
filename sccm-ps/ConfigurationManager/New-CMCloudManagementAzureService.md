---
external help file: AdminUI.PS.HS.dll-Help.xml
Module Name: ConfigurationManager
online version:
ms.date: 11/20/2020
schema: 2.0.0
---

# New-CMCloudManagementAzureService

## SYNOPSIS

Create the Azure service for **Cloud Management** in Configuration Manager.

## SYNTAX

```
New-CMCloudManagementAzureService [-AddGroupName <String[]>] [-AzureEnvironmentOption <AzureEnvironment>]
 -ClientApp <IResultObject> [-Description <String>] [-EnableGroupDeltaDiscovery <Boolean>]
 [-EnableGroupDiscovery <Boolean>] [-EnableUserDeltaDiscovery <Boolean>] [-EnableUserDiscovery <Boolean>]
 [-GroupDeltaDiscoveryMins <Int32>] [-GroupDiscoverySchedule <IResultObject>] -Name <String>
 -ServerApp <IResultObject> [-UserDeltaDiscoveryMins <Int32>] [-UserDiscoverySchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create the Azure service in Configuration Manager for **Cloud Management**.

For more information on how to use this cmdlet to create a cloud management gateway (CMG), see [2010 release notes: Cloud management gateway](/powershell/sccm/2010-release-notes#cloud-management-gateway).

For more information about the **Cloud Management** service, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

## EXAMPLES

### Example 1

This example first gets the previously imported server and client apps using the [Get-CMAADApplication](Get-CMAADApplication.md) cmdlet. It then creates the service in the site for the global Azure cloud.

```powershell
$serverApp = Get-CMAADApplication -TenantName "Contoso" -AppType ServerApplication -AppName "CmgServerApp"

$clientApp = Get-CMAADApplication -TenantName "Contoso" -AppType ClientApplication -AppName "CmgClientApp"

New-CMCloudManagementAzureService -Name "Contoso" -Description "Azure Service" -ServerApp $serverApp -ClientApp $clientApp -AzureEnvironmentOption AzurePublicCloud
```

## PARAMETERS

### -AddGroupName

Specify an Azure Active Directory (Azure AD) group name to discover. Use this parameter with the **EnableGroupDiscovery** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddGroupNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureEnvironmentOption

Specify whether this service is in the global Azure cloud (`AzurePublicCloud`), or the Azure Government cloud (`AzureUSGovernmentCloud`).

```yaml
Type: AzureEnvironment
Parameter Sets: (All)
Aliases:
Accepted values: AzurePublicCloud, AzureUSGovernmentCloud

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientApp

Specify an object for the client app registration. To get this app, use the [Get-CMAADApplication](Get-CMAADApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: ClientApplication, NativeClientApplication

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description for the service.

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

### -EnableGroupDeltaDiscovery

Set this parameter to `true` to enable delta discovery for Azure AD group discovery. Use this parameter with the **EnableGroupDiscovery** parameter. Use the **GroupDeltaDiscoveryMins** parameter to configure the delta discovery interval.

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

### -EnableGroupDiscovery

Set this parameter to `true` to enable Azure AD group discovery. When you enable this discovery method, also configure the following parameters:

- **AddGroupName**: Add Azure AD groups to discover
- **EnableGroupDeltaDiscovery**: Configure delta discovery
- **GroupDeltaDiscoveryMins**: Delta discovery interval
- **GroupDiscoverySchedule**: Full polling schedule

For more information on this discovery method, see [Azure Active Directory user group discovery](/mem/configmgr/core/servers/deploy/configure/about-discovery-methods#bkmk_azuregroupdisco).

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

### -EnableUserDeltaDiscovery

Set this parameter to `true` to enable delta discovery for Azure AD user discovery. Use this parameter with the **EnableUserDiscovery** parameter.

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

### -EnableUserDiscovery

Set this parameter to `true` to enable Azure AD user discovery. When you enable this discovery method, also configure the following parameters:

- **EnableUserDeltaDiscovery**: Configure delta discovery
- **UserDeltaDiscoveryMins**: Delta discovery interval
- **UserDiscoverySchedule**: Full polling schedule

For more information on this discovery method, see [Azure Active Directory user discovery](/mem/configmgr/core/servers/deploy/configure/about-discovery-methods#azureaddisc).

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

### -GroupDeltaDiscoveryMins

When you enable delta discovery for Azure AD group discovery with the **EnableGroupDeltaDiscovery** parameter, use this parameter to configure the delta discovery interval. The integer value you specify is the polling interval in minutes.

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

### -GroupDiscoverySchedule

Specify a schedule object for the Azure AD group discovery full polling schedule. To get this object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a name to distinguish the **Cloud Management** service in Configuration Manager.

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

### -ServerApp

Specify an object for the server app registration. To get this app, use the [Get-CMAADApplication](Get-CMAADApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: WebApp, WebApplication, ServerApplication

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDeltaDiscoveryMins

When you enable delta discovery for Azure AD user discovery with the **EnableUserDeltaDiscovery** parameter, use this parameter to configure the delta discovery interval. The integer value you specify is the polling interval in minutes.

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

### -UserDiscoverySchedule

Specify a schedule object for the Azure AD user discovery full polling schedule. To get this object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

```yaml
Type: IResultObject
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet isn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### IResultObject#SMS_Azure_CloudService

## NOTES

You can't enable Azure AD group sync when you create the service. To enable group sync, use the [Set-CMCloudManagementAzureService](Set-CMCloudManagementAzureService.md) cmdlet with the **EnableAADGroupSync** parameter.

## RELATED LINKS

[Get-CMAADApplication](Get-CMAADApplication.md)

[Import-CMAADServerApplication](Import-CMAADServerApplication.md)

[Import-CMAADClientApplication](Import-CMAADClientApplication.md)

[New-CMCloudManagementGateway](New-CMCloudManagementGateway.md)

[Add-CMCloudManagementGatewayConnectionPoint](Add-CMCloudManagementGatewayConnectionPoint.md)

[Set-CMCloudManagementAzureService](Set-CMCloudManagementAzureService.md)

[CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview)
