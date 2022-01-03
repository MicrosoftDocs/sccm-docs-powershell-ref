---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
online version:
schema: 2.0.0
---

# Get-CMApplicationPhasedDeployment

## SYNOPSIS

Get a phased deployment for an application.

## SYNTAX

### SearchByApplication
```
Get-CMApplicationPhasedDeployment -Application <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByApplicationId
```
Get-CMApplicationPhasedDeployment -ApplicationId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByApplicationName
```
Get-CMApplicationPhasedDeployment -ApplicationName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMApplicationPhasedDeployment -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMApplicationPhasedDeployment -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a phased deployment for an application.

For more information, see [Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence?toc=/mem/configmgr/apps/toc.json&bc=/mem/configmgr/apps/breadcrumb/toc.json).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get phased deployment by name

This example gets the object by the name of the phased deployment.

```powershell
Get-CMApplicationPhasedDeployment -Name "myPhasedDeploymentName"
```

### Example 2: Get phased deployment by app name

This example gets the object by the name of the application.

```powershell
Get-CMApplicationPhasedDeployment -ApplicationName "myApplicationName"
```

## PARAMETERS

### -Application

Specify an object for the application. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByApplication
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ApplicationId

Specify the application ID.

```yaml
Type: String
Parameter Sets: SearchByApplicationId
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName

Specify the application name.

```yaml
Type: String
Parameter Sets: SearchByApplicationName
Aliases: ApplicationLocalizedDisplayName

Required: True
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

[New-CMApplicationAutoPhasedDeployment](New-CMApplicationAutoPhasedDeployment.md)
[Remove-CMApplicationPhasedDeployment](Remove-CMApplicationPhasedDeployment.md)
[Set-CMApplicationPhasedDeployment](Set-CMApplicationPhasedDeployment.md)

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)
[Move-CMPhasedDeploymentToNext](Move-CMPhasedDeploymentToNext.md)
[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)
[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence?toc=/mem/configmgr/apps/toc.json&bc=/mem/configmgr/apps/breadcrumb/toc.json)
