---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
online version:
schema: 2.0.0
---

# Get-CMSoftwareUpdatePhasedDeployment

## SYNOPSIS

Get the phased deployment for software updates.

## SYNTAX

### SearchBySoftwareUpdate
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdate <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroup
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroup <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroupId
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroupName
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateId
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateName
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMSoftwareUpdatePhasedDeployment -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMSoftwareUpdatePhasedDeployment -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the phased deployment for software updates.

For more information, see [Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence?toc=/mem/configmgr/sum/toc.json&bc=/mem/configmgr/sum/breadcrumb/toc.json).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get deployment by name

This example gets the software update phased deployment by its name.

```powershell
Get-CMSoftwareUpdatePhasedDeployment -Name "myPhasedDeploymentName"
```

### Example 2: Get deployment by software update name

This example gets the software update phased deployment by the name of the software update.

```powershell
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName "myUpdateName"
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

### -SoftwareUpdate

Specify a software update object.

```yaml
Type: IResultObject
Parameter Sets: SearchBySoftwareUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroup

Specify a software update group object.

```yaml
Type: IResultObject
Parameter Sets: SearchBySoftwareUpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId

Specify the ID of a software update group.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName

Specify the name of a software update group.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId

Specify the ID of a software update.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName

Specify the name of a software update.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateName
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

[New-CMSoftwareUpdateAutoPhasedDeployment](New-CMSoftwareUpdateAutoPhasedDeployment.md)
[Remove-CMSoftwareUpdatePhasedDeployment](Remove-CMSoftwareUpdatePhasedDeployment.md)
[Set-CMSoftwareUpdatePhasedDeployment](Set-CMSoftwareUpdatePhasedDeployment.md)

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)
[Move-CMPhasedDeploymentToNext](Move-CMPhasedDeploymentToNext.md)
[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)
[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence?toc=/mem/configmgr/sum/toc.json&bc=/mem/configmgr/sum/breadcrumb/toc.json)
