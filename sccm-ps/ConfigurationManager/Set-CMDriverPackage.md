---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/01/2021
schema: 2.0.0
title: Set-CMDriverPackage
---

# Set-CMDriverPackage

## SYNOPSIS

Modify a driver package.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDriverPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-DriverManufacturer <String>] [-DriverModel <String>]
 [-DriverPackageSource <String>] -InputObject <IResultObject> [-MulticastAllow <Boolean>]
 [-MulticastEncrypt <Boolean>] [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru]
 [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMDriverPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-DriverManufacturer <String>] [-DriverModel <String>]
 [-DriverPackageSource <String>] -Id <String> [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru] [-PrestageBehavior <PrestageBehavior>]
 [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMDriverPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-DriverManufacturer <String>] [-DriverModel <String>]
 [-DriverPackageSource <String>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] -Name <String> [-NewName <String>] [-PassThru]
 [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to modify a driver package.

For more information, see [Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Configure the manufacturer and model of a driver package

This command configures the manufacturer and model of the driver package with the ID **XYZ00091**.

```powershell
Set-CMDriverPackage -PackageId "XYZ00091" -DriverManufacturer "Microsoft" -DriverModel "Surface 2"
```

## PARAMETERS

### -CopyToPackageShareOnDistributionPoint

Clients can always download a driver package from a distribution point. If you set this parameter to **$true**, the site makes it available via a named network share on distribution points. Use **CustomPackageShareName** to specify a custom share name.

When you enable this option, more space is required on distribution points. It applies to all distribution points to which you distribute this driver package.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CopyToPackageShareOnDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomPackageShareName

If you enable **CopyToPackageShareOnDistributionPoint**, you can use this parameter to customize the share name. The maximum length is 127 characters, and can't include any of the following characters: `" / [ ] : | < > + = ; , ? *`. You can specify a share name and a folder name, but then the maximum for each is 80 characters. For example, `ShareName\FolderName`.

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

### -Description

Specify an optional description of a driver package to help you identify it.

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

### -DisconnectUserFromDistributionPoint

This option is deprecated. It sets the **ForcedDisconnectEnabled** property of the driver package.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointMins

This option is deprecated. It sets the **ForcedDisconnectDelay** property of the driver package.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPointsMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointRetryCount

This option is deprecated. It sets the **ForcedDisconnectNumRetries** property of the driver package.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPointsRetries

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointUpdateSchedule

Use this parameter to update distribution points on a schedule. To get a schedule object, use the [New-CMSchedule](New-CMSchedule.md) cmdlet.

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

### -DriverManufacturer

Use this parameter to set the manufacturer of the device. The maximum length is 100 characters.

Use it with the **DriverModel** parameter. You can use them for managing the driver catalog, and with task sequence pre-caching. For more information, see [Configure pre-cache content for task sequences](/mem/configmgr/osd/deploy-use/configure-precache-content).

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

### -DriverModel

Use this parameter to set the model of the device. The maximum length is 100 characters.

Use it with the **DriverManufacturer** parameter. You can use them for managing the driver catalog, and with task sequence pre-caching. For more information, see [Configure pre-cache content for task sequences](/mem/configmgr/osd/deploy-use/configure-precache-content).

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

### -DriverPackageSource

Specify a file path to the network location to source the driver files.

When you create a driver package, the source location of the package must point to an empty network share that's not used by another driver package. The SMS Provider must have **Full control** permissions to that location.

When you add device drivers to a driver package, Configuration Manager copies it to this path. You can add to a driver package only device drivers that you've imported and that are enabled in the driver catalog.

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

### -Id

Specify the ID of a driver package to configure. This value is a standard package ID, for example: `XYZ00020`.

```yaml
Type: String
Parameter Sets: SetById
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a driver package object to configure. To get this object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MulticastAllow

Set this parameter to **$true** to allow this package to be transferred via multicast. For more information, see [Use multicast to deploy Windows over the network with Configuration Manager](/mem/configmgr/osd/deploy-use/use-multicast-to-deploy-windows-over-the-network).

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

### -MulticastEncrypt

If you enable **MulticastAllow**, set this parameter to **$true** to encrypt multicast packages.

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

### -MulticastTransferOnly

If you enable **MulticastAllow**, set this parameter to **$true** to only transfer this driver package via multicast.

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

### -Name

Specify the name of a driver package to configure.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specify a new name for the driver package.

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

### -PrestageBehavior

Specify the behavior when you enable a distribution point for prestaged content:

- `ManualCopy`: Manually copy the content in this package to the distribution point
- `DownloadDelta`: Download only content changes to the distribution point
- `OnDemand`: Automatically download content when packages are assigned to distribution points

For more information, see [Use prestaged content](/mem/configmgr/core/servers/deploy/configure/deploy-and-manage-content#bkmk_prestage).

```yaml
Type: PrestageBehavior
Parameter Sets: (All)
Aliases:
Accepted values: ManualCopy, DownloadDelta, OnDemand

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority

Specify the order in which the site sends the content to other sites and the distribution points in this site.

The site sends high priority content before packages with medium or low priority. Packages with equal priority are sent in the order in which they're created.

```yaml
Type: Priority
Parameter Sets: (All)
Aliases:
Accepted values: High, Medium, Low

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendToPreferredDistributionPoint

If you want to enable on-demand content distribution to preferred distribution points, set this parameter to **$true**. When you enable this setting, if a client requests the content for the package and the content isn't available on any distribution points, then the management point distributes the content. For more information, see [On-demand content distribution](/mem/configmgr/core/plan-design/hierarchy/fundamental-concepts-for-content-management#on-demand-content-distribution).

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: SendToPreferredDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version

Specify the version of the driver package. This value is a string that you manage.

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

### System.Object
## NOTES

## RELATED LINKS

[Export-CMDriverPackage](Export-CMDriverPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Import-CMDriverPackage](Import-CMDriverPackage.md)

[New-CMDriverPackage](New-CMDriverPackage.md)

[Remove-CMDriverPackage](Remove-CMDriverPackage.md)

[Manage drivers in Configuration Manager](/mem/configmgr/osd/get-started/manage-drivers)
