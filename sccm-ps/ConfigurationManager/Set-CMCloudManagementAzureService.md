---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
online version:
schema: 2.0.0
---

# Set-CMCloudManagementAzureService

## SYNOPSIS

Modify the settings of the Azure service for **Cloud Management** in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMCloudManagementAzureService [-AddGroupName <String[]>] [-DeleteGroupName <String[]>]
 [-Description <String>] [-EnableAADGroupSync <Boolean>] [-EnableGroupDeltaDiscovery <Boolean>]
 [-EnableGroupDiscovery <Boolean>] [-EnableUserDeltaDiscovery <Boolean>] [-EnableUserDiscovery <Boolean>]
 [-GroupDeltaDiscoveryMins <Int32>] [-GroupDiscoverySchedule <IResultObject>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-UserDeltaDiscoveryMins <Int32>] [-UserDiscoverySchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMCloudManagementAzureService [-AddGroupName <String[]>] [-DeleteGroupName <String[]>]
 [-Description <String>] [-EnableAADGroupSync <Boolean>] [-EnableGroupDeltaDiscovery <Boolean>]
 [-EnableGroupDiscovery <Boolean>] [-EnableUserDeltaDiscovery <Boolean>] [-EnableUserDiscovery <Boolean>]
 [-GroupDeltaDiscoveryMins <Int32>] [-GroupDiscoverySchedule <IResultObject>] -Id <Int32> [-NewName <String>]
 [-PassThru] [-UserDeltaDiscoveryMins <Int32>] [-UserDiscoverySchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMCloudManagementAzureService [-AddGroupName <String[]>] [-DeleteGroupName <String[]>]
 [-Description <String>] [-EnableAADGroupSync <Boolean>] [-EnableGroupDeltaDiscovery <Boolean>]
 [-EnableGroupDiscovery <Boolean>] [-EnableUserDeltaDiscovery <Boolean>] [-EnableUserDiscovery <Boolean>]
 [-GroupDeltaDiscoveryMins <Int32>] [-GroupDiscoverySchedule <IResultObject>] -Name <String>
 [-NewName <String>] [-PassThru] [-UserDeltaDiscoveryMins <Int32>] [-UserDiscoverySchedule <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to modify the settings of an Azure service in Configuration Manager for **Cloud Management**.

For more information about the **Cloud Management** service, see [CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMAzureService** cmdlet to get the service from the site. It then passes that object with the pipeline operator to **Set-CMCloudManagementAzureService**, which renames it and sets the description.

```powershell
Get-CMAzureService -Name "Contoso" | Set-CMCloudManagementAzureService -NewName "CMG service" -Description "ConfigMgr connection to Contoso tenant for CMG"
```

## PARAMETERS

### -AddGroupName

Specify a Microsoft Entra group name to discover. Use this parameter with the **EnableGroupDiscovery** parameter.

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

### -DeleteGroupName

Specify a Microsoft Entra group name to remove from discovery.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DeleteGroupNames

Required: False
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

### -EnableAADGroupSync

Enable Configuration Manager to sync collections to groups in Microsoft Entra ID. For more information, see [Synchronize members to Microsoft Entra groups](/mem/configmgr/core/clients/manage/collections/create-collections#bkmk_aadcollsync).

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

### -EnableGroupDeltaDiscovery

Set this parameter to `true` to enable delta discovery for Microsoft Entra group discovery. Use this parameter with the **EnableGroupDiscovery** parameter. Use the **GroupDeltaDiscoveryMins** parameter to configure the delta discovery interval.

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

Set this parameter to `true` to enable Microsoft Entra group discovery. When you enable this discovery method, also configure the following parameters:

- **AddGroupName**: Add Microsoft Entra groups to discover
- **EnableGroupDeltaDiscovery**: Configure delta discovery
- **GroupDeltaDiscoveryMins**: Delta discovery interval
- **GroupDiscoverySchedule**: Full polling schedule

For more information on this discovery method, see [Microsoft Entra user group discovery](/mem/configmgr/core/servers/deploy/configure/about-discovery-methods#bkmk_azuregroupdisco).


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

Set this parameter to `true` to enable delta discovery for Microsoft Entra user discovery. Use this parameter with the **EnableUserDiscovery** parameter.

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

Set this parameter to `true` to enable Microsoft Entra user discovery. When you enable this discovery method, also configure the following parameters:

- **EnableUserDeltaDiscovery**: Configure delta discovery
- **UserDeltaDiscoveryMins**: Delta discovery interval
- **UserDiscoverySchedule**: Full polling schedule

For more information on this discovery method, see [Microsoft Entra user discovery](/mem/configmgr/core/servers/deploy/configure/about-discovery-methods#azureaddisc).

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

When you enable delta discovery for Microsoft Entra group discovery with the **EnableGroupDeltaDiscovery** parameter, use this parameter to configure the delta discovery interval. The integer value you specify is the polling interval in minutes.

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

Specify a schedule object for the Microsoft Entra group discovery full polling schedule. To get this object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -Id

Specify the site's ID for the Azure service. The **Id** is the integer value stored in the site database for the service. For example, run the following SQL query, and look at the **ID** column: `select * from Azure_CloudService`.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an Azure service object to configure. To get this object, use the [Get-CMAzureService](Get-CMAzureService.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: AzureService

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify a name to distinguish the **Cloud Management** service in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: AzureServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename the **Cloud Management** service in Configuration Manager.

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

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -UserDeltaDiscoveryMins

When you enable delta discovery for Microsoft Entra user discovery with the **EnableUserDeltaDiscovery** parameter, use this parameter to configure the delta discovery interval. The integer value you specify is the polling interval in minutes.

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

Specify a schedule object for the Microsoft Entra user discovery full polling schedule. To get this object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Import-CMAADServerApplication](Import-CMAADServerApplication.md)

[Import-CMAADClientApplication](Import-CMAADClientApplication.md)

[New-CMCloudManagementAzureService](New-CMCloudManagementAzureService.md)

[New-CMCloudManagementGateway](New-CMCloudManagementGateway.md)

[Add-CMCloudManagementGatewayConnectionPoint](Add-CMCloudManagementGatewayConnectionPoint.md)

[CMG Overview](/mem/configmgr/core/clients/manage/cmg/overview)
