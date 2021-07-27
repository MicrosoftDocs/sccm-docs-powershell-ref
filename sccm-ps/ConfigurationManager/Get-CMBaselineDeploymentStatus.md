---
description: Get the status of a configuration baseline deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/23/2021
schema: 2.0.0
title: Get-CMBaselineDeploymentStatus
---

# Get-CMBaselineDeploymentStatus

## SYNOPSIS

Get the status of a configuration baseline deployment.

## SYNTAX

```
Get-CMBaselineDeploymentStatus [-Fast] -InputObject <IResultObject>
 [-StatusType <BaselineDeploymentStatusType>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the status of a configuration baseline deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Show all compliant deployments for a specific configuration baseline

```powershell
$baseline = Get-CMBaseline -Name "Check Windows health" -Fast
Get-CMBaselineDeploymentStatus -StatusType Compliant -InputObject $baseline
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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -InputObject

Specify an object for a configuration baseline. To get this object, use the [Get-CMBaseline](Get-CMBaseline.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Baseline, Assignment, Deployment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -StatusType

Specify a compliance state. For example, to only return compliant deployments, add `-StatusType Compliant`.

```yaml
Type: BaselineDeploymentStatusType
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, NonCompliant, Error, Compliant

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

[Get-CMBaseline](Get-CMBaseline.md)

[Get-CMBaselineDeployment](Get-CMBaselineDeployment.md)

[New-CMBaselineDeployment](New-CMBaselineDeployment.md)
