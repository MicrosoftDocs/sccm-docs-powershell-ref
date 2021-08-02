---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Remove-CMWdacSetting

## SYNOPSIS

Delete a Microsoft Defender Application Control policy from the site.

## SYNTAX

```
Remove-CMWdacSetting [-CMSettings] <CMSettings> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Delete a Microsoft Defender Application Control policy from the site. Use [Get-CMWdacSetting](Get-CMWdacSetting.md) to get an existing policy object.

## EXAMPLES

### Example 1

This example gets an object by name and then removes it from the site.

```powershell
Get-CMWdacSetting -Name "My App Control setting" | Remove-CMWdacSetting
```

## PARAMETERS

### -CMSettings

Specify a Microsoft Defender Application Control policy object to remove. Use the [Get-CMWdacSetting](Get-CMWdacSetting.md) to get this object.

```yaml
Type: CMSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
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

### -Force

Run the command without asking for confirmation.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.SimplifiedSettings.CMSettings
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Copy-CMWdacSetting](Copy-CMWdacSetting.md)

[Get-CMWdacSetting](Get-CMWdacSetting.md)

[New-CMWdacSetting](New-CMWdacSetting.md)

[Set-CMWdacSetting](Set-CMWdacSetting.md)

[Windows Defender Application Control management with Configuration Manager](/mem/configmgr/protect/deploy-use/use-device-guard-with-configuration-manager)
