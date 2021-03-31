---
description: Removes a deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMDeployment
---

# Remove-CMDeployment

## SYNOPSIS
Removes a deployment.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMDeployment [-Force] -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMDeployment -ApplicationName <String> -DeploymentId <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMDeployment -ApplicationName <String> -CollectionName <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDeployment** cmdlet removes an application deployment from Configuration Manager.

When you remove an application deployment, Configuration Manager does not remove instances of the application that it has already installed.
To remove these applications, you must deploy the application to computers with the action Uninstall.
If you delete an application deployment, or remove a resource from the collection you are deploying to, the application will no longer be visible in Software Center or the Application Catalog.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove an application deployment
```
PS XYZ:\> Remove-CMDeployment -ApplicationName "CMappD01" -CollectionName "All Users"
```

This command removes the Configuration Manager deployment that is associated with the application named CMappD01 and that is applied to the collection named All Users.

### Example 2: Pass a deployment object and remove it
```
PS XYZ:\> Get-CMDeployment -CollectionName "deviceCol01" -FeatureType Application | Remove-CMDeployment -Force
```

This command gets the specified application deployment object for the collection named deiceCol01 and uses the pipeline operator to pass the object to **Remove-CMDeployment**, which removes the deployment.
Because the *Force* parameter is specified, the user is not prompted before the deployment is removed.

### Example 3: Remove a deployment by its ID
```
PS XYZ:\> Remove-CMDeployment -DeploymentId "{890082B6-7C16-4600-8807-7E0003BC9D99}" -ApplicationName "application01" -Force
```

This command removes the deployment named application01 with the specified ID.
Because the *Force* parameter is specified, the user is not prompted before the deployment is removed.

## PARAMETERS

### -ApplicationName
Specifies the name of the application associated with the deployment.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory, SearchByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of the collection associated with the deployment.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

### -Force
Performs the action without a confirmation message.

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
Specifies a deployment object.
To obtain a deployment object, use the Get-CMDeployment cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Deployment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
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

[Get-CMDeployment](Get-CMDeployment.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Remove-CMDeploymentType](Remove-CMDeploymentType.md)


