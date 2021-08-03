---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Copy-CMWdacSetting

## SYNOPSIS

Make a copy of a Microsoft Defender Application Control policy object.

## SYNTAX

```
Copy-CMWdacSetting [-WdacSettings] <CMWdacSettings> -Name <String> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet makes a copy of a Microsoft Defender Application Control policy object. All existing policies are included. Use the [Get-CMWdacSetting](Get-CMWdacSetting.md) to get this object.

## EXAMPLES

### Example 1: Copy an existing policy object

This example gets an existing Microsoft Defender Application Control policy object by name, and makes a copy.

```powershell
Get-CMWdacSetting -Name "My App Control settings" | Copy-CMWdacSetting -Name "New App Control settings"
```

## PARAMETERS

### -Description

Specify a description for the new Microsoft Defender Application Control policy object.

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

Specify a name for the new Microsoft Defender Application Control policy object.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WdacSettings

Specify a Microsoft Defender Application Control policy object to copy. Use the [Get-CMWdacSetting](Get-CMWdacSetting.md) to get this object.

```yaml
Type: CMWdacSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.WDAC.CMWdacSettings
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.WDAC.CMWdacSettings
## NOTES

## RELATED LINKS

[Get-CMWdacSetting](Get-CMWdacSetting.md)

[New-CMWdacSetting](New-CMWdacSetting.md)

[Remove-CMWdacSetting](Remove-CMWdacSetting.md)

[Set-CMWdacSetting](Set-CMWdacSetting.md)
