---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Set-CMCISupportedPlatform

## SYNOPSIS

Configure the supported platforms for a configuration item.

## SYNTAX

```
Set-CMCISupportedPlatform [-InputObject] <PSObject> [-DefineVersionManually] [-VersionMajor <Int32>]
 [-VersionMinor <Int32>] [-VersionBuild <Int32>] [-ServicePackMajor <Int32>] [-ServicePackMinor <Int32>]
 [-Is64BitRequired <Boolean>] [-AddSupportedPlatform <IResultObject[]>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the supported platforms for a configuration item. For more information, see [Create configuration items in Configuration Manager](/mem/configmgr/compliance/deploy-use/create-configuration-items).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set platform for configuration item

This example removes two OS platforms for macOS, and adds two new platforms.

```powershell
$mac_ci = Get-CMConfigurationItem -Name "Mac CI"

$mac_platform1 = Get-CMSupportedPlatform -Name "Mac OS X 10.8"
$mac_platform2 = Get-CMSupportedPlatform -Name "Mac OS X 10.9"
$mac_platforms = $mac_platform1,$mac_platform2

$mac_platform3 = Get-CMSupportedPlatform -Name "Mac OS X 10.7"
$mac_platform4 = Get-CMSupportedPlatform -Name "Mac OS X 10.6"
$mac_platforms2 = $mac_platform3,$mac_platform4

Set-CMCISupportedPlatform -InputObject $mac_ci -AddSupportedPlatform $mac_platforms -RemoveSupportedPlatform $mac_platforms2
```

## PARAMETERS

### -AddSupportedPlatform

Specify one or more supported platform objects to add to the configuration item. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefineVersionManually

Add this parameter to manually specify the OS version.

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

### -InputObject

Specify a configuration item object to add the supported platforms. To get this object, use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Is64BitRequired

Set this parameter to **$true** to require 64-bit OS platforms.

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

### -RemoveSupportedPlatform

Specify one or more supported platform objects to remove from the configuration item. To get this object, use the [Get-CMSupportedPlatform](Get-CMSupportedPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServicePackMajor

If you use the **DefineVersionManually** parameter, specify the service pack major version as an integer value.

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

### -ServicePackMinor

If you use the **DefineVersionManually** parameter, specify the service pack minor version as an integer value.

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

### -VersionBuild

If you use the **DefineVersionManually** parameter, specify the build number as an integer value.

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

### -VersionMajor

If you use the **DefineVersionManually** parameter, specify the major version as an integer value.

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

### -VersionMinor

If you use the **DefineVersionManually** parameter, specify the minor version as an integer value.

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

### System.Management.Automation.PSObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMSupportedPlatform](Get-CMSupportedPlatform.md)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Create configuration items in Configuration Manager](/mem/configmgr/compliance/deploy-use/create-configuration-items)
