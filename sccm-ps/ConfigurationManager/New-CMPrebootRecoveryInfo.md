---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMPrebootRecoveryInfo

## SYNOPSIS

Configure the recovery message that the pre-boot key recovery screen displays when the OS drive is locked.

## SYNTAX

```
New-CMPrebootRecoveryInfo [-PolicyState <State>] [-RecoveryMessage <String>] [-RecoveryUrl <Uri>]
 [-UseRecoveryMessage] [-UseRecoveryUrl] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the entire recovery message or replace the existing URL the pre-boot key recovery screen shows when the OS drive is locked.

If you use both **-UseRecoveryUrl** and **-UseRecoveryMessage** parameters, the pre-boot key recovery screen displays the default BitLocker recovery message and URL. If you previously configured a custom recovery message or URL and want to revert to the default message, keep the policy enabled and use both **-UseRecoveryUrl** and **-UseRecoveryMessage** parameters

> [!NOTE]
> Pre-boot doesn't support all characters and languages. Test the characters that you want to use for the custom message or URL. Make sure the pre-boot recovery screen correctly displays your custom message or URL.

## EXAMPLES

### Example 1: New enabled policy with a custom recovery message and URL

This example creates a new policy that's enabled with custom values.

```powershell
New-CMPrebootRecoveryInfo -PolicyState Enabled -UseRecoveryMessage -RecoveryMessage "Contact the Contoso Helpdesk at 515-555-8127 or https://contoso.com/bitlockerrecovery"
```

### Example 2: New enabled policy with a custom recovery URL

```powershell
New-CMPrebootRecoveryInfo -PolicyState Enabled -UseRecoveryUrl -RecoveryUrl https://contoso.com/bitlockerrecovery
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

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, BitLocker uses the custom information that you specify.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, BitLocker uses the default information.

```yaml
Type: State
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryMessage

Specify a custom message to display on the pre-boot recovery screen. If you also want to specify a recovery URL, include it as part of this custom recovery message. The maximum string length is 32,768 characters. Use this parameter with the **-UseRecoveryMessage** parameter.

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

### -RecoveryUrl

Replace the default URL displayed in the pre-boot BitLocker recovery screen. The maximum URI length is 32,768 characters. Use this parameter with the **-UseRecoveryUrl** parameter.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseRecoveryMessage

If you add this parameter, the pre-boot key recovery screen displays the value of **-RecoveryMessage**.

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

### -UseRecoveryUrl

If you add this parameter, the URL you specify for **-RecoveryUrl** replaces the default URL in the default recovery message.

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

### Microsoft.ConfigurationManagement.AdminConsole.BitlockerManagement.PolicyObject
## NOTES

## RELATED LINKS

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#pre-boot-recovery-message-and-url)
