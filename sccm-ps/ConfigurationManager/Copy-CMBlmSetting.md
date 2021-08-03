---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Copy-CMBlmSetting

## SYNOPSIS

Make a copy of a BitLocker management policy settings object.

## SYNTAX

```
Copy-CMBlmSetting [-BlmSettings] <BlmSettings> -Name <String> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet makes a copy of a BitLocker Management policy settings object. All existing policies are included. Use the [Get-CMBlmSetting](Get-CMBlmSetting.md) to get this object.

## EXAMPLES

### Example 1: Copy an existing policy object

This example gets an existing BitLocker management policy settings object by name, and makes a copy.

```powershell
Get-CMBlmSetting -Name "My BitLocker settings" | Copy-CMBlmSetting -Name "New BitLocker settings"
```

## PARAMETERS

### -BlmSettings

Specify a BitLocker management policy settings object to copy. Use the [Get-CMBlmSetting](Get-CMBlmSetting.md) to get this object.

```yaml
Type: BlmSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Description

Specify a description for the new BitLocker management policy object.

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

Specify a name for the new BitLocker management policy object.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.BitLockerManagement.BlmSettings
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.BitLockerManagement.BlmSettings
## NOTES

## RELATED LINKS

[Get-CMBlmSetting](Get-CMBlmSetting.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[Remove-CMBlmSetting](Remove-CMBlmSetting.md)

[Set-CMBlmSetting](Set-CMBlmSetting.md)
