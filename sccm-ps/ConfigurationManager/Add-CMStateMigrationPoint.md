---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 3C642D15-E6BF-4416-99F6-98BDBC2A5D36
online version: https://go.microsoft.com/fwlink/?linkid=833762
schema: 2.0.0
---

# Add-CMStateMigrationPoint

## SYNOPSIS
Adds a state migration point in Configuration Manager.

## SYNTAX

### ByValue (Default)
```
Add-CMStateMigrationPoint -StorageFolder <StorageDirectoryData[]> [-DeleteImmediately]
 [-TimeDeleteAfter <Int32>] [-TimeUnit <IntervalType>] [-EnableRestoreOnlyMode <Boolean>]
 [-AllowFallbackSourceLocationForContent <Boolean>] [-BoundaryGroupName <String[]>]
 -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName
```
Add-CMStateMigrationPoint [-SiteSystemServerName] <String> [-SiteCode <String>]
 -StorageFolder <StorageDirectoryData[]> [-DeleteImmediately] [-TimeDeleteAfter <Int32>]
 [-TimeUnit <IntervalType>] [-EnableRestoreOnlyMode <Boolean>]
 [-AllowFallbackSourceLocationForContent <Boolean>] [-BoundaryGroupName <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Add-CMStateMigrationPoint** cmdlet adds a state migration point in Microsoft System Center Configuration Manager.
A state migration point is a site system role that manages data transfer from client computers during an operating system installation process.

## EXAMPLES

### Example 1: Add a state migration point
```
PS C:\> $s1 = New-CMStoragefolder -StorageFolderName "C:\Sto-1" -MaximumClientNumber 100 -MinimumFreeSpace 100 -SpaceUnit Megabyte
PS C:\> $s2 = New-CMStoragefolder -StorageFolderName "D:\Sto-2" -MaximumClientNumber 100 -MinimumFreeSpace 10 -SpaceUnit Gigabyte
PS C:\> Add-CMStateMigrationPoint -SiteSystemServerName "Contoso-Migration.Contoso.com" -SiteCode "CM2" -StorageFolders $s1,$s2 -DeleteImmediately -EnableRestoreOnlyMode $False -AllowFallbackSourceLocationForContent $False -BoundaryGroupName "CMC"
```

The first command creates a storage folder on the C: drive that has a maximum number of clients setting and a minimum free space setting.
The command stores the result in the $s1 variable.

The second command creates a storage folder on the D: drive that has a maximum number of clients setting and a minimum free space setting.
The command stores the result in the $s2 variable.

The third command adds a state migration point.

## PARAMETERS

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

### -BoundaryGroupName
Specifies an array of names of boundary groups.
You can get a boundary group name by using the [Get-CMBoundaryGroup](Get-CMBoundaryGroup.md) cmdlet.

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
Indicates that Configuration Manager deletes client data immediately after the target computer downloads the data.

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
If this mode is enabled, Configuration Manager refuses new requests to store client data.

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: SiteServer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the Configuration Manager site that hosts this site system role.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of the site system server in Configuration Manager.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name, ServerName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageFolder
```yaml
Type: StorageDirectoryData[]
Parameter Sets: (All)
Aliases: StorageFolders

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TimeDeleteAfter
Specifies a time interval to wait before client data is deleted.

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
Specifies the unit of time for the *TimeDeleteAfter* parameter.
Valid values are: Days and Hours.

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

[Get-CMStateMigrationPoint](Get-CMStateMigrationPoint.md)

[Remove-CMStateMigrationPoint](Remove-CMStateMigrationPoint.md)

[Set-CMStateMigrationPoint](Set-CMStateMigrationPoint.md)

[Get-CMBoundaryGroup](Get-CMBoundaryGroup.md)


