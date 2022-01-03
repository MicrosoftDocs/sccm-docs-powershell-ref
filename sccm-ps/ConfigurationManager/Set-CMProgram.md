---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Set-CMProgram
---

# Set-CMProgram

## SYNOPSIS

Modify a program of a package.

## SYNTAX

### SetStandardProgramByProgramValue (Default)
```
Set-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] [-AfterRunningType <AfterRunningType>]
 [-Category <String>] [-CommandLine <String>] [-Comment <String>] [-DisableMomAlertOnRun <Boolean>]
 [-DisableProgram <Boolean>] [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DriveLetter <String>] [-DriveMode <DriveModeType>] [-Duration <Int32>] [-EnableTaskSequence <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] -InputObject <IResultObject> [-PassThru]
 [-ProgramAssignedType <ProgramAssignedType>] [-ProgramRunType <ProgramRunType>] [-Reconnect <Boolean>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-Requirement <String>] [-RunMode <RunModeType>]
 [-RunOnAnyPlatform] [-RunType <RunType>] [-StandardProgram] [-SuppressProgramNotification <Boolean>]
 [-UserInteraction <Boolean>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramByName
```
Set-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] [-AfterRunningType <AfterRunningType>]
 [-Category <String>] [-CommandLine <String>] [-Comment <String>] [-DisableMomAlertOnRun <Boolean>]
 [-DisableProgram <Boolean>] [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DriveLetter <String>] [-DriveMode <DriveModeType>] [-Duration <Int32>] [-EnableTaskSequence <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] -PackageName <String> [-PassThru]
 [-ProgramAssignedType <ProgramAssignedType>] -ProgramName <String> [-ProgramRunType <ProgramRunType>]
 [-Reconnect <Boolean>] [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-Requirement <String>]
 [-RunMode <RunModeType>] [-RunOnAnyPlatform] [-RunType <RunType>] [-StandardProgram]
 [-SuppressProgramNotification <Boolean>] [-UserInteraction <Boolean>] [-WorkingDirectory <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramById
```
Set-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] [-AfterRunningType <AfterRunningType>]
 [-Category <String>] [-CommandLine <String>] [-Comment <String>] [-DisableMomAlertOnRun <Boolean>]
 [-DisableProgram <Boolean>] [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DriveLetter <String>] [-DriveMode <DriveModeType>] [-Duration <Int32>] [-EnableTaskSequence <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] -PackageId <String> [-PassThru]
 [-ProgramAssignedType <ProgramAssignedType>] -ProgramName <String> [-ProgramRunType <ProgramRunType>]
 [-Reconnect <Boolean>] [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-Requirement <String>]
 [-RunMode <RunModeType>] [-RunOnAnyPlatform] [-RunType <RunType>] [-StandardProgram]
 [-SuppressProgramNotification <Boolean>] [-UserInteraction <Boolean>] [-WorkingDirectory <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStandardProgramByValue
```
Set-CMProgram [-AddSupportedOperatingSystemPlatform <IResultObject[]>] [-AfterRunningType <AfterRunningType>]
 [-Category <String>] [-CommandLine <String>] [-Comment <String>] [-DisableMomAlertOnRun <Boolean>]
 [-DisableProgram <Boolean>] [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DriveLetter <String>] [-DriveMode <DriveModeType>] [-Duration <Int32>] [-EnableTaskSequence <Boolean>]
 [-GenerateMomAlertOnFail <Boolean>] -InputObject <IResultObject> [-PassThru]
 [-ProgramAssignedType <ProgramAssignedType>] -ProgramName <String> [-ProgramRunType <ProgramRunType>]
 [-Reconnect <Boolean>] [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-Requirement <String>]
 [-RunMode <RunModeType>] [-RunOnAnyPlatform] [-RunType <RunType>] [-StandardProgram]
 [-SuppressProgramNotification <Boolean>] [-UserInteraction <Boolean>] [-WorkingDirectory <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramByName
```
Set-CMProgram [-CommandLine <String>] [-CommandLineFolder <String>] [-Comment <String>] [-DeviceProgram]
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -PackageName <String> [-PassThru] -ProgramName <String>
 [-Requirement <String>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramById
```
Set-CMProgram [-CommandLine <String>] [-CommandLineFolder <String>] [-Comment <String>] [-DeviceProgram]
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -PackageId <String> [-PassThru] -ProgramName <String>
 [-Requirement <String>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramByValue
```
Set-CMProgram [-CommandLine <String>] [-CommandLineFolder <String>] [-Comment <String>] [-DeviceProgram]
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -InputObject <IResultObject> [-PassThru] -ProgramName <String>
 [-Requirement <String>] [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDeviceProgramByProgramValue
```
Set-CMProgram [-CommandLine <String>] [-CommandLineFolder <String>] [-Comment <String>] [-DeviceProgram]
 [-DiskSpaceRequirement <String>] [-DiskSpaceUnit <DiskSpaceUnitType>]
 [-DownloadProgramType <DownloadProgramType>] -InputObject <IResultObject> [-PassThru] [-Requirement <String>]
 [-WorkingDirectory <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to modify a program of a package.
Programs identify the actions that occur when the client receives the client package.
You can associate multiple programs with the same package.
For more information, see [Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify a standard program

```powershell
Set-CMProgram -Name "Test" -StandardProgramName SPM -Comment "Standard Upgrades" -CommandLine "RunThisNow" -RunType Maximized -AfterRunningType ProgramControlsRestart -Category "Laptops" -DiskSpaceRequirement 50 -DiskSpaceUnit MB -Duration 150 -Requirement 4 -Reconnect $False -SuppressProgramNotifications $False -DisableProgram $True -EnableTaskSequence $True -DisableMomAlertOnRun $True -GenerateMomAlertOnFail $True
```

### Example 2: Modify a device program

```powershell
Set-CMProgram -Name "Test" -DeviceProgramName DPM -Comment "Upgrades for December" -CommandLine "RunMe" -WorkingDirectory "\TempWork" -CommandLineFolder "C:\Windows" -DiskSpaceRequirement 30 -DiskSpaceUnit MB -DownloadProgramType AsSoonAsPossible -Requirement "All previous device updates"
```

### Example 3: Add a supported OS platform

This example sets the OS requirement for a program associated with a standard package. It uses the **Get-CMSupportedPlatform** cmdlet to get an object for the specified platform. It then uses this supported platform object to configure the program.<!-- sccm-docs-powershell-ref #240 -->

```powershell
$ProgramName = 'Script'
$PackageID = 'XYZ0000D'
$Platform = 'All Windows 10 (64-bit) Client'
$OS = Get-CMSupportedPlatform -Name $Platform -Fast

Set-CMProgram -PackageID $PackageID -ProgramName $ProgramName -AddSupportedOperatingSystemPlatform $OS -StandardProgram
```

## PARAMETERS

### -AddSupportedOperatingSystemPlatform

Specify one or more supported OS platforms to add for the program. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

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

Specify the action that occurs after the program completes successfully.

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

Specify the category under which the program is displayed on the client computer.

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

Specify the command line for the program.

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

Specify the folder that contains the executable program. This folder can be an absolute path on the client, or a path relative to the distribution folder that contains the package.

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

Specify optional text about the program, such as a description. On client computers, this text displays with the program in Software Center.

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

### -DeviceProgram

Add this parameter to configure this program as a device program.

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

Indicates whether the computer running the program is in maintenance mode for the duration of the program. When in maintenance mode, System Center Operations Manager disables alerts while the program runs.

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

Set this parameter to `$true` to temporarily disable all deployments that contain this program. You can also use the [Disable-CMProgram](Disable-CMProgram.md) cmdlet.

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
Aliases:

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

If you use the **DriveMode** parameter, specify a drive letter for the location.

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

Indicates whether the program requires a specific drive letter, specified in the **DriveLetter** parameter.

- `RunWithUnc`: Run the program from the UNC path. This value is the default. Starting in version 2010, this value was renamed from `RenameWithUnc`.

- `RequiresDriveLetter`: The program uses any available drive letter.

- `RequiresSpecificDriveLetter`: The program only runs if the drive isn't already in use.

```yaml
Type: DriveModeType
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
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
Parameter Sets: SetStandardProgramByProgramValue, SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableTaskSequence

Indicates whether this program can be installed from the **Install Package** task sequence step.

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

Specify a program object to configure. To get this object, use the [Get-CMProgram](Get-CMProgram.md) cmdlet.

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

Specify a package ID with the program to configure.

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

Specify a package name with the program to configure.

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

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

Specify whether the program runs once on the computer, or once for every user who signs in to the computer. The default value is `RunOnceForTheComputer`. The program is only assigned to users when the **ProgramRunType** parameter is set to `OnlyWhenUserIsLoggedOn`.

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

Specify the name of the program to configure.

```yaml
Type: String
Parameter Sets: SetStandardProgramByName, SetStandardProgramById, SetStandardProgramByValue, SetDeviceProgramByName, SetDeviceProgramById, SetDeviceProgramByValue
Aliases: StandardProgramName, DeviceProgramName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramRunType

Specify the logon conditions that are necessary for the program to run. The default value is `OnlyWhenUserIsLoggedOn`.

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

Indicates whether the client computer reconnects to the distribution point when the user signs in.

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

Specify one or more supported OS platforms to remove for the program. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

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

Specify any additional requirements for standard or device programs.

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

Specify the credentials the client computer requires to run the program.

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

Add this parameter to clear all supported OS platforms from this program.

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

Specify the mode in which the program runs on the client computer. The default value is `Normal`.

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

Set this parameter to `$true` to suppress program notifications.

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

[Disable-CMProgram](Disable-CMProgram.md)

[Enable-CMProgram](Enable-CMProgram.md)

[Get-CMProgram](Get-CMProgram.md)

[New-CMProgram](New-CMProgram.md)

[Remove-CMProgram](Remove-CMProgram.md)

[Packages and programs in Configuration Manager](/mem/configmgr/apps/deploy-use/packages-and-programs)
