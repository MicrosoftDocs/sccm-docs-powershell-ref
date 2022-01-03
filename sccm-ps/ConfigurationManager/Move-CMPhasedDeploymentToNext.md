---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/03/2022
online version:
schema: 2.0.0
---

# Move-CMPhasedDeploymentToNext

## SYNOPSIS

Move the specified phased deployment to the next phase.

## SYNTAX

### SearchByValue
```
Move-CMPhasedDeploymentToNext [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Move-CMPhasedDeploymentToNext [-Force] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Move-CMPhasedDeploymentToNext [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to move the specified phased deployment to the next phase.

For more information, see [Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Move to the next phase for the deployment by name

This example targets a phased deployment by its name, and moves it to the next phase.

```powershell
Move-CMPhasedDeploymentToNext -Name "myPhasedDeploymentName"
```

### Example 1: Force move to the next phase for an input deployment object

This example targets a phased deployment by a piped object, and force moves it to the next phase.

```powershell
$myPhasedDeployment | Move-CMPhasedDeploymentToNext -Force
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

### -Force

Force moves the deployment to the next phase.

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

Specify the phased deployment ID.

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

Specify a phased deployment object. To get this object, use one of the following cmdlets:

- [Get-CMApplicationPhasedDeployment](Get-CMApplicationPhasedDeployment.md)
- [Get-CMSoftwareUpdatePhasedDeployment](Get-CMSoftwareUpdatePhasedDeployment.md)
- [Get-CMTaskSequencePhasedDeployment](Get-CMTaskSequencePhasedDeployment.md)

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

Specify a phased deployment by name.

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

### System.Object
## NOTES

## RELATED LINKS

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)
[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)
[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Get-CMApplicationPhasedDeployment](Get-CMApplicationPhasedDeployment.md)
[Get-CMSoftwareUpdatePhasedDeployment](Get-CMSoftwareUpdatePhasedDeployment.md)
[Get-CMTaskSequencePhasedDeployment](Get-CMTaskSequencePhasedDeployment.md)

[Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence)
