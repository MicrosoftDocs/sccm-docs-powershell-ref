---
title: Remove-CMDeploymentType
titleSuffix: Configuration Manager
description: Removes a deployment type for a Configuration Manager deployment application.
ms.date: 11/15/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Remove-CMDeploymentType

## SYNOPSIS

Removes a deployment type for a Configuration Manager deployment application.

## SYNTAX

### SearchByInputObjectMandatory (Default)

```powershell
Remove-CMDeploymentType [-Force] [-ApplicationName <String>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory

```powershell
Remove-CMDeploymentType -DeploymentTypeId <Int32> [-Force] -ApplicationName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory

```powershell
Remove-CMDeploymentType [-DeploymentTypeName] <String> [-Force] -ApplicationName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-CMDeploymentType** cmdlet removes a deployment type in Microsoft System Center Configuration Manager.
You cannot remove a deployment type if it is referenced by a deployment type in another application.

To remove a deployment type, you must remove any dependencies to the deployment type in other deployment types.
Additionally, you must remove previous revisions of any application that contains a deployment type that references the deployment type that you want to remove.
If you have already deployed the application, you cannot remove the last deployment type that the application contains, and the application must be in an active state.

## EXAMPLES

### Example 1: Remove a deployment type

```powershell
PS C:\> Remove-CMDeploymentType -ApplicationName "CenterApp" -DeploymentTypeName "InterDept - Windows app package (.appx file)"
```

This command removes the deployment type named InterDept - Windows app package (.appx file) that is contained in the application named CenterApp.

## PARAMETERS

### -ApplicationName

Specifies the name of an application that is associated to the deployment type.

```yaml
Type: String
Parameter Sets: SearchByInputObjectMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -DeploymentTypeId

Specifies the ID of a deployment type.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID, Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentTypeName

Specifies the name of a deployment type.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

Forces the command to run without asking for user confirmation.

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

ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: SearchByInputObjectMandatory
Aliases: DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

* [Add-CMDeploymentType](Add-CMDeploymentType.md)
* [Get-CMDeployment](Get-CMDeployment.md)
* [Get-CMDeploymentType](Get-CMDeploymentType.md)
* [Set-CMDeploymentType](Set-CMDeploymentType.md)
