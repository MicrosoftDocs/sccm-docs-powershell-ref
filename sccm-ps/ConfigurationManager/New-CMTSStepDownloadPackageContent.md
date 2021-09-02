---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/12/2021
online version:
schema: 2.0.0
---

# New-CMTSStepDownloadPackageContent

## SYNOPSIS

Create a **Download Package Content** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepDownloadPackageContent -AddPackage <IResultObject[]> [-ContinueDownload <Boolean>]
 [-DestinationVariable <String>] [-LocationOption <LocationType>] [-Path <String>]
 [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>] [-Disable] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Download Package Content** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [Task sequence steps: Download package content](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_DownloadPackageContent).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a task sequence step with condition and add to a group

This example first sets variables for the necessary parameters. It then uses the **New-CMTSStepDownloadPackageContent** cmdlet to create the step, and saves that as a variable. It then adds the step to a task sequence in a specific group using the **Set-CMTaskSequenceGroup** cmdlet.

```powershell
$TaskSequenceName = "Module - Download Driver Packages"
$Model = "Latitude E7470"
$GroupName = "Dell Drivers"
$ContentPackage = Get-CMPackage -Fast -Name "Driver Dell Latitude E7470"
$StepName = $ContentPackage.Name
$ConditionQuery = "Select * From Win32_ComputerSystem Where Model = `"$Model`""
$StepCondition = New-CMTSStepConditionQueryWMI -Namespace "root\cimv2" -Query $ConditionQuery

$PackageStep = New-CMTSStepDownloadPackageContent -AddPackage $ContentPackage -Name $StepName -LocationOption TaskSequenceWorkingFolder -DestinationVariable "DRIVERS" -Condition $StepCondition

Set-CMTaskSequenceGroup -TaskSequenceName $TaskSequenceName -StepName $GroupName -AddStep $PackageStep -InsertStepStartIndex 1
```

## PARAMETERS

### -AddPackage

Specify one or more package objects to use with the step. To get this object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddPackages

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Condition

Specify a condition object to use with this step. To get a condition object, use one of the step condition cmdlets. For example, [New-CMTSStepConditionQueryWMI](New-CMTSStepConditionQueryWMI.md).

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

### -ContinueDownload

Set this parameter to `true` to continue downloading other packages in the list if a package download fails.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ContinueDownloadOnError

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

### -DestinationVariable

Use this parameter to save the package's path into a custom task sequence variable.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DestinationVariableName

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

### -LocationOption

Specify one of the following values for where the task sequence saves the package:

- `TaskSequenceWorkingFolder`: Use the task sequence working directory, which is also referred to as the task sequence cache.

- `ClientCache`: Use the Configuration Manager client cache. By default, this path is `%WinDir%\ccmcache`.

- `CustomPath`: The task sequence engine first downloads the package to the task sequence working directory. It then moves the content to this path you specify. The task sequence engine appends the path with the package ID. When you use this option, set the path with the **Path** parameter.

```yaml
Type: LocationType
Parameter Sets: (All)
Aliases:
Accepted values: TaskSequenceWorkingFolder, ClientCache, CustomPath

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

### -Path

When you specify `-LocationOption CustomPath`, use this parameter to specify the local path to save the package content. The task sequence engine appends the path with the package ID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DestinationCustomPath

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

### IResultObject#SMS_TaskSequence_DownloadPackageContentAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_DownloadPackageContentAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_downloadpackagecontentaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepDownloadPackageContent](Get-CMTSStepDownloadPackageContent.md)
[Remove-CMTSStepDownloadPackageContent](Remove-CMTSStepDownloadPackageContent.md)
[Set-CMTSStepDownloadPackageContent](Set-CMTSStepDownloadPackageContent.md)

[Task sequence steps: Download package content](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_DownloadPackageContent)
