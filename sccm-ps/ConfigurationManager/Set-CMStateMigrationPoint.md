---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 530F83FB-CCDC-4B2A-AE45-250D828201A9
online version: https://go.microsoft.com/fwlink/?linkid=834102
schema: 2.0.0
---

# Set-CMStateMigrationPoint

## SYNOPSIS
Modifies settings for a state migration point in Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMStateMigrationPoint [-AddStorageFolder <StorageDirectoryData[]>]
 [-RemoveStorageFolder <StorageDirectoryData[]>] [-DeleteImmediately] [-TimeDeleteAfter <Int32>]
 [-TimeUnit <IntervalType>] [-EnableRestoreOnlyMode <Boolean>]
 [-AllowFallbackSourceLocationForContent <Boolean>] [-AddBoundaryGroupName <String[]>]
 [-RemoveBoundaryGroupName <String[]>] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMStateMigrationPoint [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-AddStorageFolder <StorageDirectoryData[]>] [-RemoveStorageFolder <StorageDirectoryData[]>]
 [-DeleteImmediately] [-TimeDeleteAfter <Int32>] [-TimeUnit <IntervalType>] [-EnableRestoreOnlyMode <Boolean>]
 [-AllowFallbackSourceLocationForContent <Boolean>] [-AddBoundaryGroupName <String[]>]
 [-RemoveBoundaryGroupName <String[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStateMigrationPoint** cmdlet modifies settings for a state migration point in Microsoft System Center Configuration Manager.
A state migration point is a site system role that manages data transfer from client computers during an operating system installation process.
Use this cmdlet to modify the boundary groups and storage folders associated with the migration point, how long to wait before the migration point deletes client data, whether to allow a fallback source location for content, and whether to enable restore only mode.

You can specify which migration point to modify by using the site system server name and the site code, or use the [Get-CMStateMigrationPoint](Get-CMStateMigrationPoint.md) cmdlet.

## EXAMPLES

### Example 1: Modify a state migration point
```
PS C:\> $StateMigrationPoint = Get-CMStateMigrationPoint -SiteCode "CM4" -SiteSystemServerName "MigrationServer.TSQA.Contoso.com"
PS C:\> Set-CMStateMigrationPoint -InputObject $StateMigrationPoint -AllowFallbackSourceLocationForContent $True -TimeDeleteAfter 12 -TimeUnit Hours
```

This example modifies a migration point named MigrationServer.TSQA.Contoso.com for the site that has the code CM4.
The example changes the migration point to allow a fallback source location for content, and modifies how long after data download to delete data.

The first command uses the **Get-CMStateMigrationPoint** cmdlet to obtain a migration point for the specified site code and server name, and stores it in the $StateMigrationPoint variable.

The second command modifies the input object stored in the $StateMigrationPoint variable.
The command sets the *AllowFallbackSourceLocationForContent* parameter to $True, and modifies the time to delete after to 12 hours.

### Example 2: Modify storage folders and boundary groups for a state migration point
```
PS C:\> $Storage01 = New-CMStoragefolder -MaximumClientNumber 100 -MinimumFreeSpace 100 -SpaceUnit Megabyte -StorageFolderName "C:\"
PS C:\> $Storage02 = New-CMStoragefolder -MaximumClientNumber 100 -MinimumFreeSpace 10 -SpaceUnit Gigabyte -StorageFolderName "D:\"
PS C:\> Set-CMStateMigrationPoint -SiteCode "CM4" -SiteSystemServerName "MigrationServer.TSQA.Contoso.com" -AddBoundaryGroupName "BG07" -AddStorageFolder $Storage02 -AllowFallbackSourceLocationForContent $False -DeleteImmediately -EnableRestoreOnlyMode $True -RemoveBoundaryGroupName "BG22" -RemoveStorageFolder $Storage01
```

This example modifies settings for a state migration point named MigrationServer.TSQA.Contoso.com for the site that has the site code CM4.
The example substitutes a different boundary group and different storage folder, and modifies other settings.

The first command uses the **New-CMStoragefolder** cmdlet to create a storage folder object, and stores it in the $Storage01 variable.
Consult documentation for that cmdlet for more information.

The second command uses the **New-CMStoragefolder** cmdlet to create a storage folder object, and stores it in the $Storage02 variable.

The third command removes the storage folder stored in the $Storage01 variable from the migration point and, in the same command, adds the storage folder stored in the $Storage02 variable to the migration point.
Likewise, the command removes the boundary group named BG22 and adds the boundary group named BG07.
The command also specifies a value of $False for the *AllowFallbackSourceLocationForContent* parameter and a value of $True for the *EnableRestoreOnlyMode* parameter.
The command uses the *DeleteImmediately* parameter; therefore, the migration point deletes client information immediately after download.

## PARAMETERS

### -AddBoundaryGroupName
Specifies an array of boundary group names.
The cmdlet adds these boundary groups to the state migration point.
During migration, clients in a boundary group use this site as a source location for content.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddStorageFolder
Specifies an array of storage folders, as storage directory data objects.
The cmdlet adds these folders to the state migration point.
To obtain a storage directory data object, use the [New-CMStoragefolder](New-CMStoragefolder.md) cmdlet.

A state migration point stores user state data when it migrates a computer to a new operating system.

```yaml
Type: StorageDirectoryData[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowFallbackSourceLocationForContent
Indicates whether a fallback source location is available.

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

### -DeleteImmediately
Indicates that deletion of client data occurs immediately after the target computer downloads that data.
If you select a value of $False, specify how long to wait by using the *TimeDeleteAfter* and *TimeUnit* parameters.

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

### -EnableRestoreOnlyMode
Indicates whether to enable restore only mode.
In restore only mode, Configuration Manager refuses new requests to store client data.

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

### -InputObject
Specifies a state migration point object.
To obtain a state migration point object, use the [Get-CMStateMigrationPoint](Get-CMStateMigrationPoint.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: StateMigrationPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### -RemoveBoundaryGroupName
Specifies an array of boundary group names.
The cmdlet removes these boundary groups from the state migration point.
During migration, clients in a boundary group use this site as a source location for content.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveStorageFolder
Specifies an array of storage folders, as storage directory data objects.
The cmdlet removes these folders from the state migration point.
A state migration point stores user state data when it migrates a computer to a new operating system.

```yaml
Type: StorageDirectoryData[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the host name for a state migration point.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeDeleteAfter
Specifies the amount of time to wait after the target computer downloads data to delete that data.
Specify a time unit by using the *TimeUnit* parameter.
To delete data immediately, specify a value of $True for the *DeleteImmediately* parameter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeUnit
Specifies a time unit for the value specified in the *TimeDeleteAfter* parameter.
The acceptable values for this parameter are: Days and Hours.

```yaml
Type: IntervalType
Parameter Sets: (All)
Aliases: 
Accepted values: Hours, Days

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

[Add-CMStateMigrationPoint](Add-CMStateMigrationPoint.md)

[Get-CMStateMigrationPoint](Get-CMStateMigrationPoint.md)

[Remove-CMStateMigrationPoint](Remove-CMStateMigrationPoint.md)

[New-CMStoragefolder](New-CMStoragefolder.md)
