---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/26/2021
schema: 2.0.0
title: Set-CMPackage
---

# Set-CMPackage

## SYNOPSIS

Modify a package.

## SYNTAX

### SetByValue (Default)
```
Set-CMPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetry <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>]
 [-InputObject] <IResultObject> [-Language <String>] [-Manufacturer <String>] [-MifFileName <String>]
 [-MifName <String>] [-MifPublisher <String>] [-MifVersion <String>] [-MulticastAllow <Boolean>]
 [-MulticastEncrypt <Boolean>] [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru]
 [-Path <String>] [-PersistContentInCache <Boolean>] [-PrestageBehavior <PrestageBehavior>]
 [-Priority <Priorities>] [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetry <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>] -Id <String>
 [-Language <String>] [-Manufacturer <String>] [-MifFileName <String>] [-MifName <String>]
 [-MifPublisher <String>] [-MifVersion <String>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru] [-Path <String>]
 [-PersistContentInCache <Boolean>] [-PrestageBehavior <PrestageBehavior>] [-Priority <Priorities>]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetry <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-EnableBinaryDeltaReplication <Boolean>]
 [-Language <String>] [-Manufacturer <String>] [-MifFileName <String>] [-MifName <String>]
 [-MifPublisher <String>] [-MifVersion <String>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] -Name <String> [-NewName <String>] [-PassThru] [-Path <String>]
 [-PersistContentInCache <Boolean>] [-PrestageBehavior <PrestageBehavior>] [-Priority <Priorities>]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change the settings of a package. For more information, see [Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a package and add a description

This command renames the package that has the ID **ST120001** to **ScriptsPackage02** and adds a description.

```powershell
Set-CMPackage -Id "ST120001" -NewName "ScriptsPackage02" -Description "This package deploys scripts that run on a recurring schedule."
```

### Example 2: Change the package source path

The first command gets the package that has the ID **ST120001**, and stores the results in the **$Pkg** variable. The second command changes the package source path.

```powershell
$pkg = Get-CMPackage -Id "ST120001"
Set-CMPackage -InputObject $pkg -Path "\\sources\cmpkg$\newpkg01"
```

## PARAMETERS

### -CopyToPackageShareOnDistributionPoint

Clients can always download a package from a distribution point. If you set this parameter to **$true**, the site makes it available via a named network share on distribution points. Use **CustomPackageShareName** to specify a custom share name.

When you enable this option, more space is required on distribution points. It applies to all distribution points to which you distribute this package.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ShareContent, CopyToPackageShareOnDistributionPoints

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
Aliases: ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description of the package to help you identify it. You can use a maximum of 128 characters.

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
Aliases: ForceDisconnectEnabled, DisconnectUsersFromDistributionPoints

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
Aliases: ForcedDisconnectDelay, DisconnectUsersFromDistributionPointsMinutes, DisconnectUserFromDistributionPointsMins, DisconnectUserFromDistributionPointsMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointRetry

This option is deprecated. It sets the **ForcedDisconnectNumRetries** property of the driver package.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: ForceDisconnectNumRetries, DisconnectUsersFromDistributionPointsRetries

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

### -EnableBinaryDeltaReplication

Set this parameter to **$true** to enable binary differential replication (BDR). For more information, see [Fundamental concepts for content management in Configuration Manager](/mem/configmgr/core/plan-design/hierarchy/fundamental-concepts-for-content-management#binary-differential-replication).

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

### -Id

Specify the ID of a package to configure. This value is a standard package ID, for example: `XYZ00020`.

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

Specify a package object to configure. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Language

Specify a language string for the package. You can use a maximum of 32 characters in a format that you choose to use to identify the language version. To identify a package, Configuration Manager uses the **Language**, **Manufacturer**, **Name**, and **Version** parameters. For example, you can have an English version and a German version of the same package.

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

### -Manufacturer

Specify the manufacturer name for the software. You can use a maximum of 32 characters. To identify a package, Configuration Manager uses the **Language**, **Manufacturer**, **Name**, and **Version** parameters.

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

### -MifFileName

Specify the name of the Management Information Format (MIF) file that contains the package status. The file name extension must be `.mif`. Use a status MIF file to generate detailed status reporting. To generate a status MIF file, your application must call the InstallStatusMIF function. For more information, see [Status MIF Functions](/mem/configmgr/develop/reference/core/servers/manage/status-mif-functions).

If you set this parameter, when the client runs the deployment, the Configuration Manager client looks in the `%TEMP%` directory or the `%windir%` directory for the installation status MIF file that you specify. The installation status indicates whether the program successfully ran.

If the client doesn't find the file, it searches for all MIF files in those directories. It makes a case-insensitive comparison of the values that you specify for **MifName**, **MifPublisher**, and **MifVersion** to the values that the MIF file specifies. If the client finds a match, it uses the status that the MIF file specifies as the installation status for the program. If it can't find a match, or if you don't specify **MifFileName**, the client uses the program exit code to set the installation status for the program. An exit code of zero indicates that the program successfully ran. Any other values indicate application-specific error codes.

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

### -MifName

Specify the name of the package for MIF matching, up to 50 characters. For more information, see the **MifFileName** parameter.

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

### -MifPublisher

Specify the software publisher of the package for MIF matching, up to 32 characters. For more information, see the **MifFileName** parameter.

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

### -MifVersion

Specify the version number of the package for MIF matching, up to 32 characters. For more information, see the **MifFileName** parameter.

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

Specify a package name. You can use a maximum of 250 characters. To identify a package, Configuration Manager uses the **Language**, **Manufacturer**, **Name**, and **Version** parameters.

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

Use this parameter to rename a package.

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

### -Path

If the package contains source files, specify the location of the files. You can specify either a full local path on the site server, or a network path. Make sure that this location contains all the files and subdirectories that the program needs to run, including any scripts.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistContentInCache

If you don't want the content of this package to age out of the client cache to make room for other content, set this parameter to **$true** to persist it in the client cache.

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

The site sends high priority content before packages with normal or low priority. Packages with equal priority are sent in the order in which they're created.

```yaml
Type: Priorities
Parameter Sets: (All)
Aliases: DistributionPriority
Accepted values: High, Normal, Low

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

Specify a version number for the software. The maximum length of this string is 32 characters. To identify a package, Configuration Manager uses the **Language**, **Manufacturer**, **Name**, and **Version** parameters.

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

Add this parameter to prompt for confirmation before the cmdlet runs.

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

[Export-CMPackage](Export-CMPackage.md)

[Get-CMPackage](Get-CMPackage.md)

[Import-CMPackage](Import-CMPackage.md)

[New-CMPackage](New-CMPackage.md)

[Remove-CMPackage](Remove-CMPackage.md)

[Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs)
