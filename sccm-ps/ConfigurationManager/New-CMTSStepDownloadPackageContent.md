---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMTSStepDownloadPackageContent

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-CMTSStepDownloadPackageContent -AddPackage <IResultObject[]> [-LocationOption <LocationType>]
 [-Path <String>] [-DestinationVariable <String>] [-ContinueDownload <Boolean>] -Name <String>
 [-Description <String>] [-ContinueOnError] [-Disable] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1 Create Task Sequence Step with Condition, add to Group in Task Sequence
```powershell
PS XYZ:\> $TaskSequenceName = "Module - Download Driver Packages"
PS XYZ:\> $Model = "Latitude E7470"
PS XYZ:\> $GroupName = "Dell Drivers"
PS XYZ:\> $ContentPackage = Get-CMPackage -Fast -Name "Driver Dell Latitude E7470"
PS XYZ:\> $StepName = $ContentPackage.Name
PS XYZ:\> $ConditionQuery = "Select * From Win32_ComputerSystem Where Model = `"$Model`""
PS XYZ:\> $StepCondition = New-CMTaskSequenceStepConditionQueryWMI -Namespace "root\cimv2" -Query $ConditionQuery
PS XYZ:\> $PackageStep = New-CMTSStepDownloadPackageContent -AddPackage $ContentPackage -Name $StepName -LocationOption TaskSequenceWorkingFolder -DestinationVariable "DRIVERS" -Condition $StepCondition
PS XYZ:\> Set-CMTaskSequenceGroup -TaskSequenceName $TaskSequenceName -StepName $GroupName -AddStep $PackageStep -InsertStepStartIndex 1
```

{{ Add example description here }}

## PARAMETERS

### -AddPackage
{{ Fill AddPackage Description }}

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
Specify a condition object to use with this step.

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

### -ContinueDownload
{{ Fill ContinueDownload Description }}

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
{{ Fill DestinationVariable Description }}

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
{{ Fill LocationOption Description }}

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
{{ Fill Path Description }}

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

### IResultObject#SMS_TaskSequence_DownloadPackageContentAction

## NOTES

## RELATED LINKS
