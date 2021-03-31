---
description: Modifies a software update deployment package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSoftwareUpdateDeploymentPackage
---

# Set-CMSoftwareUpdateDeploymentPackage

## SYNOPSIS
Modifies a software update deployment package.

## SYNTAX

### SetById (Default)
```
Set-CMSoftwareUpdateDeploymentPackage [-Description <String>] [-Force] -Id <String> [-NewName <String>]
 [-PassThru] [-Path <String>] [-Priority <Priorities>] [-RefreshDistributionPoint] [-RemoveExpired]
 [-RemoveSuperseded] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMSoftwareUpdateDeploymentPackage [-Description <String>] [-Force] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-Path <String>] [-Priority <Priorities>] [-RefreshDistributionPoint]
 [-RemoveExpired] [-RemoveSuperseded] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareUpdateDeploymentPackage [-Description <String>] [-Force] -Name <String> [-NewName <String>]
 [-PassThru] [-Path <String>] [-Priority <Priorities>] [-RefreshDistributionPoint] [-RemoveExpired]
 [-RemoveSuperseded] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdateDeploymentPackage** cmdlet modifies a software update deployment package.
A software update deployment package contains one or more software updates for deployment to a collection of computers.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Update the name and description of a software update deployment package
```
PS XYZ:\> Set-CMSoftwareUpdateDeploymentPackage -Id "ST10000C" -Description "Deployment pack 107" -NewName "SDPTest"
```

This command sets a new name and description for the deployment package that has the ID ST10000C.

### Example 2: Add membership to a security scope of a software update deployment package
```
PS XYZ:\> Set-CMSoftwareUpdateDeploymentPackage -Name "DP107" -SecurityScopeAction AddMembership -SecurityScopeName "testScopeName"
```

This command adds membership for the security scope named testScopeName.

### Example 3: Remove membership from a security scope of a software update deployment package
```
PS XYZ:\> Set-CMSoftwareUpdateDeploymentPackage -Name "DP107" -SecurityScopeAction RemoveMembership -SecurityScopeName "testScopeName"
```

This command removes membership for the security scope named testScopeName.

## PARAMETERS

### -Description
Specifies a description for the deployment package.

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
Starting in version 1910, use this parameter to force remove an expired NAP update.

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
Specifies an array of identifiers for the deployment package.

```yaml
Type: String
Parameter Sets: SetById
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMSoftwareUpdateDeploymentPackage** object.
To obtain an **CMSoftwareUpdateDeploymentPackage** object, use the [Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for the deployment package.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the deployment package.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Path
Specifies a package source (URL) for the deployment package.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath, PkgSourcePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Specifies a distribution priority for the deployment package.

```yaml
Type: Priorities
Parameter Sets: (All)
Aliases:
Accepted values: High, Normal, Low

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshDistributionPoint
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RefreshDistributionPointAfterRemoveSoftwareUpdateFromPackage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveExpired
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RemoveDownloadedExpiredSoftwareUpdateFromPackage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSuperseded
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RemoveDownloadedSupersededSoftwareUpdateFromPackage

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)

[Remove-CMSoftwareUpdateDeploymentPackage](Remove-CMSoftwareUpdateDeploymentPackage.md)
