---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Get-CMWdacSetting

## SYNOPSIS

Get one or all of the Microsoft Defender Application Control policies from the site.

## SYNTAX

```
Get-CMWdacSetting [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Get one or all of the Microsoft Defender Application Control policies from the site. To create a new policy, use [New-CMWdacSetting](New-CMWdacSetting.md).

## EXAMPLES

### Example 1: Get a Application Control policy by name

This example gets a specific Application Control policy specified by name.

```powershell
Get-CMWdacSetting -Name "My App Control settings"
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

### -Name

Specify the name of the policy to get.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.WDAC.CMWdacSettings
## NOTES

## RELATED LINKS

[Copy-CMWdacSetting](Copy-CMWdacSetting.md)

[New-CMWdacSetting](New-CMWdacSetting.md)

[Remove-CMWdacSetting](Remove-CMWdacSetting.md)

[Set-CMWdacSetting](Set-CMWdacSetting.md)

[New-CMSettingDeployment](New-CMSettingDeployment.md)

[Windows Defender Application Control management with Configuration Manager](/mem/configmgr/protect/deploy-use/use-device-guard-with-configuration-manager)
