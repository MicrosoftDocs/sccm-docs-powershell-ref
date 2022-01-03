---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/03/2022
online version:
schema: 2.0.0
---

# New-CMSoftwareUpdateManualPhasedDeployment

## SYNOPSIS

Create a phased deployment for software updates.

## SYNTAX

### SearchByGroupMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateGroup] <IResultObject> -AddPhases <Phase[]>
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByGroupIdMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateGroupId] <String> -AddPhases <Phase[]>
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByGroupNameMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateGroupName] <String> -AddPhases <Phase[]>
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateIds] <String[]> -AddPhases <Phase[]>
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateNames] <String[]> -AddPhases <Phase[]>
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdates] <IResultObject[]> -AddPhases <Phase[]>
 [-Description <String>] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a phased deployment for software updates. Before you use this cmdlet, add new customized deployment phases with the cmdlet [New-CMSoftwareUpdatePhase](New-CMSoftwareUpdatePhase.md).

For more information, see [Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence?toc=/mem/configmgr/sum/toc.json&bc=/mem/configmgr/sum/breadcrumb/toc.json).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).
## EXAMPLES

### Example 1: Create a deployment for software updates by name

This example creates a two-phase deployment named **myPhaseDeployment** for two software updates.

```powershell
$phase1 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM001" -PhaseName "test01" -UserNotificationOption DisplaySoftwareCenterOnly
$phase2 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM003" -PhaseName "test02" -UserNotificationOption DisplaySoftwareCenterOnly
New-CMSoftwareUpdateManualPhasedDeployment -SoftwareUpdateNames ("myUpdateA", "myUpdateB") -Name "myPhaseDeployment" -AddPhases ($phase1, $phase2)
```

### Example 2: Create a deployment for a software update group by name

This example creates a two-phase deployment named **myPhaseDeploymentForGroup** for the software update group **myGroup**.

```powershell
$phase3 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM001" -PhaseName "test03" -UserNotificationOption DisplaySoftwareCenterOnly
$phase4 = New-CMSoftwareUpdatePhase -CollectionId "SMSDM003" -PhaseName "test04" -UserNotificationOption DisplaySoftwareCenterOnly
New-CMSoftwareUpdateManualPhasedDeployment -SoftwareUpdateGroupName "myGroup" -Name "myPhaseDeploymentForGroup" -AddPhases ($phase3, $phase4)
```

## PARAMETERS

### -AddPhases

Specify an array of phases. Use [New-CMSoftwareUpdatePhase](New-CMSoftwareUpdatePhase.md) to create the phases.

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

Specify a description for the software update phased deployment.

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

### -Name

Specify a name for the software update phased deployment.

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

### -SoftwareUpdateGroup

Specify an object for a software update group. To get this object, use the [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByGroupMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId

Specify a software update group by ID.

```yaml
Type: String
Parameter Sets: SearchByGroupIdMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName

Specify a software update group by name.

```yaml
Type: String
Parameter Sets: SearchByGroupNameMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateIds

Specify an array of software update IDs.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateNames

Specify an array of software update names.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdates

Specify an array of software update objects. To get this object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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
### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
## OUTPUTS

### IResultObject#SMS_PhasedDeployment
## NOTES

The return object is the **SMS_PhasedDeployment** server WMI class.

## RELATED LINKS

[Get-CMSoftwareUpdatePhasedDeployment](Get-CMSoftwareUpdatePhasedDeployment.md)
[Remove-CMSoftwareUpdatePhasedDeployment](Remove-CMSoftwareUpdatePhasedDeployment.md)
[Set-CMSoftwareUpdatePhasedDeployment](Set-CMSoftwareUpdatePhasedDeployment.md)

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)
[Move-CMPhasedDeploymentToNext](Move-CMPhasedDeploymentToNext.md)
[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)
[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence?toc=/mem/configmgr/sum/toc.json&bc=/mem/configmgr/sum/breadcrumb/toc.json)
