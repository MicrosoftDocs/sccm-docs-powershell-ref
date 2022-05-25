---
description: Get a software update deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/07/2020
schema: 2.0.0
title: Get-CMSoftwareUpdateDeployment
---

# Get-CMSoftwareUpdateDeployment

## SYNOPSIS

Get a software update deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateDeployment [-Name <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMSoftwareUpdateDeployment [-DeploymentId <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMSoftwareUpdateDeployment [-InputObject <IResultObject>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMSoftwareUpdateDeployment [-SmsObjectId <Int32>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMSoftwareUpdateDeployment** cmdlet gets a software update deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Display deployment status for a Patch Tuesday deployment

This example uses the **Get-CMSoftwareUpdateDeployment** cmdlet to get a software update deployment object. That object is then used as the input to show the status.

```powershell
$sudeploy = Get-CMSoftwareUpdateDeployment -Name "Patch Tuesday - Office and Edge 2020-07-15 00:11:11"

Get-CMSoftwareUpdateDeploymentStatus -InputObject $sudeploy
```

## PARAMETERS

### -Collection

Specify a collection object for the software update deployment.

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

Specify a collection by ID for the software update deployment.

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

Specify a collection by name for the software update deployment.

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

Specify the deployment ID to get. The format is a GUID.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentUniqueID, SoftwareUpdateDeploymentID

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

### -InputObject

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: SoftwareUpdate

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the software update deployment to get.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: SoftwareUpdateName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SmsObjectId

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, SoftwareUpdateID

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
### IResultObject[]#SMS_UpdateAssignment
### IResultObject#SMS_UpdateAssignment
## NOTES

For more information on these return objects and their properties, see the following articles:

- [SMS_DeploymentSummary server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class)
- [SMS_UpdateAssignment server WMI class](/mem/configmgr/develop/reference/sum/sms_updatesassignment-server-wmi-class)

## RELATED LINKS

[Get-CMSoftwareUpdateDeploymentStatus](Get-CMSoftwareUpdateDeploymentStatus.md)
