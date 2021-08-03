---
description: Get a baseline deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/23/2021
schema: 2.0.0
title: Get-CMBaselineDeployment
---

# Get-CMBaselineDeployment

## SYNOPSIS

Get a baseline deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMBaselineDeployment [-Fast] [-Name <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMBaselineDeployment [-Fast] [-DeploymentId <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMBaselineDeployment [-Fast] [-InputObject <IResultObject>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMBaselineDeployment [-Fast] [-SmsObjectId <Int32>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get the deployments of configuration baselines.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all deployments for a configuration baseline

```powershell
$baseline = Get-CMBaseline -Name "Check Windows health" -Fast

Get-CMBaselineDeployment -InputObject $baseline
```

## PARAMETERS

### -Collection

Specify a collection object. This collection is the target for the baseline deployment. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId

Specify a collection ID that's the target for the baseline deployment. For example, `XYZ00023`.

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

### -CollectionName

Specify a collection name that's the target for the baseline deployment.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -DeploymentId

Specify the ID of the deployment. This value is a standard GUID, the same as the **Deployment ID** in the console.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentUniqueID, BaselineDeploymentID

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

Specify a configuration baseline object to get its deployments. To get this object, use the [Get-CMBaseline](Get-CMBaseline.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Baseline

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a configuration baseline to get its deployments.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: BaselineName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SmsObjectId

Specify the ID of a configuration baseline to get its deployments.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, BaselineID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Summary

Add this parameter to return the [SMS_DeploymentSummary WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class) object.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_DeploymentSummary
### IResultObject#SMS_DeploymentSummary
### IResultObject[]#SMS_BaselineAssignment
### IResultObject#SMS_BaselineAssignment
## NOTES

For more information on these return objects and their properties, see the following articles:

- [SMS_DeploymentSummary server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class)
- [SMS_BaselineAssignment server WMI class](/mem/configmgr/develop/reference/compliance/sms_baselineassignment-server-wmi-class)

## RELATED LINKS

[New-CMBaselineDeployment](New-CMBaselineDeployment.md)

[Remove-CMBaselineDeployment](Remove-CMBaselineDeployment.md)

[Set-CMBaselineDeployment](Set-CMBaselineDeployment.md)

[Get-CMBaseline](Get-CMBaseline.md)

[Get-CMBaselineDeploymentStatus](Get-CMBaselineDeploymentStatus.md)
