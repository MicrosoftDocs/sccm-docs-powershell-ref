<<<<<<< HEAD
---
title: New-CMBootableMedia
titleSuffix: Configuration Manager
description: Creates bootable media.
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
=======
﻿---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: 111C231D-453E-481C-A43D-2109531917A9
online version: https://go.microsoft.com/fwlink/?linkid=834270
schema: 2.0.0
>>>>>>> master
---

# New-CMBootableMedia

## SYNOPSIS
Creates bootable media.

## SYNTAX

```
New-CMBootableMedia [-AllowUacPrompt] [-AllowUnattended] [-AllowUnknownMachine] -BootImage <IResultObject>
 [-CertificateExpireTime <DateTime>] [-CertificatePassword <SecureString>] [-CertificatePath <String>]
 [-CertificateStartTime <DateTime>] -DistributionPoint <IResultObject[]> [-Force] [-FormatMedia]
 -ManagementPoint <IResultObject[]> -MediaMode <MediaMode> [-MediaPassword <SecureString>]
 -MediaType <MediaInputType> -Path <String> [-PrestartCommand <String>] [-PrestartPackage <IResultObject>]
 [-ProviderCredential <PSCredential>] [-UserDeviceAffinity <UserDeviceAffinityType>] [-Variable <Hashtable>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMBootableMedia** cmdlet creates media used to deploy operating systems using the Configuration Manager infrastructure.
Bootable media deploys an operating system when the destination computer starts.

NOTE: This cmdlet requires elevated permissions to run.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Create bootable media
```
PS XYZ:\> $BootImage = Get-CMBootImage -Name "Boot image (x64)"
PS XYZ:\> $DistributionPoint = Get-CMDistributionpoint -SiteCode CM1
PS XYZ:\> $ManagementPoint = Get-CMManagementPoint -SiteSystemServerName "SiteSystemServer02.Contoso.com"
PS XYZ:\> New-CMBootableMedia -MediaMode Dynamic -MediaType CdDvd -Path "\\Server\share\test.iso" -AllowUnknownMachine -BootImage $BootImage -DistributionPoint $DistributionPoint -ManagementPoint $ManagementPoint
```

The first command gets the boot image object named Boot image (x64) and stores the object in the $BootImage variable.

The second command gets the distribution point object for the system site server named SiteServer01.Contoso.com and stores the object in the $DistributionPoint variable.

The third command gets the management point object for the site system server named SiteServer02.Contoso.com and stores the object in the $ManagementPoint variable.

The last command creates bootable media in dynamic mode using the BootImage stored in $BootImage, the distribution point stored in $DistributionPoint, and the management point stored in $ManagementPoint.

## PARAMETERS

### -AllowUacPrompt
Indicates that User Account Control (UAC) prompts are allowed.

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
Indicates that unattended operating system deployments are allowed.
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
Indicates that Configuration Manager is allowed to provision unknown computers.

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

### -BootImage
Specifies a boot image object.
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
Specifies an expiration date and time for a self-signed media certificate.

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
Specifies, as a secure string, the password for a PKI certificate.
You need to import a PKI certificate for HTTPS communication.

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
Specifies a path from which to import a PKI certificate.

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
Specifies a start date and time for a self-signed media certificate.

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
Specifies an array of distribution point objects.
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

### -FormatMedia
Indicates that the cmdlet formats the removable USB drive (FAT32), and makes it bootable.

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
Specifies the media mode.
Valid values are: 

- Dynamic
- SiteBased

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
Specifies, as a secure string, a password to protect task sequence media.

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

### -MediaType
Specifies the media type.
Valid values are: 

- CdDvd
- Usb
- Hd

```yaml
Type: MediaInputType
Parameter Sets: (All)
Aliases: 
Accepted values: Usb, CdDvd

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the name and path where the output files are written.

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
Specifies a prestart command that will run before the task sequence runs.
A prestart command is a script or an executable that can interact with the user in Windows PE before the task sequence runs to install the operating system.

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
Specifies a package object that contains files for the prestart command.
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

### -ProviderCredential
 

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDeviceAffinity
Specifies how users are associated with their devices.
Valid values are: 

- DoNotAllow
- AdministratorApproval
- AutoApproval

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
A task sequence variable is a name/value pair that is used during the task sequence deployment.

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

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMManagementPoint](Get-CMManagementPoint.md)

[Get-CMPackage](Get-CMPackage.md)


