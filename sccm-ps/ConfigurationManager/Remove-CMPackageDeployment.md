---
title: Remove-CMPackageDeployment
titleSuffix: Configuration Manager
description: Removes a package deployment from Configuration Manager.
ms.date: 11/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Remove-CMPackageDeployment

## SYNOPSIS

Removes a package deployment from Configuration Manager.

## SYNTAX

### SearchByValue (Default)

```powershell
Remove-CMPackageDeployment [-ProgramName <String>] -InputObject <IResultObject> [-Force]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName

```powershell
Remove-CMPackageDeployment [-Name <String>] [-ProgramName <String>] [-Force] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById

```powershell
Remove-CMPackageDeployment [-ProgramName <String>] [-PackageId <String>] [-Force] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDeploymentId

```powershell
Remove-CMPackageDeployment [-ProgramName <String>] [-DeploymentId <String>] [-Force] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-CMPackageDeployment** cmdlet remove a package deployment from Microsoft System Center Configuration Manager.
A deployment includes a collection of devices or users, a package to deploy, and either a device program name or a standard program name.
To specify which deployment to modify, specify the collection name, package, and program name.
You can specify the package by name or ID, or you can use the [Get-CMPackage](Get-CMPackage.md) cmdlet to get a package object.

## EXAMPLES

### Example 1

```powershell
PS C:\>  
```

## PARAMETERS

### -Collection

Specifies the user collection.

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

Specifies the ID of a device or user collection. 

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

Specifies the name of a user collection.

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentId

Specifies the ID of a package deployment.

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AdvertisementID, PackageDeploymentID

Required: False
Position: Named
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

Specifies a package deployment object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Advertisement, PackageDeployment, Package

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies the name of a package deployment.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: PackageName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId

Specifies the ID of a package.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProgramName

Specifies the name of a program.

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

### -WhatIf

Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

## RELATED LINKS

- [New-CMPackageDeployment](New-CMPackageDeployment.md)
- [Start-CMPackageDeployment](Start-CMPackageDeployment.md)
- [Get-CMPackageDeployment](Get-CMPackageDeployment.md)
- [Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)
- [Set-CMPackageDeployment](Set-CMPackageDeployment.md)
- [Get-CMPackage](Get-CMPackage.md)