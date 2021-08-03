---
description: Get a task sequence deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Get-CMTaskSequenceDeployment
---

# Get-CMTaskSequenceDeployment

## SYNOPSIS

Get a task sequence deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMTaskSequenceDeployment [-Fast] [-Name <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMTaskSequenceDeployment [-Fast] [-DeploymentId <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMTaskSequenceDeployment [-Fast] [-InputObject <IResultObject>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMTaskSequenceDeployment [-Fast] [-TaskSequenceId <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a task sequence deployment. A task sequence deployment assigns a task sequence to a collection of computers. For more information, see [Deploy a task sequence in Configuration Manager](/mem/configmgr/osd/deploy-use/deploy-a-task-sequence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all deployments for a task sequence by name

This command gets the deployments for the task sequence named **Upgrade to Windows 10 latest**.

```powershell
Get-CMTaskSequenceDeployment -Name "Upgrade to Windows 10 latest"
```

### Example 2: Get all task sequence deployments to a specific collection

This command gets all task sequence deployments to the collection with ID **XYZ00112**

```powershell
Get-CMTaskSequenceDeployment -Fast -CollectionId "XYZ00112"
```

## PARAMETERS

### -Collection

Specify a collection object to which a task sequence is deployed. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify a collection ID to which a task sequence is deployed. This value is a standard collection ID, for example, `XYZ00581`.

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

Specify a collection name to which a task sequence is deployed.

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

Specify the ID for the deployment. This value is a standard ID, for example, `XYZ20174`. It's the same value as the **Deployment ID** property in the console, and the **AdvertisementID** attribute of the SMS_Advertisement WMI class that this cmdlet returns.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AdvertisementID, TaskSequenceDeploymentID

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

Specify a task sequence object to get its deployments. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: TaskSequence

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of a task sequence to get its deployments.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: TaskSequenceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

### -TaskSequenceId

Specify the ID of a task sequence to get its deployments. This value is a standard ID, for example, `XYZ00279`.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: SmsObjectId, TaskSequencePackageID

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
### IResultObject[]#SMS_Advertisement
### IResultObject#SMS_Advertisement
## NOTES

For more information on these return objects and their properties, see the following articles:

- [SMS_DeploymentSummary server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class)
- [SMS_Advertisement server WMI class](/mem/configmgr/develop/reference/core/servers/configure/sms_advertisement-server-wmi-class)

## RELATED LINKS

[New-CMTaskSequenceDeployment](./New-CMTaskSequenceDeployment.md)
[Set-CMTaskSequenceDeployment](./Set-CMTaskSequenceDeployment.md)
[Remove-CMTaskSequenceDeployment](./Remove-CMTaskSequenceDeployment.md)

[Deploy a task sequence in Configuration Manager](/mem/configmgr/osd/deploy-use/deploy-a-task-sequence)
