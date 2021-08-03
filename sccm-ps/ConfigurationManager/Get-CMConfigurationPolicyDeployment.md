---
description: Get a configuration policy deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Get-CMConfigurationPolicyDeployment
---

# Get-CMConfigurationPolicyDeployment

## SYNOPSIS

Get a configuration policy deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMConfigurationPolicyDeployment [-Fast] [-Name <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMConfigurationPolicyDeployment [-Fast] [-DeploymentId <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMConfigurationPolicyDeployment [-Fast] [-InputObject <IResultObject>] [-Summary]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMConfigurationPolicyDeployment [-Fast] [-SmsObjectId <Int32>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more deployments for a configuration policy. These policies include the following types:

- User Data and Profiles
- OneDrive for Business profiles
- Remote Connection profiles
- Company Resource Access
- Microsoft Edge Browser profiles

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: List all configuration policy deployments

This command returns all configuration policy deployments and displays only the name and ID.

```powershell
Get-CMConfigurationPolicyDeployment -Fast | Select-Object AssignmentName,AssignmentID
```

### Example 2: Get all deployments for a configuration policy

```powershell
$policy = Get-CMConfigurationPolicy -Name "ODfB policy" -Fast

Get-CMConfigurationPolicyDeployment -InputObject $policy -Fast | Select-Object TargetCollectionID,StartTime,Enabled
```

## PARAMETERS

### -Collection

Specify a collection object. This collection is the target for the configuration policy deployment. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify a collection ID that's the target for the configuration policy deployment. For example, `XYZ00023`.

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

Specify a collection name that's the target for the configuration policy deployment.

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

Specify the ID of the deployment. This value is a standard GUID, the same as the **Deployment ID** in the console, and the **AssignmentUniqueID** attribute on the returned object.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentUniqueID, ConfigurationPolicyDeploymentID

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

Specify a configuration policy object to get its deployments. To get this object, use the [Get-CMConfigurationPolicy](Get-CMConfigurationPolicy.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: ConfigurationPolicy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a configuration policy to get its deployments.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ConfigurationPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SmsObjectId

Specify the ID of a configuration policy to get its deployments.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, ConfigurationPolicyID

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
### IResultObject[]#SMS_ConfigurationPolicyAssignment
### IResultObject#SMS_ConfigurationPolicyAssignment
## NOTES

## RELATED LINKS

[New-CMConfigurationPolicyDeployment](New-CMConfigurationPolicyDeployment.md)

[Remove-CMConfigurationPolicyDeployment](Remove-CMConfigurationPolicyDeployment.md)

[Set-CMConfigurationPolicyDeployment](Set-CMConfigurationPolicyDeployment.md)

[Get-CMConfigurationPolicy](Get-CMConfigurationPolicy.md)
