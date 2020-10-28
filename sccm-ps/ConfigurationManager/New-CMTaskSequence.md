---
description: Creates a task sequence in Configuration Manager.
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: New-CMTaskSequence
---

# New-CMTaskSequence

## SYNOPSIS

Creates a task sequence in Configuration Manager.

## SYNTAX

### NewBuildOSImage (Default)
```
New-CMTaskSequence [-BuildOperatingSystemImage] [-HighPerformance <Boolean>] -Name <String>
 [-Description <String>] -BootImagePackageId <String> -OperatingSystemImagePackageId <String>
 -OperatingSystemImageIndex <UInt32> [-ApplyAll <Boolean>] [-ProductKey <String>]
 [-InstallationLicensingMode <ServerLicensingMode>] [-MaximumServerConnection <Int32>]
 [-GeneratePassword <Boolean>] [-LocalAdminPassword <SecureString>] [-TimeZone <TimeZoneInfo>]
 -JoinDomain <JoinType> [-WorkgroupName <String>] [-DomainName <String>] [-DomainOrganizationUnit <String>]
 [-DomainAccount <String>] [-DomainPassword <SecureString>] [-ClientPackagePackageId <String>]
 [-InstallationProperty <String>] [-SoftwareUpdateStyle <SoftwareUpdateStyleType>]
 [-ApplicationName <String[]>] [-IgnoreInvalidApplication <Boolean>] [-CreatedBy <String>]
 [-ImageVersion <String>] [-ImageDescription <String>] -OperatingSystemFilePath <String>
 -OperatingSystemFileAccount <String> [-OperatingSystemFileAccountPassword <SecureString>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewInstallOSImage
```
New-CMTaskSequence [-InstallOperatingSystemImage] [-HighPerformance <Boolean>] -Name <String>
 [-Description <String>] -BootImagePackageId <String> -OperatingSystemImagePackageId <String>
 -OperatingSystemImageIndex <UInt32> [-ApplyAll <Boolean>] [-PartitionAndFormatTarget <Boolean>]
 [-ConfigureBitLocker <Boolean>] [-ProductKey <String>] [-InstallationLicensingMode <ServerLicensingMode>]
 [-GeneratePassword <Boolean>] [-LocalAdminPassword <SecureString>] [-TimeZone <TimeZoneInfo>]
 -JoinDomain <JoinType> [-WorkgroupName <String>] [-DomainName <String>] [-DomainOrganizationUnit <String>]
 [-DomainAccount <String>] [-DomainPassword <SecureString>] [-ClientPackagePackageId <String>]
 [-InstallationProperty <String>] [-CaptureUserSetting <Boolean>] [-UserStateMigrationToolPackageId <String>]
 [-SaveLocally <Boolean>] [-CaptureLocallyUsingLink <Boolean>] [-CaptureNetworkSetting <Boolean>]
 [-CaptureWindowsSetting <Boolean>] [-SoftwareUpdateStyle <SoftwareUpdateStyleType>]
 [-ApplicationName <String[]>] [-IgnoreInvalidApplication <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewInstallOSImageVhd
```
New-CMTaskSequence [-InstallOperatingSystemImageVhd] [-HighPerformance <Boolean>] -Name <String>
 [-Description <String>] -BootImagePackageId <String> -OperatingSystemImagePackageId <String>
 -OperatingSystemImageIndex <UInt32> [-ApplyAll <Boolean>] [-PartitionAndFormatTarget <Boolean>]
 [-ConfigureBitLocker <Boolean>] [-ProductKey <String>] [-InstallationLicensingMode <ServerLicensingMode>]
 [-GeneratePassword <Boolean>] [-LocalAdminPassword <SecureString>] [-TimeZone <TimeZoneInfo>]
 -JoinDomain <JoinType> [-WorkgroupName <String>] [-DomainName <String>] [-DomainOrganizationUnit <String>]
 [-DomainAccount <String>] [-DomainPassword <SecureString>] [-ClientPackagePackageId <String>]
 [-InstallationProperty <String>] [-ApplicationName <String[]>] [-IgnoreInvalidApplication <Boolean>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpgradeOSImage
```
New-CMTaskSequence [-UpgradeOperatingSystem] [-HighPerformance <Boolean>] -Name <String>
 -UpgradePackageId <String> [-ProductKey <String>] [-SoftwareUpdateStyle <SoftwareUpdateStyleType>]
 [-ApplicationName <String[]>] [-IgnoreInvalidApplication <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewCustom
```
New-CMTaskSequence [-CustomTaskSequence] [-HighPerformance <Boolean>] -Name <String> [-Description <String>]
 [-BootImagePackageId <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMTaskSequence** cmdlet creates a task sequence.
A task sequence performs multiple steps or tasks on a Configuration Manager client computer without user intervention.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a custom task sequence

```powershell
PS XYZ:\> New-CMTaskSequence -CustomTaskSequence -Name "TaskSequence01"
```

This command creates a task sequence with the name TaskSequence01.

### Example 2: Create a task sequence to install an operating system image

```powershell
PS XYZ:\> New-CMTaskSequence -InstallOperatingSystemImage -Name "TaskSequence02" -BootImagePackageId SC100002 -OperatingSystemImagePackageId SC10000D -OperatingSystemImageIndex 1 -JoinDomain WorkgroupType -WorkgroupName "WorkGroup01" -ApplyAll $True -Description "Task sequence description"
```

This command creates a task sequence named TaskSequence02 that installs an operating system image and joins a workgroup.

### Example 3: Create a task sequence to build an operating system and join a workgroup

```powershell
PS XYZ:\> New-CMTaskSequence -BuildOperatingSystemImage -Name "TaskSequence03" -BootImagePackageId SC100002 -OperatingSystemImagePackageId SC10000D -OperatingSystemImageIndex 1 -JoinDomain WorkgroupType -WorkgroupName "WorkGroup01" -OperatingSystemFilePath "\\Server1\image\OSImage.wim" -OperatingSystemFileAccount "domain\account"
```

This command creates a task sequence named TaskSequence03 that builds an operating system using the supplied location and account, and joins a workgroup.

### Example 4: Create a task sequence to install an operating system to a virtual hard disk

```powershell
PS XYZ:\> New-CMTaskSequence -InstallOperatingSystemImageVhd -Name "TaskSequence04" -BootImagePackageId SC100002 -OperatingSystemImagePackageId SC10000D -OperatingSystemImageIndex 1 -JoinDomain WorkgroupType -WorkgroupName "WorkGroup01"
```

This command creates a task sequence named TaskSequence04 that installs an operating system to a vhd and joins a workgroup.

### Example 5: Create a task sequence to upgrade an operating system

```powershell
PS XYZ:\> New-CMTaskSequence -UpgradeOperatingSystem -Name "TaskSequence05" -UpgradePackageId SC102EBA
```

This command creates the task sequence named TaskSequence05 and specifies that the task sequence will upgrade the operating system using the upgrade package with the ID SC102EBA.

## PARAMETERS

### -ApplicationName

Specifies an array of names for applications.

```yaml
Type: String[]
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, UpgradeOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplyAll

Indicates whether to apply all of the images.

```yaml
Type: Boolean
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases: ApplyAllImages

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImagePackageId

Specifies the ID of a boot image package.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NewCustom
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BuildOperatingSystemImage

Indicates that the task sequence builds and captures a reference operating system image from a set of operating system installation files.

```yaml
Type: SwitchParameter
Parameter Sets: NewBuildOSImage
Aliases: BuildOperatingSystemImageOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureLocallyUsingLink

Indicates whether Configuration Manager stores captured data locally on the destination computer.

The links that Configuration Manager uses to store the user state locally are referred to as hard-links.
Added in User State Migration Tool (USMT) 4.0, hard-links  is a USMT feature that scans the computer for user files and settings and then creates a directory of hard-links to those files.
The hard-links are then used to restore user data after the new operating system is deployed.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases: CaptureLocallyUsingLinks

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureNetworkSetting

Indicates whether the task sequence captures network settings from the computer that runs the task sequence.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureUserSetting

Indicates whether the task sequence captures the user state.
If you specify this parameter, also specify the *UserStateMigrationToolPackageId* parameter.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CaptureWindowsSetting

Indicates whether the task sequence captures Windows settings from the computer that runs the task sequence.
You can capture the computer name, registered user and organization name, and the time zone settings.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClientPackagePackageId

Specifies the ID of the client package to install on the destination computer.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigureBitLocker

Indicates whether the task sequence enables BitLocker encryption on the hard drive.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage, NewInstallOSImageVhd
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

### -CreatedBy

Specifies the name of the user that created the operating system image that the task sequence captures.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomTaskSequence

Indicates that the cmdlet creates a custom task sequence.

```yaml
Type: SwitchParameter
Parameter Sets: NewCustom
Aliases: CustomOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description for the task sequence.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, NewCustom
Aliases: TaskSequenceDescription

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

### -DomainAccount

Specifies an account, in the format Domain\User, that has the necessary permissions to join the computer to the domain.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainName

Specifies a domain name.
Include this parameter to have the target computer join the specified domain.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainOrganizationUnit

Specifies the Lightweight Directory Access Protocol (LDAP) path for an organizational unit (OU) for the computer to join.
Use the following format: LDAP//OU=computers, DC=Contoso.com, C=com.
Specify an OU in the domain that you specified in the *DomainName* parameter.

If the computer is already a member of some other OU, Active Directory Domain Services (AD DS) does not allow you to change the OU and this setting is ignored.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword

Specifies, as a secure string, the password for the user account that you specified for the *DomainAccount* parameter.

```yaml
Type: SecureString
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
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

### -GeneratePassword

Indicates whether Configuration Manager randomly generates a password for the local administrator account in the new operating system.

```yaml
Type: Boolean
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HighPerformance
Starting in version 1910, use this parameter to set the following option on the **Performance** page of the task sequence properties: **Run as high performance power plan**.

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

### -IgnoreInvalidApplication

Indicates whether the task sequence step continues if an individual application installation encounters a recoverable failure.

If you specify this parameter, the task sequence continues regardless of any installation errors.
If you do not specify this parameter, the task sequence step ends immediately when an installation fails.

```yaml
Type: Boolean
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, UpgradeOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageDescription

Specifies a description of the operating system image that the task sequence captures.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageVersion

Specifies the user-defined version of the operating system that the task sequence captures.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallOperatingSystemImage

Indicates that the task sequence installs an operating system image.

```yaml
Type: SwitchParameter
Parameter Sets: NewInstallOSImage
Aliases: InstallOperatingSystemImageOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallOperatingSystemImageVhd

Indicates that the task sequence installs an existing operating system image to a virtual hard disk.

```yaml
Type: SwitchParameter
Parameter Sets: NewInstallOSImageVhd
Aliases: InstallOperatingSystemImageVhdOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationLicensingMode

Specifies the Windows Server license mode that the task sequence uses.
Valid values are:

- NonSpecify
- PerSeat
- PerServer

```yaml
Type: ServerLicensingMode
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:
Accepted values: NonSpecify, PerSeat, PerServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstallationProperty

Specifies Configuration Manager client installation properties.

Site assignment and the default configuration are automatically specified by the task sequence action.
You can use this parameter to specify any additional installation properties to use when you install the client.
To enter multiple installation properties, separate them with a space.
If a property contains spaces, surround it by quotation marks ("").

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JoinDomain

Specifies the destination computer to add to a workgroup or domain.
Valid values are:

- DomainType
- WorkgroupType

```yaml
Type: JoinType
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:
Accepted values: DomainType, WorkgroupType

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalAdminPassword

Specifies, as a secure string, the local administrator password for the destination computer.

```yaml
Type: SecureString
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaximumServerConnection

Specifies the maximum number of server connections.
Specify this parameter if you use the PerServer value for the *InstallationLicensingMode* parameter.

```yaml
Type: Int32
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies a name for the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskSequenceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemFileAccount

Specifies the Windows account that has permissions to the network share that you specify in the *OperatingSystemFilePath* parameter.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases: CaptureOperatingSystemFileAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemFileAccountPassword

Specifies as a secure string the password for the account that you specify in the *OperatingSystemFileAccount* parameter.

```yaml
Type: SecureString
Parameter Sets: NewBuildOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemFilePath

Specifies the file system path to the location that Configuration Manager uses when it stores the captured operating system image.

```yaml
Type: String
Parameter Sets: NewBuildOSImage
Aliases: CaptureOperatingSystemFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageIndex

Specifies the index of the operating system image to install.
Use this parameter if the operating system image package has multiple images.

```yaml
Type: UInt32
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImagePackageId

Specifies the ID of the package that contains the operating system image to install.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionAndFormatTarget

Indicates whether the task sequence partitions and formats the destination computer before the operating system is installed.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductKey

Specifies the Windows product key for the operating system installation.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd, UpgradeOSImage
Aliases: InstallationProductKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SaveLocally

This parameter has been deprecated.

```yaml
Type: Boolean
Parameter Sets: NewInstallOSImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateStyle

Specifies whether the task sequence installs all updates or only mandatory updates for the destination computers that receive the task sequence.
Valid values are:

- All
- Mandatory
- NoInstall

```yaml
Type: SoftwareUpdateStyleType
Parameter Sets: NewBuildOSImage, NewInstallOSImage, UpgradeOSImage
Aliases:
Accepted values: All, Mandatory, NoInstall

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeZone

Specifies time zone info.

```yaml
Type: TimeZoneInfo
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradeOperatingSystem

Indicates that the task sequence upgrades the operating system from an upgrade package.

```yaml
Type: SwitchParameter
Parameter Sets: UpgradeOSImage
Aliases: UpgradeOperatingSystemOption

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpgradePackageId

Specifies the ID for an upgrade package.

```yaml
Type: String
Parameter Sets: UpgradeOSImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserStateMigrationToolPackageId

Specifies the ID of the USMT package.

To store the user state data locally or on a state migration point, you must create a package that contains the USMT source files that you want to use.

```yaml
Type: String
Parameter Sets: NewInstallOSImage
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

### -WorkgroupName

Specifies the name of a workgroup.
Specify this parameter if you use the WorkgroupType value for the *JoinDomain* parameter.

```yaml
Type: String
Parameter Sets: NewBuildOSImage, NewInstallOSImage, NewInstallOSImageVhd
Aliases:

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

### IResultObject#SMS_TaskSequencePackage

## NOTES

## RELATED LINKS

[Get-CMTaskSequence](Get-CMTaskSequence.md)
[Set-CMTaskSequence](Set-CMTaskSequence.md)
[Copy-CMTaskSequence](Copy-CMTaskSequence.md)
[Import-CMTaskSequence](Import-CMTaskSequence.md)
[Export-CMTaskSequence](Export-CMTaskSequence.md)
[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
[New-CMTaskSequenceMedia](New-CMTaskSequenceMedia.md)
