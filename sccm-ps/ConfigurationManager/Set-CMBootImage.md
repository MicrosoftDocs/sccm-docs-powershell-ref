---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: 1FF11796-0904-4BED-91C8-05DCC05CDDA3
online version: https://go.microsoft.com/fwlink/?linkid=833682
schema: 2.0.0
---

# Set-CMBootImage

## SYNOPSIS
Modifies an operating system boot image.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMBootImage -InputObject <IResultObject> [-NewName <String>] [-Version <String>] [-Description <String>]
 [-Path <String>] [-EnablePrestartCommand <Boolean>] [-PrestartCommandLine <String>]
 [-IncludeFilesForPrestart <Boolean>] [-PrestartIncludeFilesDirectory <String>]
 [-BackgroundBitmapPath <String>] [-ScratchSpace <UInt32>] [-EnableCommandSupport <Boolean>]
 [-PersistContentInCache <Boolean>] [-EnableBinaryDeltaReplication <Boolean>]
 [-DeployFromPxeDistributionPoint <Boolean>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-CustomPackageShareName <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointRetryCount <UInt32>] [-DisconnectUserFromDistributionPointMins <UInt32>]
 [-AddOptionalComponent <IResultObject[]>] [-RemoveOptionalComponent <IResultObject[]>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-Force] [-Priority <Priority>]
 [-SendToPreferredDistributionPoint <Boolean>] [-PrestageBehavior <PrestageBehavior>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMBootImage -Id <String> [-NewName <String>] [-Version <String>] [-Description <String>] [-Path <String>]
 [-EnablePrestartCommand <Boolean>] [-PrestartCommandLine <String>] [-IncludeFilesForPrestart <Boolean>]
 [-PrestartIncludeFilesDirectory <String>] [-BackgroundBitmapPath <String>] [-ScratchSpace <UInt32>]
 [-EnableCommandSupport <Boolean>] [-PersistContentInCache <Boolean>] [-EnableBinaryDeltaReplication <Boolean>]
 [-DeployFromPxeDistributionPoint <Boolean>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-CustomPackageShareName <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointRetryCount <UInt32>] [-DisconnectUserFromDistributionPointMins <UInt32>]
 [-AddOptionalComponent <IResultObject[]>] [-RemoveOptionalComponent <IResultObject[]>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-Force] [-Priority <Priority>]
 [-SendToPreferredDistributionPoint <Boolean>] [-PrestageBehavior <PrestageBehavior>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMBootImage -Name <String> [-NewName <String>] [-Version <String>] [-Description <String>] [-Path <String>]
 [-EnablePrestartCommand <Boolean>] [-PrestartCommandLine <String>] [-IncludeFilesForPrestart <Boolean>]
 [-PrestartIncludeFilesDirectory <String>] [-BackgroundBitmapPath <String>] [-ScratchSpace <UInt32>]
 [-EnableCommandSupport <Boolean>] [-PersistContentInCache <Boolean>] [-EnableBinaryDeltaReplication <Boolean>]
 [-DeployFromPxeDistributionPoint <Boolean>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-CustomPackageShareName <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointRetryCount <UInt32>] [-DisconnectUserFromDistributionPointMins <UInt32>]
 [-AddOptionalComponent <IResultObject[]>] [-RemoveOptionalComponent <IResultObject[]>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-Force] [-Priority <Priority>]
 [-SendToPreferredDistributionPoint <Boolean>] [-PrestageBehavior <PrestageBehavior>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMBootImage** cmdlet modifies an operating system boot image.
Boot images are Windows Preinstallation Environment (Windows PE) images into which you boot a client computer before you install an operating system.

You can add device drivers to a boot image or change its properties.
Before you can add a new device driver, you must first import the driver to the Microsoft System Center Configuration Manager driver catalog and enable it.

A modification to the boot image does not change its source package.

## EXAMPLES

### Example 1: Rename a boot image object that is identified by using its ID
```
PS C:\> Set-CMBootimage -Id "CM100004" -NewName "Windows8 (x64)"
```

This command retrieves a boot image by using its ID, and then renames the boot image.
Depending on replication issues, this modification can take a long time to display in the Configuration Manager console.

### Example 2: Rename a boot image object that is identified by using its name
```
PS C:\> Set-CMBootImage -Name "Boot Image (x64)" -NewName "Windows 8 x64" -Version "6.2.8400.1" -Description "Microsoft Windows 8 PE (x64)"
```

This command retrieves a boot image by using its name, and then renames the boot image.
The command also adds a version and description to the boot image object.
Depending on replication issues, this modification can take a long time to display in the Configuration Manager console.

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMBootImage](Get-CMBootImage.md)

[New-CMBootImage](New-CMBootImage.md)

[Remove-CMBootImage](Remove-CMBootImage.md)
