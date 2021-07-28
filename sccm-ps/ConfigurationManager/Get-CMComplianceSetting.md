---
description: Get a setting for a configuration item.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Get-CMComplianceSetting
---

# Get-CMComplianceSetting

## SYNOPSIS

Get a setting for a configuration item.

## SYNTAX

### ById
```
Get-CMComplianceSetting [-Fast] [-Id] <Int32> [-SettingName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMComplianceSetting [-Fast] -InputObject <IResultObject> [-SettingName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMComplianceSetting [-Fast] [-Name] <String> [-SettingName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a setting for a configuration item. Settings represent the business or technical conditions to assess compliance on client devices. Configure a new setting or browse to an existing setting on a reference computer. For more information, see [Get started with compliance settings in Configuration Manager](/mem/configmgr/compliance/get-started/get-started-with-compliance-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the location for a setting in a configuration item

This example queries the setting named **appevents** for the configuration item **Windows health check** and returns just the location attribute. This attribute includes the registry or file path for the setting.

```powershell
Get-CMComplianceSetting -Name "Windows health check" -SettingName "appevents" -Fast | Select-Object Location
```

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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

Specify the **CI_ID** for the configuration item that has the setting you want to get. For example, `258895`.

```yaml
Type: Int32
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a configuration item object that has the setting you want to get. To get this object, use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md).

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the configuration item that has the setting you want to get.

```yaml
Type: String
Parameter Sets: ByName
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingName

Specify the name of the setting in the configuration item. This value is the same as the **Name** value on the **Settings** tab of the configuration item properties in the console.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### Microsoft.ConfigurationManagement.DesiredConfigurationManagement.ConfigurationItemSetting
## NOTES

## RELATED LINKS

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMComplianceRule](Get-CMComplianceRule.md)
