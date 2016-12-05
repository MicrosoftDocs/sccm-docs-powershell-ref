---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833963
schema: 2.0.0
ms.assetid: B08C17F1-A997-4352-A9C2-6757E0D19C3A
---

# Set-CMOperatingSystemInstaller

## SYNOPSIS
Changes configuration settings of operating system installers.

## SYNTAX

### SetById (Default)
```
Set-CMOperatingSystemInstaller -Id <String> [-NewName <String>] [-Path <String>] [-Version <String>]
 [-Description <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMOperatingSystemInstaller -Name <String> [-NewName <String>] [-Path <String>] [-Version <String>]
 [-Description <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMOperatingSystemInstaller -InputObject <IResultObject> [-NewName <String>] [-Path <String>]
 [-Version <String>] [-Description <String>] [-DistributionPointUpdateSchedule <IResultObject>]
 [-DisconnectUserFromDistributionPoint <Boolean>] [-DisconnectUserFromDistributionPointRetryCount <UInt32>]
 [-DisconnectUserFromDistributionPointMins <UInt32>] [-CustomPackageShareName <String>]
 [-CopyToPackageShareOnDistributionPoint <Boolean>] [-MulticastAllow <Boolean>] [-MulticastEncrypt <Boolean>]
 [-MulticastTransferOnly <Boolean>] [-Priority <Priority>] [-SendToPreferredDistributionPoint <Boolean>]
 [-PrestageBehavior <PrestageBehavior>] [-PersistContentInCache <Boolean>]
 [-EnableBinaryDeltaReplication <Boolean>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMOperatingSystemInstaller** cmdlet changes configuration settings of one or more operating system installers in Microsoft System Center Configuration Manager.
An operating system installer is an installation package that contains all the files that System Center Configuration Manager needs to install a Windows operating system on a reference computer.

## EXAMPLES

### Example 1: Change settings for an operating system installer by using a name
```
PS C:\>Set-CMOperatingSystemInstaller -Name "Win8x64" -NewName "OsiWin8x64" -Version "I20B" -Description "Dept02 Sys Install" -Path "\\Win2k3X64contoso\Public\OSD\win8x64"
```

This command changes configuration settings of the operating system installer named Win8x64.
The command renames the operating system installer, adds a version and description, and specifies the path to the installation source files of the operating system installer.

### Example 2: Add an operating system installer to a security scope by using a name
```
PS C:\>Set-CMOperatingSystemInstaller -SecurityScopeAction AddMembership -SecurityScopeName "SecScope02" -Name "InstPkg01"
```

This command adds membership to the security scope named SecScope02 for the operating system installer named InstPkg01.

### Example 3: Remove an operating system installer from a security scope
```
PS C:\>Set-CMOperatingSystemInstaller -SecurityScopeAction RemoveMembership -SecurityScopeName "SecScope02" -Name "InstPkg01"
```

This command removes membership to the security scope named SecScope02 for the operating system installer named InstPkg01.

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
Specifies a description for the operating system installer.

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
Specifies an array of IDs of operating system installers.

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
Specifies a CMOperatingSystemInstaller object.
To obtain a CMOperatingSystemInstaller object, use the Get-CMOperatingSystemInstaller cmdlet.

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
Specifies the name of an operating system installer.

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
Specifies the new name of an operating system installer.

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
Specifies the network path to the installation source files of an operating system installer.

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
Specifies the version of an operating system installer.

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

[Get-CMOperatingSystemInstaller](./Get-CMOperatingSystemInstaller.md)

[New-CMOperatingSystemInstaller](./New-CMOperatingSystemInstaller.md)

[Remove-CMOperatingSystemInstaller](./Remove-CMOperatingSystemInstaller.md)


