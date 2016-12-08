---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833829
schema: 2.0.0
ms.assetid: 60B0C10A-9997-40B0-87A3-5E0ABE5D0908
---

# Set-CMDriverPackage

## SYNOPSIS
Modifies a driver package

## SYNTAX

### SetByValueMandatory (Default)
```
Set-CMDriverPackage -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-Version <String>] [-DriverPackageSource <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMDriverPackage -Id <String> [-NewName <String>] [-Description <String>] [-Version <String>]
 [-DriverPackageSource <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMDriverPackage -Name <String> [-NewName <String>] [-Description <String>] [-Version <String>]
 [-DriverPackageSource <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMDriverPackage** cmdlet modifies a driver package in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Add a security scope action to a driver package
```
PS C:\> Set-CMDriverPackage -SecurityScopeAction AddMembership -SecurityScopeName "Scope 001" -Name "Windows 7 Standard Hardware Package"
```

This command adds a security scope action to the driver package that is named Windows 7 Standard Hardware Package.

### Example 2: Remove a security scope action from a driver package
```
PS C:\> Set-CMDriverPackage -SecurityScopeAction RemoveMembership -SecurityScopeName "Scope 001" -Name "Windows 7 Standard Hardware Package"
```

This command removes a security scope action from the driver package that is named Windows 7 Standard Hardware Package.

## PARAMETERS

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
Indicates that wildcard handling is disabled.

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
Indicates that wildcard handling is enabled.

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
To obtain a driver package object, use the [Get-CMDriverPackage](./Get-CMDriverPackage.md) cmdlet.

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
Returns an object representing the item with which you are working.
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

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Export-CMDriverPackage](./Export-CMDriverPackage.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)

[Import-CMDriverPackage](./Import-CMDriverPackage.md)

[New-CMDriverPackage](./New-CMDriverPackage.md)

[Remove-CMDriverPackage](./Remove-CMDriverPackage.md)
