---
description: Get a Configuration Manager deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/07/2020
schema: 2.0.0
title: Get-CMDeployment
---

# Get-CMDeployment

## SYNOPSIS

Get a Configuration Manager deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMDeployment [-CollectionName <String>] [-FeatureType <DeploymentFeature>] [-ProgramName <String>]
 [-SoftwareName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeployment -DeploymentId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

**The Get-CMDeployment** cmdlet gets one or more Configuration Manager deployments. The cmdlet gets summary information about deployments of applications, software updates, or classic programs.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a deployment for a collection

This command gets the application deployment for the device collection named **deviceCol1**.

```powershell
Get-CMDeployment -CollectionName "deviceCol1" -FeatureType "Application"
```

## PARAMETERS

### -CollectionName

Specifies the name of the collection associated with the deployment.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -DeploymentId

Specifies the ID of a deployment.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

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

### -FeatureType

Specifies the feature type of the deployment.

```yaml
Type: DeploymentFeature
Parameter Sets: SearchByName
Aliases:
Accepted values: Application, Package, SoftwareUpdate, ConfigurationItem, TaskSequence, FirewallSetting, ApplicationGroup

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

### -ProgramName

Specifies the name of the program associated with the deployment. Use this parameter with a legacy distribution program.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SoftwareName

Specifies the name of the software associated with the deployment. Use this parameter with a software update.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_DeploymentSummary
### IResultObject#SMS_DeploymentSummary
## NOTES

## RELATED LINKS

[Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Remove-CMDeployment](Remove-CMDeployment.md)

[Set-CMDeploymentType](Set-CMDeploymentType.md)
