---
description: Creates stand-alone media.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMStandaloneMedia
---

# New-CMStandaloneMedia

## SYNOPSIS
Creates stand-alone media.

## SYNTAX

```
New-CMStandaloneMedia [-Application <IResultObject[]>] [-DriverPackage <IResultObject[]>]
 [-IncludeApplicationDependency] [-MediaExpirationDate <DateTime>] [-MediaSize <MediaSize>]
 [-MediaStartDate <DateTime>] [-Package <IResultObject[]>] -TaskSequence <IResultObject> [-AllowUacPrompt]
 [-AllowUnattended] [-CertificatePath <String>] -DistributionPoint <IResultObject[]> [-Force] [-FormatMedia]
 [-SiteCode <String>] [-MediaPassword <SecureString>] -MediaType <MediaInputType> [-NoAutoRun] -Path <String>
 [-PrestartCommand <String>] [-PrestartPackage <IResultObject>] [-TemporaryFolder <String>]
 [-Variable <Hashtable>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMStandaloneMedia** cmdlet creates media used to deploy operating systems without network access.

NOTE: This cmdlet requires elevated permissions to run.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create stand-alone media using variables
```
PS XYZ:\> $TaskSequence = Get-CMTaskSequence -Name "TaskSequence01"
PS XYZ:\> $DistributionPoint = Get-CMDistributionpoint -SiteCode CM1
PS XYZ:\> New-CMStandaloneMedia -MediaType CdDvd -Path \\server\share\standaloneMedia.iso -TaskSequence $TaskSequence -DistributionPoint $DistributionPoint
```

The first command gets the task sequence object named TaskSequence01 and stores the object in the $TaskSequence variable.

The second command gets the distribution point object for the site code named CM1 and stores the object in the $DistributionPoint variable.

The last command creates stand-alone media using the task sequence stored in $TaskSequence and the distribution point stored in $DistributionPoint.

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

### -IncludeApplicationDependency
Indicates that the cmdlet detects associated application dependencies and adds them to this media.

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

### -MediaExpirationDate
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: Expiration

Required: False
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

### -MediaSize
Specifies the size of the media.
Valid values are:

- None
- Size4GB
- Size8GB
- Size650MB
- SizeUnlimited

```yaml
Type: MediaSize
Parameter Sets: (All)
Aliases:
Accepted values: None, Size650MB, Size4GB, Size8GB, SizeUnlimited

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaStartDate
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: Start

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

### -NoAutoRun
Starting in version 1906, use this parameter to configure the following option from the create task sequence media wizard: **Include autorun.inf file on media**


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

### -SiteCode
{{ Fill SiteCode Description }}

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

### -TaskSequence
Specifies a task sequence object.
To obtain a task sequence object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMDistributionPoint](Get-CMDistributionPoint.md)

[Get-CMPackage](Get-CMPackage.md)

[Get-CMTaskSequence](Get-CMTaskSequence.md)


