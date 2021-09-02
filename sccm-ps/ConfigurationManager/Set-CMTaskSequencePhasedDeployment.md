---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
online version:
schema: 2.0.0
---

# Set-CMTaskSequencePhasedDeployment

## SYNOPSIS

Configure a phased deployment for a task sequence.

## SYNTAX

### SearchByValue
```
Set-CMTaskSequencePhasedDeployment [-AddPhases <Phase[]>] [-Description <String>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-RemovePhaseIds <String[]>] [-RemovePhaseOrders <Int32[]>]
 [-RemovePhases <Phase[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchById
```
Set-CMTaskSequencePhasedDeployment [-AddPhases <Phase[]>] [-Description <String>] [-NewName <String>]
 [-PassThru] [-RemovePhaseIds <String[]>] [-RemovePhaseOrders <Int32[]>] [-RemovePhases <Phase[]>] -Id <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Set-CMTaskSequencePhasedDeployment [-AddPhases <Phase[]>] [-Description <String>] [-NewName <String>]
 [-PassThru] [-RemovePhaseIds <String[]>] [-RemovePhaseOrders <Int32[]>] [-RemovePhases <Phase[]>]
 -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Applies to version 2006 and later. Configure a phased deployment for a task sequence. For more information, see [Create phased deployments](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence).

## EXAMPLES

### Example 1: Rename a phased deployment

This example renames a task sequence phased deployment that's passed through on the command line.

```powershell
$tsPhasedDeployment = Get-CMTaskSequencePhasedDeployment -Name "myPhasedDeployment"

$tsPhasedDeployment | Set-CMTaskSequencePhasedDeployment -NewName "New TS phased deployment" -Description "New description" -PassThru
```

### Example 2: Add a phase

This example adds a phase to a task sequence phased deployment targeted by its ID.

```powershell
$newPhase = New-CMTaskSequencePhase -CollectionName "MyCollection" -PhaseName "MyTSPhase" -UserNotification DisplayAll -AllowRemoteDP $true

Set-CMTaskSequencePhasedDeployment -Id "0bc464d9-e7dd-44c1-a157-3f8be6a79c03" -AddPhases ($newPhase)
```

## PARAMETERS

### -AddPhases

Use this parameter to add one or more phases to a task sequence phased deployment. Use the [New-CMTaskSequencePhase](New-CMTaskSequencePhase.md) cmdlet to create a new phase object.

```yaml
Type: Phase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description to better identify this task sequence phased deployment.

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

### -Id

Specify the ID of the task sequence phased deployment to configure. The format of this value is a GUID.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: PhasedDeploymentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for an task sequence phased deployment to configure. For example, use the [Get-CMTaskSequencePhasedDeployment](Get-CMTaskSequencePhasedDeployment.md) cmdlet to get this object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: PhasedDeployment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the task sequence phased deployment to configure.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename the task sequence phased deployment.

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

### -RemovePhaseIds

Remove one or more phases specified by their ID.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemovePhaseOrders

Remove one or more phases specified by their order in the phased deployment.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemovePhases

Remove one or more phases from a task sequence phased deployment. Use the [Get-CMPhase](Get-CMPhase.md) cmdlet to identify the phase to remove.

```yaml
Type: Phase[]
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_PhasedDeployment
## NOTES

## RELATED LINKS

[Get-CMTaskSequencePhasedDeployment](Get-CMTaskSequencePhasedDeployment.md)

[New-CMTaskSequenceAutoPhasedDeployment](New-CMTaskSequenceAutoPhasedDeployment.md)

[New-CMTaskSequenceManualPhasedDeployment](New-CMTaskSequenceManualPhasedDeployment.md)

[Remove-CMTaskSequencePhasedDeployment](Remove-CMTaskSequencePhasedDeployment.md)

[Get-CMPhase](Get-CMPhase.md)

[New-CMTaskSequencePhase](New-CMTaskSequencePhase.md)

[Set-CMTaskSequencePhase](Set-CMTaskSequencePhase.md)

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)

[Move-CMPhasedDeploymentToNext](Move-CMPhasedDeploymentToNext.md)

[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)

[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Create phased deployments](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence)
