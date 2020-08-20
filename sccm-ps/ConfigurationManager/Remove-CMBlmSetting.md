---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/20/2020
---

# Remove-CMBlmSetting

## SYNOPSIS

Delete a BitLocker management policy setting object from the site.

## SYNTAX

```
Remove-CMBlmSetting [-CMSettings] <CMSettings> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Delete a BitLocker management policy setting object from the site. Use [Get-CMBlmSetting](Get-CMBlmSetting.md) to get an existing management policy.

## EXAMPLES

### Example 1

This example gets an object by name and then removes it from the site.

```powershell
Get-CMBlmSetting -Name "My BitLocker setting" | Remove-CMBlmSetting
```

## PARAMETERS

### -CMSettings

Specify a BitLocker management policy settings object to remove. Use the [Get-CMBlmSetting](Get-CMBlmSetting.md) to get this object.

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

### Microsoft.ConfigurationManagement.Cmdlets.BitLockerManagement.Commands.CMSettings

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMBlmSetting](Get-CMBlmSetting.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[Set-CMBlmSetting](Set-CMBlmSetting.md)

[Deploy BitLocker management](/mem/configmgr/protect/deploy-use/bitlocker/deploy-management-agent)
