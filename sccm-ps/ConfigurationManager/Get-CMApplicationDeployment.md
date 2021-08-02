---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/29/2021
schema: 2.0.0
title: Get-CMApplicationDeployment
---

# Get-CMApplicationDeployment

## SYNOPSIS

Get an application deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMApplicationDeployment [-Name <String>] [-Summary] [-Collection <IResultObject>] [-CollectionId <String>]
 [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMApplicationDeployment [-DeploymentId <String>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationDeployment [-InputObject <IResultObject>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMApplicationDeployment [-SmsObjectId <Int32>] [-Summary] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get an object for an application deployment. You can use this object to configure or remove the deployment.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all deployments for an application

```powershell
Get-CMApplicationDeployment -Name 'WebView2 Redist (x64)'
```

### Example 2: Get a specific deployment by name

```powershell
Get-CMApplicationDeployment -Name 'Configuration Manager console' -CollectionName 'CM admins'
```

## PARAMETERS

### -Collection

Specify a collection object to which the application is deployed. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

Specify the ID of the collection to which the application is deployed. This value is a standard collection ID, for example, `XYZ00034`.

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

Specify the name of the collection to which the collection is deployed.

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

Specify the deployment ID to get. This value is a GUID. It's the **Deployment ID** value in the console and the **AssignmentUniqueID** property of the **SMS_ApplicationAssignment** WMI class.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentUniqueID, ApplicationDeploymentID

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

Specify an application object to get its deployments. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Application

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of an application to get its deployments.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ApplicationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SmsObjectId

Specify the **CI_ID** of the application to get its deployments. This value is the **CI Unique ID** in the console, the **AssignedCI_UniqueID** property of the **SMS_ApplicationAssignment** WMI class, and the **CI_UniqueID** property of the **SMS_Application** WMI class. For example, the format is like `ScopeId_0D7D8B60-F2F9-484A-B9F3-4A8B68D14D59/Application_70659c7c-694b-4563-965f-d82537a1de1b/2`.

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, ApplicationID

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
### IResultObject[]#SMS_ApplicationAssignment
### IResultObject#SMS_ApplicationAssignment
## NOTES

For more information on these return objects and their properties, see the following articles:

- [SMS_DeploymentSummary server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymentsummary-server-wmi-class)

- [SMS_ApplicationAssignment server WMI class](/mem/configmgr/develop/reference/apps/sms_applicationassignment-server-wmi-class)

## RELATED LINKS

[New-CMApplicationDeployment](New-CMApplicationDeployment.md)

[Remove-CMApplicationDeployment](Remove-CMApplicationDeployment.md)

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)
