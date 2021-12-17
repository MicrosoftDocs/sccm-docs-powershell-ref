---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
schema: 2.0.0
title: Get-CMDeploymentType
---

# Get-CMDeploymentType

## SYNOPSIS

Get a deployment type for an application.

## SYNTAX

### SearchByName (Default)
```
Get-CMDeploymentType -ApplicationName <String> [-DeploymentTypeName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeploymentType -ApplicationName <String> -DeploymentTypeId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDTValue
```
Get-CMDeploymentType [-DeploymentTypeName <String>] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a deployment type for a Configuration Manager application.

A deployment type is contained within an application and contains the information that Configuration Manager requires to install software.
A deployment type also contains rules that specify if and how the software is deployed.

For more information, see [Introduction to application management in Configuration Manager](/mem/configmgr/apps/understand/introduction-to-application-management).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all deployment types for an application

This command gets all of the deployment types for the application named **CenterApp**.

```powershell
Get-CMDeploymentType -ApplicationName "CenterApp"
```

### Example 2: Get a specific deployment type by name

This command gets the deployment type named **InterDept - Windows app package (.appx file)** for the application named **CenterApp**.

```powershell
Get-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows app package (.appx file)"
```

## PARAMETERS

### -ApplicationName

Specify the name of the application for the deployment type.

```yaml
Type: String
Parameter Sets: SearchByName, SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeId

Specify the ID of a deployment type to get. This value is the **CI_ID**, for example: `33554475`.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeName

Specify the name of a deployment type to get.

```yaml
Type: String
Parameter Sets: SearchByName, SearchByDTValue
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

Specify an application object to get its deployment types. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByDTValue
Aliases: Application

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_DeploymentType

### IResultObject#SMS_DeploymentType

## NOTES

For more information on this return object and its properties, see [SMS_DeploymentType server WMI class](/mem/configmgr/develop/reference/apps/sms_deploymenttype-server-wmi-class).

## RELATED LINKS

[Convert-CMDeploymentType](Convert-CMDeploymentType.md)

[Remove-CMDeploymentType](Remove-CMDeploymentType.md)

[Set-CMDeploymentType](Set-CMDeploymentType.md)

[Get-CMDeploymentTypeRequirement](Get-CMDeploymentTypeRequirement.md)
