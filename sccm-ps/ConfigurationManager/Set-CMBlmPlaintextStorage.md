---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Set-CMBlmPlaintextStorage

## SYNOPSIS

Set a policy to allow the site to store BitLocker recovery information in plain text.

## SYNTAX

```
Set-CMBlmPlaintextStorage [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Set a policy to allow the site to store BitLocker recovery information in plain text. Without a BitLocker management encryption certificate for SQL Server, Configuration Manager stores the key recovery information in plain text. For more information, see [Encrypt recovery data](/mem/configmgr/protect/deploy-use/bitlocker/encrypt-recovery-data).

To add this policy to a settings object, use the [New-CMBlmSetting](New-CMBlmSetting.md) or [Set-CMBlmSetting](Set-CMBlmSetting.md) cmdlets.

## EXAMPLES

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMBlmSetting](New-CMBlmSetting.md)

[Set-CMBlmSetting](Set-CMBlmSetting.md)

[Encrypt recovery data](/mem/configmgr/protect/deploy-use/bitlocker/encrypt-recovery-data)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#bitlocker-management-services)
