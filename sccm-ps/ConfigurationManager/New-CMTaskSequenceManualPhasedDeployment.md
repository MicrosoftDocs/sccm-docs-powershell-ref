---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMTaskSequenceManualPhasedDeployment

## SYNOPSIS

Use this cmdlet to create a phased deployment for a task sequence.

## SYNTAX

### SearchByValueMandatory
```
New-CMTaskSequenceManualPhasedDeployment [-TaskSequence] <IResultObject> -AddPhases <Phase[]> -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMTaskSequenceManualPhasedDeployment [-TaskSequenceId] <String> -AddPhases <Phase[]> -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMTaskSequenceManualPhasedDeployment [-TaskSequenceName] <String> -AddPhases <Phase[]> -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to create a phased deployment for a task sequence. Before you use this cmdlet, add new customized deployment phases with the cmdlet [New-CMTaskSequencePhase](New-CMTaskSequencePhase.md).

## EXAMPLES

### Example 1: Create a deployment for a task sequence by name

This example creates a two-phase deployment named **phaseDeployment** for the task sequence **myTaskSequence**.

```powershell
$phase1 = New-CMTaskSequencePhase -CollectionId "SMSDM001" -PhaseName "test01" -UserNotification DisplayAll
$phase2 = New-CMTaskSequencePhase -CollectionId "SMSDM003" -PhaseName "test02" -UserNotification HideAll
New-CMTaskSequenceManualPhasedDeployment -TaskSequenceName "myTaskSequence" -Name "phasedDeployment" -AddPhases ($phase1, $phase2)
```

### Example 2: Create a deployment for a task sequence object

This example creates a two-phase deployment named **phasedDeployment** for a piped task sequence object.

```powershell
$phase3 = New-CMTaskSequencePhase -CollectionId "SMSDM001" -PhaseName "test03" -UserNotification DisplayAll
$phase4 = New-CMTaskSequencePhase -CollectionId "SMSDM003" -PhaseName "test04" -UserNotification HideAll
$myTaskSequence | New-CMTaskSequenceManualPhasedDeployment -Name "phasedDeployment" -AddPhases ($phase3, $phase4)
```

## PARAMETERS

### -AddPhases

Specify an array of phases. Use [New-CMTaskSequencePhase](New-CMTaskSequencePhase.md) to create the phases.

```yaml
Type: Phase[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify a description for the task sequence phased deployment.

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

### -Name

Specify a name for the task sequence phased deployment.

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

### -TaskSequence

Specify a task sequence object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskSequenceId

Specify a task sequence by ID.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: TaskSequencePackageId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify a task sequence by name.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: 0
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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
