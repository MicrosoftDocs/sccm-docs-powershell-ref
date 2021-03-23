---
description: Modifies a driver package.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMDriverPackage
---

# Set-CMDriverPackage

## SYNOPSIS
Modifies a driver package.

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDriverPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-DriverManufacturer <String>] [-DriverModel <String>]
 [-DriverPackageSource <String>] -InputObject <IResultObject> [-MulticastAllow <Boolean>]
 [-MulticastEncrypt <Boolean>] [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru]
 [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMDriverPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-DriverManufacturer <String>] [-DriverModel <String>]
 [-DriverPackageSource <String>] -Id <String> [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-NewName <String>] [-PassThru] [-PrestageBehavior <PrestageBehavior>]
 [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>] [-Version <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMDriverPackage [-CopyToPackageShareOnDistributionPoint <Boolean>] [-CustomPackageShareName <String>]
 [-Description <String>] [-DisconnectUserFromDistributionPoint <Boolean>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DistributionPointUpdateSchedule <IResultObject>] [-DriverManufacturer <String>] [-DriverModel <String>]
 [-DriverPackageSource <String>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] -Name <String> [-NewName <String>] [-PassThru]
 [-PrestageBehavior <PrestageBehavior>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-Version <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDriverPackage** cmdlet modifies a driver package in Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Add a security scope action to a driver package
```
PS XYZ:\> Set-CMDriverPackage -SecurityScopeAction AddMembership -SecurityScopeName "Scope 001" -Name "Windows 7 Standard Hardware Package"
```

This command adds a security scope action to the driver package that is named Windows 7 Standard Hardware Package.

### Example 2: Remove a security scope action from a driver package
```
PS XYZ:\> Set-CMDriverPackage -SecurityScopeAction RemoveMembership -SecurityScopeName "Scope 001" -Name "Windows 7 Standard Hardware Package"
```

This command removes a security scope action from the driver package that is named Windows 7 Standard Hardware Package.

## PARAMETERS

### -CopyToPackageShareOnDistributionPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CopyToPackageShareOnDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomPackageShareName
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

### -Description
Specifies a description of a driver package.

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

### -DisconnectUserFromDistributionPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointMins
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPointsMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointRetryCount
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: DisconnectUsersFromDistributionPointsRetries

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointUpdateSchedule
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

### -DriverManufacturer
Starting in version 1910, use this parameter to set the manufacturer. Use with the DriverModel parameter. You can use them for managing the driver catalog, and with task sequence pre-caching.

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

### -DriverModel
Starting in version 1910, use this parameter to set the model. Use with the DriverManufacturer parameter. You can use them for managing the driver catalog, and with task sequence pre-caching.


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

### -DriverPackageSource
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

### -Id
Specifies an array of identifiers for a driver package.

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
Specifies a driver package object.
To obtain a driver package object, use the [Get-CMDriverPackage](Get-CMDriverPackage.md) cmdlet.

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

### -MulticastAllow
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MulticastEncrypt
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MulticastTransferOnly
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name of a driver package.

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
Specifies a new name of a driver package.

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -PrestageBehavior
```yaml
Type: PrestageBehavior
Parameter Sets: (All)
Aliases:
Accepted values: ManualCopy, DownloadDelta, OnDemand

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Specifies a change for the priority of the deployment type.
Valid values are: Increase and Decrease.

```yaml
Type: Priority
Parameter Sets: (All)
Aliases:
Accepted values: High, Medium, Low

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SendToPreferredDistributionPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: SendToPreferredDistributionPoints

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies the version of a security scope.

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

[Export-CMDriverPackage](Export-CMDriverPackage.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)

[Import-CMDriverPackage](Import-CMDriverPackage.md)

[New-CMDriverPackage](New-CMDriverPackage.md)

[Remove-CMDriverPackage](Remove-CMDriverPackage.md)
