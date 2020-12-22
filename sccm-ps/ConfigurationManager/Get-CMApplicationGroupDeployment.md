---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2020
online version:
schema: 2.0.0
---

# Get-CMApplicationGroupDeployment

## SYNOPSIS

Get the deployment of an application group.

## SYNTAX

### SearchByName (Default)
```
Get-CMApplicationGroupDeployment [-Name <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMApplicationGroupDeployment [-DeploymentId <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationGroupDeployment [-InputObject <IResultObject>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMApplicationGroupDeployment [-SmsObjectId <Int32>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Get the deployment of an application group. An app group contains multiple applications, and users see the group in Software Center as a single entity. For more information, see [Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups).

## EXAMPLES

### Example 1: Get an app group by ID

```powershell
Get-CMApplicationGroupDeployment -SmsObjectId "16777536"
```

### Example 2: Get an app group by deployment ID

```powershell
Get-CMApplicationGroupDeployment -DeploymentId "{483392DD-92BF-4CFD-9E21-2BB5F3C01BCD}"
```

## PARAMETERS

### -Collection

Specify a collection object to which the app group is deployed. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify the ID of the collection to which the app group is deployed. The format is `SMS00001` for example.

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

Specify the name of the collection to which the app group is deployed.

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

### -DeploymentId

Specify the ID for the app group deployment. The format of this ID is a standard GUID.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentID, ApplicationGroupDeploymentID

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

Specify an object for the app group.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: ApplicationGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name for the app group.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ApplicationGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SmsObjectId

Specify the ID of the application group.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, ApplicationGroupID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Summary

Add this parameter to show a summary for the deployment. This summary includes the number of devices targeted, in progress, success, and errors.

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

For more information on this return object and its properties, see [SMS_DeploymentSummary server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class).

### IResultObject[]#SMS_ApplicationGroupAssignment

### IResultObject#SMS_ApplicationGroupAssignment

## NOTES

## RELATED LINKS

[New-CMApplicationGroupDeployment](New-CMApplicationGroupDeployment.md)

[Remove-CMApplicationGroupDeployment](Remove-CMApplicationGroupDeployment.md)

[Set-CMApplicationGroupDeployment](Set-CMApplicationGroupDeployment.md)

[Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups)
