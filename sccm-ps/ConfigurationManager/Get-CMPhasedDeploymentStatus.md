---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
online version:
schema: 2.0.0
---

# Get-CMPhasedDeploymentStatus

## SYNOPSIS

Get the status of a specific phased deployment.

## SYNTAX

### SearchByValue
```
Get-CMPhasedDeploymentStatus -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMPhasedDeploymentStatus -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMPhasedDeploymentStatus -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the status of a specific phased deployment.

For more information, see [Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).


## EXAMPLES

### Example 1: Get status by the deployment name

This example displays the status of a phased deployment based on its name.

```powershell
Get-CMPhasedDeploymentStatus -Name "myPhasedDeploymentName"
```

### Example 2: Get status of a variable deployment object

This example displays the status of a phased deployment object that's saved into a variable.

```powershell
$myPhasedDeployment | Get-CMPhasedDeploymentStatus
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

### -InputObject

Specify a phased deployment object.

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

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.Deployments.PhasedDeploymentInfo
## NOTES

## RELATED LINKS

[Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence)
