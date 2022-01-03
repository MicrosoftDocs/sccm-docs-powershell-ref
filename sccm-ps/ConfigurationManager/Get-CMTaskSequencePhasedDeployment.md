---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/03/2022
online version:
schema: 2.0.0
---

# Get-CMTaskSequencePhasedDeployment

## SYNOPSIS

Get the phased deployment for a task sequence.

## SYNTAX

### SearchByTaskSequence
```
Get-CMTaskSequencePhasedDeployment -TaskSequence <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByTaskSequenceId
```
Get-CMTaskSequencePhasedDeployment -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByTaskSequenceName
```
Get-CMTaskSequencePhasedDeployment -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMTaskSequencePhasedDeployment -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMTaskSequencePhasedDeployment -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the phased deployment for a task sequence.

For more information, see [Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the deployment by name

This example gets a task sequence phased deployment by the name of the phased deployment.

```powershell
Get-CMTaskSequencePhasedDeployment -Name "myPhasedDeploymentName"
```

### Example 2: Get the deployment by task sequence name

This example gets a task sequence phased deployment by the name of the task sequence.

```powershell
Get-CMTaskSequencePhasedDeployment -TaskSequenceName "myTaskSequenceName"
```

## PARAMETERS

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

Specify the ID of the phased deployment.

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

### -Name

Specify the name of the phased deployment.

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

### -TaskSequence

Specify a task sequence object. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByTaskSequence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskSequenceId

Specify the ID for a task sequence.

```yaml
Type: String
Parameter Sets: SearchByTaskSequenceId
Aliases: TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify the name for a task sequence.

```yaml
Type: String
Parameter Sets: SearchByTaskSequenceName
Aliases:

Required: True
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
### IResultObject[]#SMS_PhasedDeployment
## NOTES

The return object is the **SMS_PhasedDeployment** server WMI class.

## RELATED LINKS

[New-CMTaskSequenceAutoPhasedDeployment](New-CMTaskSequenceAutoPhasedDeployment.md)
[Remove-CMTaskSequencePhasedDeployment](Remove-CMTaskSequencePhasedDeployment.md)
[Set-CMTaskSequencePhasedDeployment](Set-CMTaskSequencePhasedDeployment.md)

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)
[Move-CMPhasedDeploymentToNext](Move-CMPhasedDeploymentToNext.md)
[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)
[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence)
