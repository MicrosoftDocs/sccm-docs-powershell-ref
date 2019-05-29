---
title: New-CMPrestagedMedia
titleSuffix: Configuration Manager
description: Creates prestaged media.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMPrestagedMedia

## SYNOPSIS
Creates prestaged media.

## SYNTAX

```
New-CMPrestagedMedia [-Application <IResultObject[]>] [-Comment <String>] [-CreatedBy <String>]
 [-DriverPackage <IResultObject[]>] -OperatingSystemImage <IResultObject> [-OperatingSystemImageIndex <Int32>]
 [-Package <IResultObject[]>] [-Version <String>] [-AllowUacPrompt] [-AllowUnattended] [-AllowUnknownMachine]
 -BootImage <IResultObject> [-CertificateExpireTime <DateTime>] [-CertificatePassword <SecureString>]
 [-CertificatePath <String>] [-CertificateStartTime <DateTime>] -DistributionPoint <IResultObject[]> [-Force]
 -ManagementPoint <IResultObject[]> -MediaMode <MediaMode> -Path <String> [-PrestartCommand <String>]
 [-PrestartPackage <IResultObject>] [-UserDeviceAffinity <UserDeviceAffinityType>] [-Variable <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMPrestagedMedia** cmdlet creates a file to prestage on a new hard drive that includes an operating system image.

## EXAMPLES

### Example 1: Create prestaged media
```
PS C:\> $ManagementPoint = Get-CMManagementPoint -SiteSystemServerName "dist01.contoso.com" -SiteCode "CM1"
PS C:\> $BootImage = Get-CMBootImage -Name "BootImage01"
PS C:\> $DistributionPoint = Get-CMDistributionPoint -SiteSystemServerName "dist01.contoso.com" -SiteCode "CM1"
PS C:\> $OSImage = Get-CMOperatingSystemImage -Name "OSImagePkg01"
PS C:\> New-CMPrestagedMedia -MediaMode Dynamic -Path "\\server\share\PrestargedMedia.wim" -BootImage $BootImage -DistributionPoint $DistributionPoint -ManagementPoint $ManagementPoint -OperatingSystemImage $OSImage
```

The first command gets the management point object for the site system server named dist01.contoso.com with the site code CM1 and stores the object in the $ManagementPoint variable.

The second command gets the boot image object named BootImage01 and stores the object in the $BootImage variable.

The third command gets the Distribution point object for the site system server named dist01.contoso.com with the site code CM1 and stores the object in the $DistributionPoint variable.

The fourth command gets the operating system image object named OSImagePkg01 and stores the object inthe $OSImage variable.

The last command creates a dynamic prestaged media file named PrestargedMedia.wim with the boot image stored in $BootImage, the distribution point stored in $DistributionPoint, the management point stored in $ManagementPoint, and the operating system image stored in $OSImage.

## PARAMETERS

### -AllowUacPrompt
Indicates that the user access control (UAC) prompt is allowed.

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

### -AllowUnattended
Indicates that unattended operating system deployment is allowed.
An unattended operating system deployment does not prompt for network configuration or optional task sequences.

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

### -AllowUnknownMachine
Indicates that provisioning of unknown computers is allowed.

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

### -Application
Specifies an array of application objects.
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Applications
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImage
Specifies the boot image object associated with the task sequence media.
To obtain a boot image object, use the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: BootImagePackage
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateExpireTime
Specifies the expiration date of the self-signed media certificate.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePassword
Specifies, as a secure string, the password to import a certificate. 
A PKI-issued certificate is added to the boot media for client authentication and communication with a Configuration Manager site.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificatePath
Specifies the path to a PKI certificate.

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

### -CertificateStartTime
Specifies a start date for the self-signed media certificate.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies a comment for a prestaged media file.

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

### -CreatedBy
Specifies the name of an individual or organization responsible for the creation of the prestaged media.

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
Indicates that wildcard handling is disabled.

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

### -DistributionPoint
Specifies a distribution point object.
To obtain a distribution point object, use the [Get-CMDistributionPoint](Get-CMDistributionPoint.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DistributionPoints
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackage
Specifies an array of driver package objects.
To obtain driver package object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: DriverPackages, PackageDriver, PackageDrivers
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
Indicates that wildcard handling is enabled.

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

### -ManagementPoint
Specifies an array of management point objects.
To obtain a management point object, use the [Get-CMManagementPoint](Get-CMManagementPoint.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: ManagementPoints
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaMode
Specifies a media mode.
The media mode specifies how the client finds a management point to obtain deployment information.
Valid values are: 

- Dynamic.
The media contacts a management point that redirects the client to a different management point based on the client location in the site boundaries. 
- SiteBased.
The media contacts the specified management point.

```yaml
Type: MediaMode
Parameter Sets: (All)
Aliases: 
Accepted values: Dynamic, SiteBased
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImage
Specifies an operating system image object.
To obtain an operating system image object, use the [Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: OperatingSystemImagePackage
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OperatingSystemImageIndex
Specifies the operating system image index.

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

### -Package
Specifies an array of package objects.
To obtain a package object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Packages
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the path to the media file (.wim).

```yaml
Type: String
Parameter Sets: (All)
Aliases: MediaPath, OutputPath, DriveName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestartCommand
Specifies a prestart command.
A prestart command is a script or executable that runs before the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PreExecCommandLine
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrestartPackage
Specifies the package object that includes files for the prestart command.
To obtain a package object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

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

### -UserDeviceAffinity
Specifies user device affinity.
User device affinity associates users with a destination computer.
Valid values are: 

- AdministratorApproval
- AutoApproval
- DoNotAllow

```yaml
Type: UserDeviceAffinityType
Parameter Sets: (All)
Aliases: 
Accepted values: DoNotAllow, AdministratorApproval, AutoApproval
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable
Specifies a task sequence variable.
The task sequence variable consists of a name and a value.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: TaskSequenceVariables, Variables
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies the version information for the media.

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

[Get-CMApplication](Get-CMApplication.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMPackage](Get-CMPackage.md)


