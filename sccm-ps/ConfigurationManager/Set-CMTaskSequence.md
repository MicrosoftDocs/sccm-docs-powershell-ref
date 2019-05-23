---
title: Set-CMTaskSequence
titleSuffix: Configuration Manager
description: 
ms.date: 11/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Set-CMTaskSequence

## SYNOPSIS

Sets a Configuration Manager task sequence.

## SYNTAX

### SetByValue (Default)

```powershell
Set-CMTaskSequence -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-Category <String>] [-UseDefaultText <Boolean>] [-CustomText <String>] [-RunAnotherProgram <Boolean>]
 [-DeploymentPackageId <String>] [-ProgramName <String>] [-RunEveryTime <Boolean>]
 [-SuppressNotification <Boolean>] [-EnableNotification <Boolean>] [-DisableTaskSequence <Boolean>]
 [-EnableTaskSequence <Boolean>] [-MaxRunTimeMins <Int64>] [-UseBootImage <Boolean>] [-BootImageId <String>]
 [-AddSupportedOperatingSystemPlatform <IResultObject[]>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-RunOnAnyPlatform] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById

```powershell
Set-CMTaskSequence -TaskSequenceId <String> [-NewName <String>] [-Description <String>] [-Category <String>]
 [-UseDefaultText <Boolean>] [-CustomText <String>] [-RunAnotherProgram <Boolean>]
 [-DeploymentPackageId <String>] [-ProgramName <String>] [-RunEveryTime <Boolean>]
 [-SuppressNotification <Boolean>] [-EnableNotification <Boolean>] [-DisableTaskSequence <Boolean>]
 [-EnableTaskSequence <Boolean>] [-MaxRunTimeMins <Int64>] [-UseBootImage <Boolean>] [-BootImageId <String>]
 [-AddSupportedOperatingSystemPlatform <IResultObject[]>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-RunOnAnyPlatform] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName

```powershell
Set-CMTaskSequence -TaskSequenceName <String> [-NewName <String>] [-Description <String>] [-Category <String>]
 [-UseDefaultText <Boolean>] [-CustomText <String>] [-RunAnotherProgram <Boolean>]
 [-DeploymentPackageId <String>] [-ProgramName <String>] [-RunEveryTime <Boolean>]
 [-SuppressNotification <Boolean>] [-EnableNotification <Boolean>] [-DisableTaskSequence <Boolean>]
 [-EnableTaskSequence <Boolean>] [-MaxRunTimeMins <Int64>] [-UseBootImage <Boolean>] [-BootImageId <String>]
 [-AddSupportedOperatingSystemPlatform <IResultObject[]>]
 [-RemoveSupportedOperatingSystemPlatform <IResultObject[]>] [-RunOnAnyPlatform] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMTaskSequence** cmdlet modifies a Microsoft System Center Configuration Manager task sequence.

## EXAMPLES

### Example 1: Get a task sequence and change its name

```powershell
PS C:\> $TaskSequence = Get-CMTaskSequence -Name "TaskSequence01"
PS C:\> Set-CMTaskSequence -InputObject $TaskSequence -NewName "NewTS01"
```

The first command gets the task sequence object named TaskSequence01 and stores the object in the $TaskSequence variable.

The second command changes the name of the task sequence stored in $TaskSequence to NewTS01.

### Example 2: Pass a task sequence and change its name

```powershell
PS C:\> Get-CMTaskSequence -Name "TaskSequence02" | Set-CMTaskSequence -NewName "NewTS02"
```

This command gets the task sequence object named TaskSequence02 and uses the pipeline operator to pass the object to **Set-CMTaskSequence**, which changes the name of the task sequence object to NewTS02.

## PARAMETERS

### -AddSupportedOperatingSystemPlatform

Adds a supported operating system platform object to the task sequence.
To obtain a supported operating system platform object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BootImageId

Specifies the ID of a boot image.

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

### -Category

Specifies a category for the task sequence.
You can use categories to group task sequences.

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

### -CustomText

Specifies custom text for the task sequence.
Custom text appears in the progress notification dialog box while the task sequence runs.

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

### -DeploymentPackageId

Specifies the ID of a package.
If you specify a value of $True for the *RunAnotherProgram* parameter, the specified package runs before the task sequence runs.

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

### -Description

Specifies a description for the task sequence.

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

### -DisableTaskSequence

Indicates whether to disable this task sequence.

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

### -EnableNotification

Indicates whether to enable notifications for this task sequence.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableNotifications

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableTaskSequence

Indicates whether to enable this task sequence.

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

### -InputObject

Specifies a task sequence object.
To obtain a task sequence object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: TaskSequence

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxRunTimeMins

Specifies, in minutes, the maximum running time for the task sequence.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: Duration

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specifies a new name for the task sequence.

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

### -ProgramName

Specifies the name of a program to run from a Configuration Manager software package specified by the *DeploymentPackageId* parameter.

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

### -RemoveSupportedOperatingSystemPlatform

Removes a supported operating system platform object from the task sequence.
To obtain a supported operating system platform object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RunAnotherProgram

Indicates whether to run another program before running the task sequence.
Specify the program by using the *DeploymentPackageId* parameter and the *ProgramName* parameter.

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

### -RunEveryTime

Indicates whether the program specified in the *ProgramName* parameter runs every time that the task sequence runs.
If you specify a value of $False, the program does not run if it has run successfully in the past.

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

### -RunOnAnyPlatform

Indicates that the task sequence runs on any operating system platform.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ClearSupportedOperatingSystemPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SuppressNotification

Indicates whether to suppress notifications for this task sequence.

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

### -TaskSequenceId

Specifies the ID of a task sequence.

```yaml
Type: String
Parameter Sets: SetById
Aliases: Id, TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specifies the name of a task sequence.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseBootImage

Indicates whether the task sequence uses the boot image specified by using the *BootImageID* parameter.

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

### -UseDefaultText

Indicates whether to use default text in the progress notification dialog box while the task sequence runs.
If you select a value of $False for this parameter, be sure to specify custom text by using the *CustomText* parameter.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[New-CMTaskSequence](New-CMTaskSequence.md)
[Get-CMTaskSequence](Get-CMTaskSequence.md)
[Set-CMTaskSequence](Set-CMTaskSequence.md)
[Copy-CMTaskSequence](Copy-CMTaskSequence.md)
[Enable-CMTaskSequence](Enable-CMTaskSequence.md)
[Disable-CMTaskSequence](Disable-CMTaskSequence.md)
[Import-CMTaskSequence](Import-CMTaskSequence.md)
[Export-CMTaskSequence](Export-CMTaskSequence.md)
[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)
