---
description: Retrieves a deployment package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMSoftwareUpdateDeploymentPackage
---

# Get-CMSoftwareUpdateDeploymentPackage

## SYNOPSIS
Retrieves a deployment package.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateDeploymentPackage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateDeploymentPackage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateDeploymentPackage** cmdlet retrieves a deployment package for a software update.
A **CMSoftwareUpdateDeploymentPackage** object contains one or more software updates.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a deployment package by using a name
```
PS XYZ:\> Get-CMSoftwareUpdateDeploymentPackage -Name "Asdset"
```

This command gets a deployment package named Asdset.

### Example 2: Get a deployment package by using an ID
```
PS XYZ:\> Get-CMSoftwareUpdateDeploymentPackage -Id "ST10000C"
```

This command gets a deployment package that has the ID ST10000C.

## PARAMETERS

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

### -Id
Specifies an array of IDs for the deployment package.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the deployment package.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_SoftwareUpdatesPackage
### IResultObject#SMS_SoftwareUpdatesPackage
## NOTES

## RELATED LINKS

[Remove-CMSoftwareUpdateDeploymentPackage](Remove-CMSoftwareUpdateDeploymentPackage.md)

[Set-CMSoftwareUpdateDeploymentPackage](Set-CMSoftwareUpdateDeploymentPackage.md)


