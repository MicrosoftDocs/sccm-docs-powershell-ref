---
description: Changes configuration settings for Configuration Manager packages.
external help file: AdminUI.PS.AppModel.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMPackage
---

# Set-CMPackage

## SYNOPSIS
Changes configuration settings for Configuration Manager packages.

## SYNTAX

### SetByValue (Default)
```
Set-CMPackage [-InputObject] <IResultObject> [-NewName <String>] [-Version <String>] [-Manufacturer <String>]
 [-Language <String>] [-Description <String>] [-Path <String>] [-MifFileName <String>] [-MifName <String>]
 [-MifPublisher <String>] [-MifVersion <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetry <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priorities>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMPackage -Id <String> [-NewName <String>] [-Version <String>] [-Manufacturer <String>]
 [-Language <String>] [-Description <String>] [-Path <String>] [-MifFileName <String>] [-MifName <String>]
 [-MifPublisher <String>] [-MifVersion <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetry <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priorities>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMPackage -Name <String> [-NewName <String>] [-Version <String>] [-Manufacturer <String>]
 [-Language <String>] [-Description <String>] [-Path <String>] [-MifFileName <String>] [-MifName <String>]
 [-MifPublisher <String>] [-MifVersion <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetry <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priorities>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMPackage** cmdlet changes configuration settings for Microsoft System Center Configuration Manager packages.

If you set the *MifFileName* parameter, System Center Configuration Manager looks in the %TEMP% directory or the %windir% directory for the installation status Management Information Format (MIF) file that you specified in *MifFileName*.
The installation status indicates whether the program successfully ran.

If System Center Configuration Manager does not find the file, it searches for all MIF files in those directories.
System Center Configuration Manager makes a case-insensitive comparison of the values that you specify for *MifName*, *MifPublisher*, and *MifVersion* to the values that the MIF file specifies.
If System Center Configuration Manager finds a match, it uses the status that the MIF file specifies as the installation status for the program.
If System Center Configuration Manager cannot find a match, or if you do not specify *MifFileName*, System Center Configuration Manager uses the program exit code to set the installation status for the program.
An exit code of zero indicates that the program successfully ran.
Any other values indicate application-specific error codes.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Rename a package and add a description
```
PS XYZ:\> Set-CMPackage -Id "ST120001" -NewName "ScriptsPackage02" -Description "This package deploys scripts that run on a recurring schedule."
```

This command renames the package that has the ID ST120001.
The command changes the name of the package to ScriptsPackage02 and adds a description for the package.

### Example 2: Rename a package by using an object variable
```
PS XYZ:\> $Pkg = Get-CMPackage -Id ST120001
PS XYZ:\> Set-CMPackage -InputObject $Pkg -Newname "ScriptsPackage02" -Description "This package deploys scripts that run on a recurring schedule."
```

The first command gets the package that has the ID ST120001, and stores the results in the $Pkg variable.

The second command changes the name of the package stored in $Pkg to ScriptsPackage02, and adds a description for the package.

## PARAMETERS

### -CopyToPackageShareOnDistributionPoint
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: ShareContent, CopyToPackageShareOnDistributionPoints

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
Aliases: ShareName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the package.
You can use a maximum of 128 characters.

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
Aliases: ForceDisconnectEnabled, DisconnectUsersFromDistributionPoints

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
Aliases: ForcedDisconnectDelay, DisconnectUsersFromDistributionPointsMinutes, DisconnectUserFromDistributionPointsMins, DisconnectUserFromDistributionPointsMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisconnectUserFromDistributionPointRetry
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: ForceDisconnectNumRetries, DisconnectUsersFromDistributionPointsRetries

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

### -EnableBinaryDeltaReplication
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
Specifies an array of package IDs.

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
Specifies a **CMPackage** object.
To obtain a **CMPackage** object, use the [Get-CMPackage](Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Language
Specifies the language version of the package.
You can use a maximum of 32 characters in a format that you choose to use to identify the language version.
Configuration Manager uses the *Language* parameter together with *Manufacturer*, *Name*, and *Version* parameters to identify a package.
For example, you can have an English version and a German version of the same package.

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

### -Manufacturer
Specifies a manufacturer name to help you identify the package.
You can use a maximum of 32 characters.

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

### -MifFileName
Specifies the name of the MIF file that contains the package status.

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

### -MifName
Specifies the name of the MIF file that contains the program status for the package.
The file name extension must be .mif.

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

### -MifPublisher
Specifies the name of the software publisher of the package.

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

### -MifVersion
Specifies the version number of the MIF file.

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
Specifies a package name.

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
Specifies a new name for the package.

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

### -Path
Specifies the location of the files of update contents for the package.

You can specify either a full local path or a Universal Naming Convention (UNC) path.
Make sure that this location contains all the files and subdirectories that the program needs to run, including any scripts.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PersistContentInCache
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
Specifies the priority of the package. The acceptable values for this parameter are:

- Increase
- Decrease

```yaml
Type: Priorities
Parameter Sets: (All)
Aliases: DistributionPriority
Accepted values: High, Normal, Low

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
Specifies a version number for the package.

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

[Export-CMPackage](Export-CMPackage.md)

[Get-CMPackage](Get-CMPackage.md)

[Import-CMPackage](Import-CMPackage.md)

[New-CMPackage](New-CMPackage.md)

[Remove-CMPackage](Remove-CMPackage.md)
