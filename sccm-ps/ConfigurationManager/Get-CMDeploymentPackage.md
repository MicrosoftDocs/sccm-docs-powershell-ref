---
description: Gets information about deployment packages on a distribution point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMDeploymentPackage
---

# Get-CMDeploymentPackage

## SYNOPSIS
Gets information about deployment packages on a distribution point.

## SYNTAX

```
Get-CMDeploymentPackage [-DeploymentPackageName <String>] -DistributionPointName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeploymentPackage** cmdlet gets information about one or more deployment packages on a distribution point.
If you do not specify the *DeploymentPackageName* parameter, Configuration Manager returns all the deployment packages on the distribution point that you specify.

A deployment package is a Configuration Manager object that contains the content files and instructions for distributing programs, software updates, boot images, operating system images, and drivers to Configuration Manager clients.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all deployment packages for a distribution point
```
PS XYZ:\> Get-CMDeploymentPackage -DistributionPointName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM"
```

This command gets all deployment packages that are distributed to clients from the distribution point named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM.

### Example 2: Get a deployment package for a distribution point
```
PS XYZ:\> Get-CMDeploymentPackage -DistributionPointName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM" -DeploymentPackageName "Depack01"
```

This command gets the deployment package named Depack01 that is distributed to clients from the distribution point named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM.

## PARAMETERS

### -DeploymentPackageName
Specifies an array of names of deployment packages. If you do not specify this parameter, the cmdlet returns status information about all deployment packages on the distribution point.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

### -DistributionPointName
Specifies an array of names of distribution points that are associated with deployment packages.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_DPContentInfo
### IResultObject#SMS_DPContentInfo
## NOTES

## RELATED LINKS

[Get-CMDeployment](Get-CMDeployment.md)

[Get-CMPackageDeploymentStatus](Get-CMPackageDeploymentStatus.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Invoke-CMDeploymentSummarization](Invoke-CMDeploymentSummarization.md)
