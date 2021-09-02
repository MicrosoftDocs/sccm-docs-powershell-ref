---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/01/2021
schema: 2.0.0
title: Set-CMBootImage
---

# Set-CMBootImage

## SYNOPSIS

Modify an OS boot image.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMBootImage [-AddOptionalComponent <IResultObject[]>] [-BackgroundBitmapPath <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-DeployFromPxeDistributionPoint <Boolean>] [-Description <String>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointMins <UInt32>]
 [-DisconnectUserFromDistributionPointRetryCount <UInt32>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-EnableBinaryDeltaReplication <Boolean>] [-EnableCommandSupport <Boolean>] [-EnablePrestartCommand <Boolean>]
 [-Force] [-IncludeFilesForPrestart <Boolean>] [-InputLocale <String>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-Path <String>] [-PersistContentInCache <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PrestartCommandLine <String>]
 [-PrestartIncludeFilesDirectory <String>] [-Priority <Priority>] [-Reload]
 [-RemoveOptionalComponent <IResultObject[]>] [-ScratchSpace <UInt32>]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMBootImage [-AddOptionalComponent <IResultObject[]>] [-BackgroundBitmapPath <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-DeployFromPxeDistributionPoint <Boolean>] [-Description <String>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointMins <UInt32>]
 [-DisconnectUserFromDistributionPointRetryCount <UInt32>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-EnableBinaryDeltaReplication <Boolean>] [-EnableCommandSupport <Boolean>] [-EnablePrestartCommand <Boolean>]
 [-Force] -Id <String> [-IncludeFilesForPrestart <Boolean>] [-InputLocale <String>] [-NewName <String>]
 [-PassThru] [-Path <String>] [-PersistContentInCache <Boolean>] [-PrestageBehavior <PrestageBehavior>]
 [-PrestartCommandLine <String>] [-PrestartIncludeFilesDirectory <String>] [-Priority <Priority>] [-Reload]
 [-RemoveOptionalComponent <IResultObject[]>] [-ScratchSpace <UInt32>]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMBootImage [-AddOptionalComponent <IResultObject[]>] [-BackgroundBitmapPath <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-DeployFromPxeDistributionPoint <Boolean>] [-Description <String>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointMins <UInt32>]
 [-DisconnectUserFromDistributionPointRetryCount <UInt32>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-EnableBinaryDeltaReplication <Boolean>] [-EnableCommandSupport <Boolean>] [-EnablePrestartCommand <Boolean>]
 [-Force] [-IncludeFilesForPrestart <Boolean>] [-InputLocale <String>] -Name <String> [-NewName <String>]
 [-PassThru] [-Path <String>] [-PersistContentInCache <Boolean>] [-PrestageBehavior <PrestageBehavior>]
 [-PrestartCommandLine <String>] [-PrestartIncludeFilesDirectory <String>] [-Priority <Priority>] [-Reload]
 [-RemoveOptionalComponent <IResultObject[]>] [-ScratchSpace <UInt32>]
 [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to modify an OS boot image. Boot images are Windows Preinstallation Environment (Windows PE) images into which you boot a client computer before you install an OS.

You can add device drivers to a boot image or change its properties. Before you can add a new device driver, you must first import the driver to the Configuration Manager driver catalog and enable it.

Each version of Configuration Manager supports a specific version of the Windows Assessment and Deployment Kit (Windows ADK). You can service, or customize, boot images when they're based on a Windows PE version from the supported version of Windows ADK.

For more information, see [Manage boot images with Configuration Manager](/mem/configmgr/osd/get-started/manage-boot-images).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a boot image

This command gets a boot image by its package ID, and then renames it.

```powershell
Set-CMBootimage -Id "CM100004" -NewName "Custom boot image"
```

### Example 2: Set descriptive properties

This command gets a boot image by its name, and then adds a version and description to it.

```powershell
Set-CMBootImage -Name "Custom boot image (x64)" -Version "Contoso v2.1" -Description "Managed by jqpublic"
```

### Example 3: Set the keyboard layout

The following example sets the default keyboard layout of the boot image to the **Russian (Russia)** language. It identifies the boot image by its ID.

```powershell
Set-CMBootimage -Id "CM100004" -InputLocale "ru-ru"
```

### Example 4: Add optional components

This example gets the .NET and PowerShell optional components, and then adds them to the boot image.

```powershell
$netfxOC = Get-CMWinPEOptionalComponentInfo -Architecture 'x64' -Name 'WinPE-NetFX' -LanguageId 1033
$pwshOC = Get-CMWinPEOptionalComponentInfo -Architecture 'x64' -Name 'WinPE-PowerShell' -LanguageId 1033
$OCs = @($netfxOC, $pwshOC)

Set-CMBootImage -Id 'XYZ00556' -AddOptionalComponent $OCs
```

## PARAMETERS

### -AddOptionalComponent

Specify an array of optional component objects to add to the boot image. To get this object, use the [Get-CMWinPEOptionalComponentInfo](Get-CMWinPEOptionalComponentInfo.md) cmdlet.

The following components are commonly used:

- Microsoft .NET (WinPE-NetFX): This component is a prerequisite for PowerShell. It's one of the larger optional components.
- Windows PowerShell (WinPE-PowerShell): This component requires .NET, and adds limited PowerShell support. If you run custom PowerShell scripts during the WinPE phase of your task sequence, add this component. There are other components that may be required for other PowerShell cmdlets.
- HTML (WinPE-HTA): If you run custom HTML applications during the WinPE phase of your task sequence, add this component.

For more information, see [Manage boot images - optional components](/mem/configmgr/osd/get-started/manage-boot-images#optional-components).

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddOptionalComponents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BackgroundBitmapPath

Specify the network file path of a custom background image file to use in Windows PE.

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

### -CopyToPackageShareOnDistributionPoint

Clients can always download a boot image from a distribution point. If you set this parameter to **$true**, the site makes it available via a named network share on distribution points. Use **CustomPackageShareName** to specify a custom share name.

When you enable this option, more space is required on distribution points. It applies to all distribution points to which you distribute this boot image.

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

### -DeployFromPxeDistributionPoint

Set this parameter to **$true** to make this boot image available from a PXE-enabled distribution point. For more information, see [Use PXE to deploy Windows over the network](/mem/configmgr/osd/deploy-use/use-pxe-to-deploy-windows-over-the-network).

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

### -Description

Specify an optional description of a boot image to help you identify it.

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

This option is deprecated. It sets the **ForcedDisconnectEnabled** property of the boot image.

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

This option is deprecated. It sets the **ForcedDisconnectDelay** property of the boot image.

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

This option is deprecated. It sets the **ForcedDisconnectNumRetries** property of the boot image.

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

### -EnableCommandSupport

In non-production, test environments only, you can set this parameter to **$true** to enable command support. When a device boots to this image, you can press **F8** to open an administrative command prompt. This option is useful for troubleshooting while you're testing your deployment. Using this setting in a production deployment isn't advised because of security concerns.

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

### -EnablePrestartCommand

Set this parameter to **$true** to enable a prestart command. This command line runs before the task sequence starts.

Also configure the following parameters: **IncludeFilesForPrestart**, **PrestartCommandLine**, **PrestartIncludeFilesDirectory**.

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

### -Force

Run the command without asking for confirmation.

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

### -Id

Specify a boot image ID to configure. This value is a standard package ID, for example: `XYZ00002`.

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

### -IncludeFilesForPrestart

If you enable **EnablePrestartCommand**, use this parameter if your prestart command requires other files to run. Then use the **PrestartIncludeFilesDirectory** parameter to specify the location of the files to include.

For example, if you want to run a batch script, use this option to include the script file.

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

### -InputLocale

Use this parameter to configure the default keyboard layout for a boot image. Specify the _language tag_. For example, to set the input locale to Russian (Russia), specify the string `ru-ru`. For more information, see [[MS-LCID]: Windows Language Code Identifier (LCID) Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

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

### -InputObject

Specify a boot image object to configure. To get this object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

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

### -Name

Specify the name of a boot image to configure.

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

Specify a new name for the boot image.

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

Specify the network path of the Windows PE image that this boot image uses. You can't change the path for default boot images.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ImagePath

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

### -PrestartCommandLine

If you enable **EnablePrestartCommand**, use this parameter to specify the command line to run. The maximum length is 4096 characters.

If the command line requires files that aren't in Windows PE, use the **IncludeFilesForPrestart** and **PrestartIncludeFilesDirectory** parameters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CommandLine

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestartIncludeFilesDirectory

If you enable **EnablePrestartCommand** and **IncludeFilesForPrestart**, use this parameter to specify the network path of the files to include in the boot image.

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

### -Reload

Applies to version 2006 and later. If the versions of the Windows ADK components in the boot image are out of date, add this parameter to reload the boot image with the current Windows PE version from the Windows ADK. For more information, see [Update distribution points with the boot image](/mem/configmgr/osd/get-started/manage-boot-images#update-distribution-points-with-the-boot-image).

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ReloadImage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOptionalComponent

Specify an array of optional component objects to remove from the boot image. To get this object, use the [Get-CMWinPEOptionalComponentInfo](Get-CMWinPEOptionalComponentInfo.md) cmdlet.

Don't remove the following components, which are required by Configuration Manager:

- Scripting (WinPE-Scripting)
- Startup (WinPE-SecureStartup)
- Network (WinPE-WDS-Tools)
- Scripting (WinPE-WMI)

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveOptionalComponents

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ScratchSpace

Configure the Windows PE scratch space, which is temporary storage (RAM drive) used by WinPE. For example, when an application is run within WinPE and needs to write temporary files, WinPE redirects the files to the scratch space in memory to simulate the presence of a hard disk. By default, this amount is 512 MB for devices with more than 1 GB of RAM, otherwise the default is 32 MB.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:
Accepted values: 32, 64, 128, 256, 512

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

Specify the version of the boot image. This value isn't the OS version, but a string that you manage.

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

[Get-CMBootImage](Get-CMBootImage.md)

[New-CMBootImage](New-CMBootImage.md)

[Remove-CMBootImage](Remove-CMBootImage.md)

[Get-CMWinPEOptionalComponentInfo](Get-CMWinPEOptionalComponentInfo.md)

[Manage boot images with Configuration Manager](/mem/configmgr/osd/get-started/manage-boot-images)
