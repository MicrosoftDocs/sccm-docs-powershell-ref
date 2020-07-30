---
description: Gets a package deployment from Configuration Manager.
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/30/2018
schema: 2.0.0
title: Get-CMPackageDeployment
---

# Get-CMPackageDeployment

## SYNOPSIS

Gets a package deployment from Configuration Manager.

## SYNTAX

### SearchByName (Default)
```
Get-CMPackageDeployment [-Name <String>] [-ProgramName <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMPackageDeployment [-ProgramName <String>] [-PackageId <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMPackageDeployment [-ProgramName <String>] [-DeploymentId <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMPackageDeployment [-ProgramName <String>] [-InputObject <IResultObject>] [-Summary]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMPackageDeployment** cmdlet starts deployment of a specified software package to computers that belong to a Configuration Manager collection.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1

```powershell
PS XYZ:\> Get-CMPackageDeployment -PackageId $thisPackage.packageid
```

This command gets a package deployment by the package id.

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

### -DeploymentId

Specifies the ID of a deployment.

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

Specifies a package.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Package

Required: False
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
Parameter Sets: SearchById
Aliases: SmsObjectId

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

### -Summary

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_DeploymentSummary

### IResultObject#SMS_DeploymentSummary

### IResultObject[]#SMS_Advertisement

### IResultObject#SMS_Advertisement

## NOTES

## RELATED LINKS

[New-CMPackageDeployment](New-CMPackageDeployment.md)
[Start-CMPackageDeployment](Start-CMPackageDeployment.md)
[Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)
[Set-CMPackageDeployment](Set-CMPackageDeployment.md)
[Remove-CMPackageDeployment](Remove-CMPackageDeployment.md)
[Get-CMPackage](Get-CMPackage.md)
