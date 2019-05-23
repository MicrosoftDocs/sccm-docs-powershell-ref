---
title: Get-CMPackageDeploymentStatus
titleSuffix: Configuration Manager
description: Gets the status of classic software distribution deployments.
ms.date: 11/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Get-CMPackageDeploymentStatus

## SYNOPSIS

Gets the status of classic software distribution deployments.

## SYNTAX

### SearchByName (Default)

```powershell
Get-CMPackageDeploymentStatus [-Name <String>] [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDeploymentId

```powershell
Get-CMPackageDeploymentStatus -DeploymentId <String> [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPackageId

```powershell
Get-CMPackageDeploymentStatus -PackageId <String> [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue

```powershell
Get-CMPackageDeploymentStatus [-StatusType <PackageDeploymentStatusType>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMPackageDeploymentStatus** cmdlet gets the status of one or more classic software distribution deployments.
A classic software distribution is a legacy software distribution program on a client.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1

```powershell
PS XYZ:\> Get-CMPackageDeploymentStatus -Name "Depack01"
```

This command gets the status of a deployment that is distributed to Configuration Manager clients by using the deployment package named Depack01.

## PARAMETERS

### -DeploymentId

Specifies the ID of a deployment

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: Id

Required: True
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

Specifies a deployment package.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Package, Advertisement, Deployment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies the name of a package.

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
Parameter Sets: SearchByPackageId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusType

Specifies a status type.

```yaml
Type: PackageDeploymentStatusType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Success, InProgress, RequirementsNotMet, Unknown, Error

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

[New-CMPackageDeployment](New-CMPackageDeployment.md)
[Start-CMPackageDeployment](Start-CMPackageDeployment.md)
[Get-CMPackageDeployment](Get-CMPackageDeployment.md)
[Set-CMPackageDeployment](Set-CMPackageDeployment.md)
[Remove-CMPackageDeployment](Remove-CMPackageDeployment.md)
[Get-CMPackage](Get-CMPackage.md)
[Invoke-CMDeploymentSummarization](Invoke-CMDeploymentSummarization.md)
[Remove-CMDeployment](Remove-CMDeployment.md)
