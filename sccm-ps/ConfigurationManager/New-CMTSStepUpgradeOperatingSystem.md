---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/04/2021
online version:
schema: 2.0.0
---

# New-CMTSStepUpgradeOperatingSystem

## SYNOPSIS

Create an **Upgrade OS** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepUpgradeOperatingSystem [-DriverPackage <IResultObject>]
 [-DynamicUpdateSetting <DynamicUpdateOption>] [-EditionIndex <Int32>] [-IgnoreMessage <Boolean>]
 [-ProductKey <String>] [-ScanOnly <Boolean>] [-SetupTimeout <Int32>] [-SourcePath <String>]
 [-StagedContent <String>] [-UpgradePackage <IResultObject>] [-SoftwareUpdate <IResultObject[]>]
 [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>] [-Disable] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Upgrade OS** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Upgrade OS](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_UpgradeOS).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMOperatingSystemInstaller** cmdlet to get an object for the OS upgrade package. It saves this object in the **$osUpgPkg** variable. The next step creates an object for the **Upgrade OS** step, using the **$osUpgPkg** object as the OS upgrade package.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$osUpgPkg = Get-CMOperatingSystemInstaller -Name "OSUpgradePkg01"
$step = New-CMTSStepUpgradeOperatingSystem -Name "Upgrade OS" -UpgradePackage $osUpgPkg -EditionIndex 1

$tsNameOsd = "Default OS upgrade"
$tsUpg = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsUpg | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -Condition

Specify a condition object to use with this step. To get this object, use one of the task sequence condition cmdlets. For example, [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md).

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Conditions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinueOnError

Add this parameter to enable the step option **Continue on error**. When you enable this option, if the step fails, the task sequence continues.

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

### -Description

Specify an optional description for this task sequence step.

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

### -Disable

Add this parameter to disable this task sequence step.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableThisStep

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

### -DriverPackage

Specify a driver package object to provide its driver content to Windows Setup during upgrade. To get this package, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

Use the **StagedContent** parameter to specify the location for the driver content.

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

### -DynamicUpdateSetting

Use this parameter to dynamically update Windows Setup with Windows Update.

- `DisablePolicy`: Don't use Dynamic Update
- `UsingPolicy`: Enable setup to use Dynamic Update, such as search, download, and install updates.
- `OverridePolicy`: Temporarily override the local policy in real time to run Dynamic Update operations. The computer gets updates from Windows Update.

```yaml
Type: DynamicUpdateOption
Parameter Sets: (All)
Aliases:
Accepted values: DisablePolicy, UsingPolicy, OverridePolicy

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EditionIndex

Specify an integer value of the OS upgrade package edition. Use this parameter with the **UpgradePackage** parameter.

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

### -IgnoreMessage

Set this parameter to `$true` to specify that Windows Setup completes the installation, ignoring any dismissible compatibility messages.

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

### -Name

Specify a name for this step to identify it in the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductKey

Specify the product key to apply to the upgrade process.

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

### -ScanOnly

Set this parameter to `$true` to run the Windows Setup compatibility scan without starting upgrade.

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

### -SetupTimeout

Specify the number of minutes before Configuration Manager fails this step. This option is useful if Windows Setup stops processing but doesn't terminate.

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

### -SoftwareUpdate

Starting in version 2107, specify a software update object to upgrade a client's Windows OS by using a feature update. To get this object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourcePath

Specify a local or network path to the Windows media that Windows Setup uses.

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

### -StagedContent

Use this parameter with **DriverPackage** to specify the location for the driver content. You can specify a local folder, network path, or a task sequence variable.

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

### -UpgradePackage

Specify an OS upgrade package object. Use the **EditionIndex** parameter to set the edition.

To get this object, use the [Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md) cmdlet.

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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### IResultObject#SMS_TaskSequence_UpgradeOperatingSystemAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_UpgradeOperatingSystemAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_upgradeoperatingsystemaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepUpgradeOperatingSystem](Get-CMTSStepUpgradeOperatingSystem.md)
[Remove-CMTSStepUpgradeOperatingSystem](Remove-CMTSStepUpgradeOperatingSystem.md)
[Set-CMTSStepUpgradeOperatingSystem](Set-CMTSStepUpgradeOperatingSystem.md)

[About task sequence steps: Upgrade OS](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_UpgradeOS)
