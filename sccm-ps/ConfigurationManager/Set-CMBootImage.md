---
description: Modifies an operating system boot image.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
schema: 2.0.0
title: Set-CMBootImage
---

# Set-CMBootImage

## SYNOPSIS
Modifies an operating system boot image.

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
The **Set-CMBootImage** cmdlet modifies an operating system boot image.
Boot images are Windows Preinstallation Environment (Windows PE) images into which you boot a client computer before you install an operating system.

You can add device drivers to a boot image or change its properties.
Before you can add a new device driver, you must first import the driver to the Configuration Manager driver catalog and enable it.

A modification to the boot image does not change its source package.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a boot image object that is identified by using its ID

This command retrieves a boot image by using its ID, and then renames the boot image. Depending on replication issues, this modification can take a long time to display in the Configuration Manager console.

```powershell
Set-CMBootimage -Id "CM100004" -NewName "Windows8 (x64)"
```

### Example 2: Rename a boot image object that is identified by using its name

This command retrieves a boot image by using its name, and then renames the boot image. It also adds a version and description to the boot image object. Depending on replication issues, this modification can take a long time to display in the Configuration Manager console.

```powershell
Set-CMBootImage -Name "Boot Image (x64)" -NewName "Windows 8 x64" -Version "6.2.8400.1" -Description "Microsoft Windows 8 PE (x64)"
```

### Example 3: Set the keyboard layout

The following example sets the default keyboard layout of the boot image to the **Russian (Russia)** language. It identifies the boot image by its ID.

```powershell
Set-CMBootimage -Id "CM100004" -InputLocale "ru-ru"
```

## PARAMETERS

### -AddOptionalComponent
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
Describes the contents of a boot image.

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
Forces the command to run without asking for user confirmation.

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
Specifies an array of boot image identifiers.

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
Starting in version 1910, use this parameter to configure the default keyboard layout for a boot image. It's the same setting as the **Set default keyboard layout in WinPE** option on the Customization tab of a boot image. For example, to set the input locale to Russian (Russia), specify the string `ru-ru`.

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
Specifies a boot image object.

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
Specifies a name of a boot image.

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
Specifies a new name for the boot image.

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

Applies to version 2006 and later. If the version of the Windows ADK components in the boot image are out of date, use this parameter to reload this boot image with the current Windows PE version from the Windows ADK. For more information on this process, see [Update distribution points with the boot image](/mem/configmgr/osd/get-started/manage-boot-images#update-distribution-points-with-the-boot-image).

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
Specifies the version of the boot image.

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
