---
author: aczechowski
description: Creates a prestage media.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMPrestageMedia
titleSuffix: Configuration Manager
---

# New-CMPrestageMedia

## SYNOPSIS
Creates a prestage media.

## SYNTAX

```
New-CMPrestageMedia [-Application <IResultObject[]>] [-Comment <String>] [-CreatedBy <String>]
 [-DriverPackage <IResultObject[]>] -OperatingSystemImage <IResultObject> [-OperatingSystemImageIndex <Int32>]
 [-Package <IResultObject[]>] [-Version <String>] [-IncludeApplicationDependency] -TaskSequence <IResultObject>
 [-AllowUacPrompt] [-AllowUnattended] [-AllowUnknownMachine] -BootImage <IResultObject>
 [-CertificateExpireTime <DateTime>] [-CertificatePassword <SecureString>] [-CertificatePath <String>]
 [-CertificateStartTime <DateTime>] -DistributionPoint <IResultObject[]> [-Force]
 -ManagementPoint <IResultObject[]> -MediaMode <MediaMode> [-MediaPassword <SecureString>] -Path <String>
 [-TemporaryFolder <String>] [-PrestartCommand <String>] [-PrestartPackage <IResultObject>]
 [-UserDeviceAffinity <UserDeviceAffinityType>] [-Variable <Hashtable>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMPrestagedMedia** cmdlet creates a file to prestage on a new hard drive that includes an operating system image.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\> $ManagementPoint = Get-CMManagementPoint -SiteSystemServerName "dist01.contoso.com" -SiteCode "CM1"
PS XYZ:\> $BootImage = Get-CMBootImage -Name "BootImage01"
PS XYZ:\> $DistributionPoint = Get-CMDistributionPoint -SiteSystemServerName "dist01.contoso.com" -SiteCode "CM1"
PS XYZ:\> $OSImage = Get-CMOperatingSystemImage -Name "OSImagePkg01"
PS XYZ:\> New-CMPrestagedMedia -MediaMode Dynamic -Path "\\server\share\PrestargedMedia.wim" -BootImage $BootImage -DistributionPoint $DistributionPoint -ManagementPoint $ManagementPoint -OperatingSystemImage $OSImage
```

The first command gets the management point object for the site system server named dist01.contoso.com with the site code CM1 and stores the object in the $ManagementPoint variable.

The second command gets the boot image object named BootImage01 and stores the object in the $BootImage variable.

The third command gets the Distribution point object for the site system server named dist01.contoso.com with the site code CM1 and stores the object in the $DistributionPoint variable.

The fourth command gets the operating system image object named OSImagePkg01 and stores the object inthe $OSImage variable.

The last command creates a dynamic prestaged media file named PrestargedMedia.wim with the boot image stored in $BootImage, the distribution point stored in $DistributionPoint, the management point stored in $ManagementPoint, and the operating system image stored in $OSImage.

## PARAMETERS

### -AllowUacPrompt
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreatedBy
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

### -DistributionPoint
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

### -IncludeApplicationDependency
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: IncludeApplicationDependencies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagementPoint
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

### -MediaPassword
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

### -OperatingSystemImage
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

### -TaskSequence
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TemporaryFolder
{{ Fill TemporaryFolder Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: TemporaryDirectory, StagingArea

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDeviceAffinity
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMApplication](Get-CMApplication.md)

[Get-CMBootImage](Get-CMBootImage.md)

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Get-CMOperatingSystemImage](Get-CMOperatingSystemImage.md)

[Get-CMPackage](Get-CMPackage.md)
