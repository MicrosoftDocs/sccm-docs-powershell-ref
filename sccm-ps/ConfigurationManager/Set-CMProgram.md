---
author: aczechowski
description: Modifies a program in Configuration Manager.
external help file: AdminUI.PS.AppModel.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMProgram
titleSuffix: Configuration Manager
---

# Set-CMProgram

## SYNOPSIS
Modifies a program in Configuration Manager.

## SYNTAX

### SetStandardProgramByProgramValue (Default)
```
Set-CMProgram -InputObject <IResultObject> [-StandardProgram] [-Comment <String>] [-CommandLine <String>]
 [-WorkingDirectory <String>] [-RunType <RunType>] [-AfterRunningType <AfterRunningType>] [-Category <String>]
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>] [-Duration <Int32>]
 [-Requirement <String>] [-ProgramRunType <ProgramRunType>] [-RunMode <RunModeType>]
 [-UserInteraction <Boolean>] [-DriveMode <DriveModeType>] [-DriveLetter <String>] [-Reconnect <Boolean>]
 [-ProgramAssignedType <ProgramAssignedType>] [-SuppressProgramNotification <Boolean>]
 [-DisableProgram <Boolean>] [-EnableTaskSequence <Boolean>] [-DisableMomAlertOnRun <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] [-AddSupportedOperatingSystemPlatform <IResultObject[]>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-RunOnAnyPlatform] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramByName
```
Set-CMProgram -PackageName <String> [-StandardProgram] -ProgramName <String> [-Comment <String>]
 [-CommandLine <String>] [-WorkingDirectory <String>] [-RunType <RunType>]
 [-AfterRunningType <AfterRunningType>] [-Category <String>] [-DiskSpaceRequirement <String>]
 [-DiskSpaceUnit <DiskSpaceUnitType>] [-Duration <Int32>] [-Requirement <String>]
 [-ProgramRunType <ProgramRunType>] [-RunMode <RunModeType>] [-UserInteraction <Boolean>]
 [-DriveMode <DriveModeType>] [-DriveLetter <String>] [-Reconnect <Boolean>]
 [-ProgramAssignedType <ProgramAssignedType>] [-SuppressProgramNotification <Boolean>]
 [-DisableProgram <Boolean>] [-EnableTaskSequence <Boolean>] [-DisableMomAlertOnRun <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] [-AddSupportedOperatingSystemPlatform <IResultObject[]>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-RunOnAnyPlatform] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramByName
```
Set-CMProgram -PackageName <String> [-DeviceProgram] -ProgramName <String> [-Comment <String>]
 [-CommandLine <String>] [-WorkingDirectory <String>] [-DiskSpaceRequirement <String>]
 [-DiskSpaceUnit <DiskSpaceUnitType>] [-Requirement <String>] [-CommandLineFolder <String>]
 [-DownloadProgramType <DownloadProgramType>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramById
```
Set-CMProgram -PackageId <String> [-StandardProgram] -ProgramName <String> [-Comment <String>]
 [-CommandLine <String>] [-WorkingDirectory <String>] [-RunType <RunType>]
 [-AfterRunningType <AfterRunningType>] [-Category <String>] [-DiskSpaceRequirement <String>]
 [-DiskSpaceUnit <DiskSpaceUnitType>] [-Duration <Int32>] [-Requirement <String>]
 [-ProgramRunType <ProgramRunType>] [-RunMode <RunModeType>] [-UserInteraction <Boolean>]
 [-DriveMode <DriveModeType>] [-DriveLetter <String>] [-Reconnect <Boolean>]
 [-ProgramAssignedType <ProgramAssignedType>] [-SuppressProgramNotification <Boolean>]
 [-DisableProgram <Boolean>] [-EnableTaskSequence <Boolean>] [-DisableMomAlertOnRun <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] [-AddSupportedOperatingSystemPlatform <IResultObject[]>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-RunOnAnyPlatform] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramById
```
Set-CMProgram -PackageId <String> [-DeviceProgram] -ProgramName <String> [-Comment <String>]
 [-CommandLine <String>] [-WorkingDirectory <String>] [-DiskSpaceRequirement <String>]
 [-DiskSpaceUnit <DiskSpaceUnitType>] [-Requirement <String>] [-CommandLineFolder <String>]
 [-DownloadProgramType <DownloadProgramType>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramByValue
```
Set-CMProgram -InputObject <IResultObject> [-StandardProgram] -ProgramName <String> [-Comment <String>]
 [-CommandLine <String>] [-WorkingDirectory <String>] [-RunType <RunType>]
 [-AfterRunningType <AfterRunningType>] [-Category <String>] [-DiskSpaceRequirement <String>]
 [-DiskSpaceUnit <DiskSpaceUnitType>] [-Duration <Int32>] [-Requirement <String>]
 [-ProgramRunType <ProgramRunType>] [-RunMode <RunModeType>] [-UserInteraction <Boolean>]
 [-DriveMode <DriveModeType>] [-DriveLetter <String>] [-Reconnect <Boolean>]
 [-ProgramAssignedType <ProgramAssignedType>] [-SuppressProgramNotification <Boolean>]
 [-DisableProgram <Boolean>] [-EnableTaskSequence <Boolean>] [-DisableMomAlertOnRun <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] [-AddSupportedOperatingSystemPlatform <IResultObject[]>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-RunOnAnyPlatform] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramByValue
```
Set-CMProgram -InputObject <IResultObject> [-DeviceProgram] -ProgramName <String> [-Comment <String>]
 [-CommandLine <String>] [-WorkingDirectory <String>] [-DiskSpaceRequirement <String>]
 [-DiskSpaceUnit <DiskSpaceUnitType>] [-Requirement <String>] [-CommandLineFolder <String>]
 [-DownloadProgramType <DownloadProgramType>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramByProgramValue
```
Set-CMProgram -InputObject <IResultObject> [-DeviceProgram] [-Comment <String>] [-CommandLine <String>]
 [-WorkingDirectory <String>] [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-Requirement <String>] [-CommandLineFolder <String>] [-DownloadProgramType <DownloadProgramType>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMProgram** cmdlet modifies a program in Microsoft System Center Configuration Manager.
Programs are commands that are associated with a System Center Configuration Manager package.
Programs identify the actions that occur when the client receives the client package.
You can associate multiple programs with the same package.

## EXAMPLES

### Example 1: Modify a standard program
```
PS XYZ:\> Set-CMProgram -Name "Test" -StandardProgramName SPM -Comment "Standard Upgrades" -CommandLine "RunThisNow" -RunType Maximized -AfterRunningType ProgramControlsRestart -Category "Laptops" -DiskSpaceRequirement 50 -DiskSpaceUnit MB -Duration 150 -Requirement 4 -Reconnect $False -SuppressProgramNotifications $False -DisableProgram $True -EnableTaskSequence $True -DisableMomAlertOnRun $True -GenerateMomAlertOnFail $True
```

This command modifies a standard program.

### Example 2: Modify a device program
```
PS XYZ:\> Set-CMProgram -Name "Test" -DeviceProgramName DPM -Comment "Upgrades for December" -CommandLine "RunMe" -WorkingDirectory "\TempWork" -CommandLineFolder "C:\Windows" -DiskSpaceRequirement 30 -DiskSpaceUnit MB -DownloadProgramType AsSoonAsPossible -Requirement "All previous device updates"
```

This command modifies a device program.

## PARAMETERS

### -AddSupportedOperatingSystemPlatform
```yaml
Type: IResultObject[]
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases: AddSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AfterRunningType
Specifies the action that occurs after the program completes successfully.
The acceptable values for this parameter are:

- ConfigurationManagerLogUserOff 
- ConfigurationManagerStartsComputer 
 NoActionRequired 
- ProgramControlsRestart.

```yaml
Type: AfterRunningType
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:
Accepted values: NoActionRequired, ConfigurationManagerRestartsComputer, ProgramControlsRestart, ConfigurationManagerLogsUserOff

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Category
Specifies the category under which the program is displayed on the client computer.

```yaml
Type: String
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommandLine
Specifies the command line for the program.

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

### -CommandLineFolder
Specifies the folder that contains the executable program.
This folder can be an absolute path on the client, or a path relative to the distribution folder that contains the package.

```yaml
Type: String
Parameter Sets: SetDeviceProgramByName, SetDeviceProgramById, SetDeviceProgramByValue, SetDeviceProgramByProgramValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies optional text about a program, such as a description.
On client computers, this text appears in Run Advertised Programs in Control Panel.

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

### -DeviceProgram
```yaml
Type: SwitchParameter
Parameter Sets: SetDeviceProgramByName, SetDeviceProgramById, SetDeviceProgramByValue, SetDeviceProgramByProgramValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableMomAlertOnRun
Indicates whether the computer running the program is in maintenance mode for the duration of the program.
When in maintenance mode, Microsoft Operations Manager (MOM) disables alerts while the program runs.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableProgram
Indicates whether to temporarily disable all advertisements that contain this program.
If this option is selected, the program is removed from the list of available programs for users to run and it is run through assignment until re-enabled.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
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

### -DiskSpaceRequirement
Specifies the amount of disk space that the software program requires to run on the computer.
Requires the *DiskSpaceUnit* parameter be set.
The value must be greater than or equal to zero.

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

### -DiskSpaceUnit
Specifies the units for the *DiskSpaceRequirement* parameter.
The acceptable values for this parameter are: GB, KB, and MB.

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
Specifies when the program is to run.
The acceptable values for this parameter are:

- AsSoonAsPossible 
- OnlyOverFastNetwork 
- OnlyWhenTheDeviceIsLocked

```yaml
Type: DownloadProgramType
Parameter Sets: SetDeviceProgramByName, SetDeviceProgramById, SetDeviceProgramByValue, SetDeviceProgramByProgramValue
Aliases:
Accepted values: AsSoonAsPossible, OnlyOverFastNetwork, OnlyWhenTheDeviceIsDocked

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveLetter
Specifies a drive letter to qualify the location if the *DriveMode* parameter is used.

```yaml
Type: String
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriveMode
Indicates whether the program requires a specific drive letter, specified in the *DriveLetter* parameter.
By default, the program runs with a Universal Naming Convention (UNC) name.
If *DriveMode* is set to RequiresDriveLetter, the program uses any available drive letter.
If *DriveMode* is set to RequiresSpecificDriveLetter, the program only runs if the drive is not already used.

```yaml
Type: DriveModeType
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:
Accepted values: RenameWithUnc, RequiresDriveLetter, RequiresSpecificDriveLetter

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Duration
Specifies the maximum amount of time the program is expected to run.
The default value is 120 minutes.

```yaml
Type: Int32
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableTaskSequence
Indicates whether this program can be installed from the Install Software task sequence.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
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

### -GenerateMomAlertOnFail
Indicates whether Configuration Manager generates an application log event entry if the program fails.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMProgram** object.
To obtain a **CMProgram** object, use the [Get-CMProgram](Get-CMProgram.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByValue, SetDeviceProgramByValue, SetDeviceProgramByProgramValue
Aliases: ProgramPackage, Package, Program

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -PackageId
Specifies a package ID.

```yaml
Type: String
Parameter Sets: SetStandardProgramById, SetDeviceProgramById
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageName
Specifies a package name.

```yaml
Type: String
Parameter Sets: SetStandardProgramByName, SetDeviceProgramByName
Aliases: Name

Required: True
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

### -ProgramAssignedType
Specifies whether the program runs once on the computer, or once for every user who logs on to the computer.
The default setting is RunOnceForTheComputer.
The program is only assigned to users when the *ProgramRunType* parameter is set to OnlyWhenUserIsLoggedOn.

```yaml
Type: ProgramAssignedType
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:
Accepted values: RunOnceForTheComputer, RunOnceForEveryUserWhoLogsOn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramName
Specifies the name of the program.

```yaml
Type: String
Parameter Sets: SetStandardProgramByName, SetDeviceProgramByName, SetStandardProgramById, SetDeviceProgramById, SetStandardProgramByValue, SetDeviceProgramByValue
Aliases: StandardProgramName, DeviceProgramName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramRunType
Specifies the logon conditions that are necessary for the program to run.
The acceptable values for this parameter are:

- OnlyWhenNoUserIsLoggedOn 
- OnlyWhenUserIsLoggedOn 
- WhetherOrNotUserIsLoggedOn 

The default setting is OnlyWhenUserIsLoggedOn.

```yaml
Type: ProgramRunType
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:
Accepted values: OnlyWhenUserIsLoggedOn, WhetherOrNotUserIsLoggedOn, OnlyWhenNoUserIsLoggedOn

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Reconnect
Indicates whether the client computer reconnects to the distribution point when the user logs on.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSupportedOperatingSystemPlatform
```yaml
Type: IResultObject[]
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases: RemoveSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Requirement
Specifies any additional requirements for standard or device programs.

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

### -RunMode
Specifies the credentials the client computer requires to run the program.
The acceptable values for this parameter are: RunWithAdministrativeRights and RunWithUserRights.

```yaml
Type: RunModeType
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:
Accepted values: RunWithUserRights, RunWithAdministrativeRights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunOnAnyPlatform
```yaml
Type: SwitchParameter
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases: ClearSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunType
Specifies the mode is which the program will run on the client computer.
The acceptable values for this parameter are:

- Hidden 
- Maximized 
- Minimized 
- Normal 

The default is Normal.

```yaml
Type: RunType
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:
Accepted values: Normal, Minimized, Maximized, Hidden

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StandardProgram
Indicates that the program type in the deployment package is standard program.

```yaml
Type: SwitchParameter
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuppressProgramNotification
```yaml
Type: Boolean
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserInteraction
Indicates whether to allow users to interact with the program.

```yaml
Type: Boolean
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
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

### -WorkingDirectory
Specifies a working directory for the program.

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

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMProgram](Disable-CMProgram.md)

[Enable-CMProgram](Enable-CMProgram.md)

[Get-CMProgram](Get-CMProgram.md)

[New-CMProgram](New-CMProgram.md)

[Remove-CMProgram](Remove-CMProgram.md)
