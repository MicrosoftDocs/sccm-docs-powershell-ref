---
description: Create a new program for a package.
external help file: AdminUI.PS.AppModel.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/20/2020
schema: 2.0.0
title: New-CMProgram
---

# New-CMProgram

## SYNOPSIS

Create a new program for a package.

## SYNTAX

### NewStandardProgram (Default)
```
New-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] -CommandLine <String>
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>] [-DriveLetter <String>]
 [-DriveMode <DriveModeType>] [-Duration <Int32>] -PackageName <String> [-ProgramRunType <ProgramRunType>]
 [-Reconnect <Boolean>] [-RunMode <RunModeType>] [-RunType <RunType>] -StandardProgramName <String>
 [-UserInteraction <Boolean>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewStandardProgramById
```
New-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] -CommandLine <String>
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>] [-DriveLetter <String>]
 [-DriveMode <DriveModeType>] [-Duration <Int32>] -PackageId <String> [-ProgramRunType <ProgramRunType>]
 [-Reconnect <Boolean>] [-RunMode <RunModeType>] [-RunType <RunType>] -StandardProgramName <String>
 [-UserInteraction <Boolean>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewDeviceProgram
```
New-CMProgram -CommandLine <String> [-CommandLineFolder <String>] [-Comment <String>]
 -DeviceProgramName <String> [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -PackageName <String> [-Requirement <String>]
 [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### NewDeviceProgramById
```
New-CMProgram -CommandLine <String> [-CommandLineFolder <String>] [-Comment <String>]
 -DeviceProgramName <String> [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -PackageId <String> [-Requirement <String>]
 [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

The **New-CMProgram** cmdlet creates a program in Configuration Manager.
Programs are commands that are associated with a Configuration Manager package.
Programs identify the actions that occur when the client receives the client package.
You can associate multiple programs with the same package.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a standard program

This command creates a standard program in Configuration Manager.

```powershell
New-CMProgram -PackageName "test" -StandardProgramName SPM -CommandLine "RunMe" -WorkingDirectory "C:\temp" -RunType Hidden -ProgramRunType OnlyWhenNoUserIsLoggedOn -DiskSpaceRequirement 100 -DiskSpaceUnit GB -Duration 100 -DriveMode RunWithUnc
```

### Example 2: Create a device program

This command creates a device program in Configuration Manager.

```powershell
New-CMProgram -PackageName "Contoso-12" -DeviceProgramName DPM -Comment "Upgrades for December" -WorkingDirectory "C:\temp" -CommandLine "RunMe" -CommandLineFolder "C:\Windows\" -DiskSpaceRequirement 10 -DiskSpaceUnit GB -DownloadProgramType OnlyWhenTheDeviceIsDocked -Requirement "All previous updates"
```

## PARAMETERS

### -AddSupportedOperatingSystemPlatform

Specify one or more supported OS platforms to add for the program. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases: AddSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandLine

Specify the command line for the program.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandLineFolder

Specify the folder that contains the executable program. This folder can be an absolute path on the client, or a path relative to the distribution folder that contains the package.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment

Specify optional text about the program, such as a description. On client computers, this text displays with the program in Software Center.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
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

### -DeviceProgramName

Specifies a device program name.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases:

Required: True
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

### -DiskSpaceRequirement

Specify the amount of disk space that the software program requires to run on the computer. The value must be greater than or equal to zero. If you specify a value, use the **DiskSpaceUnit** parameter to specify units for the value.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DiskSpaceReq

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSpaceUnit

Specify an accepted unit for the **DiskSpaceRequirement** parameter.

```yaml
Type: DiskSpaceUnitType
Parameter Sets: (All)
Aliases:
Accepted values: KB, MB, GB

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DownloadProgramType

Specify when the program is to run.

```yaml
Type: DownloadProgramType
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases:
Accepted values: AsSoonAsPossible, OnlyOverFastNetwork, OnlyWhenTheDeviceIsDocked

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveLetter

If you use the **DriveMode** parameter, specify a drive letter for the location.

```yaml
Type: String
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveMode

Indicates whether the program requires a specific drive letter, specified in the **DriveLetter** parameter.

- `RunWithUnc`: Run the program from the UNC path. This value is the default. Starting in version 2010, this value was renamed from `RenameWithUnc`.

- `RequiresDriveLetter`: The program uses any available drive letter.

- `RequiresSpecificDriveLetter`: The program only runs if the drive isn't already in use.

```yaml
Type: DriveModeType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: RunWithUnc, RequiresDriveLetter, RequiresSpecificDriveLetter

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Duration

Specifies the maximum amount of time that you expect the program to run. The default value is 120 minutes.

```yaml
Type: Int32
Parameter Sets: NewStandardProgram, NewStandardProgramById
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

### -PackageId

Specify the ID of the package for this program.

```yaml
Type: String
Parameter Sets: NewStandardProgramById, NewDeviceProgramById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName

Specify a package name for this program.

```yaml
Type: String
Parameter Sets: NewStandardProgram, NewDeviceProgram
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramRunType

Specifies the logon conditions that are necessary for the program to run.

The default setting is `OnlyWhenUserIsLoggedOn`.

```yaml
Type: ProgramRunType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: OnlyWhenUserIsLoggedOn, WhetherOrNotUserIsLoggedOn, OnlyWhenNoUserIsLoggedOn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reconnect

Indicates whether the client computer reconnects to the distribution point when the user signs in to Windows.

```yaml
Type: Boolean
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Requirement

Specifies additional requirements for standard or device programs.

```yaml
Type: String
Parameter Sets: NewDeviceProgram, NewDeviceProgramById
Aliases: Requirements

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunMode

Specify the credentials that the program requires to run on the client computer.

```yaml
Type: RunModeType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: RunWithUserRights, RunWithAdministrativeRights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunType

Specify the mode in which the program runs on the client computer.

The default value is `Normal`.

```yaml
Type: RunType
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:
Accepted values: Normal, Minimized, Maximized, Hidden

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardProgramName

Specify the standard program name.

```yaml
Type: String
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserInteraction

Indicates whether to allow users to interact with the program.

```yaml
Type: Boolean
Parameter Sets: NewStandardProgram, NewStandardProgramById
Aliases:

Required: False
Position: Named
Default value: None
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

### -WorkingDirectory

Specify a working directory for the program.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_Program

For more information on this return object and its properties, see [SMS_Program server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_program-server-wmi-class).

## NOTES

## RELATED LINKS

[Disable-CMProgram](Disable-CMProgram.md)

[Enable-CMProgram](Enable-CMProgram.md)

[Get-CMProgram](Get-CMProgram.md)

[Remove-CMProgram](Remove-CMProgram.md)

[Set-CMProgram](Set-CMProgram.md)
