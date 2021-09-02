---
description: Sets a client setting client cache.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientSettingClientCache
---

# Set-CMClientSettingClientCache

## SYNOPSIS
Sets a client setting client cache.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingClientCache [-BroadcastPort <Int32>] [-ConfigureBranchCache <Boolean>]
 [-ConfigureCacheSize <Boolean>] [-DownloadPort <Int32>] [-EnableBranchCache <Boolean>]
 [-EnableHttps <Boolean>] [-EnableSuperPeer <Boolean>] [-MaxBranchCacheSizePercent <Int32>]
 [-MaxCacheSize <Int32>] [-MaxCacheSizePercent <Int32>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingClientCache [-BroadcastPort <Int32>] [-ConfigureBranchCache <Boolean>]
 [-ConfigureCacheSize <Boolean>] [-DownloadPort <Int32>] [-EnableBranchCache <Boolean>]
 [-EnableHttps <Boolean>] [-EnableSuperPeer <Boolean>] [-MaxBranchCacheSizePercent <Int32>]
 [-MaxCacheSize <Int32>] [-MaxCacheSizePercent <Int32>] [-DefaultSetting] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingClientCache [-BroadcastPort <Int32>] [-ConfigureBranchCache <Boolean>]
 [-ConfigureCacheSize <Boolean>] [-DownloadPort <Int32>] [-EnableBranchCache <Boolean>]
 [-EnableHttps <Boolean>] [-EnableSuperPeer <Boolean>] [-MaxBranchCacheSizePercent <Int32>]
 [-MaxCacheSize <Int32>] [-MaxCacheSizePercent <Int32>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -BroadcastPort
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PortForInitialNetworkBroadcast

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigureBranchCache
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

### -ConfigureCacheSize
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

### -DefaultSetting
```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

Required: True
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

### -DownloadPort
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PortForContentDownloadFromPeer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableBranchCache
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

### -EnableHttps
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableHttpsForClientPeerCommunication

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSuperPeer
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableClientInFullOsToShareContent

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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaxBranchCacheSizePercent
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumBranchCacheSizePercent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCacheSize
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumCacheSizeMb

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxCacheSizePercent
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumCacheSizePercent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
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
