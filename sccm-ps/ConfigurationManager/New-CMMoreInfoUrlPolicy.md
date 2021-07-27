---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMMoreInfoUrlPolicy

## SYNOPSIS

Create a policy to specify the **Security Policy** link that BitLocker displays to users.

## SYNTAX

```
New-CMMoreInfoUrlPolicy [-PolicyState <State>] [-MoreInfoUrl <Uri>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Create a policy to specify the **Security Policy** link that BitLocker displays to users. The link should point to your organization's internal security policy. This policy site should provide users with information about your disk encryption requirements. BitLocker displays this link when it prompts users to encrypt a drive.

## EXAMPLES

### Example 1: New enabled policy with specified URL

This example creates a policy that's enabled with a link to the Contoso security policy for BitLocker Drive Encryption.

```powershell
New-CMMoreInfoUrlPolicy -PolicyState Enabled -MoreInfoUrl https://contoso.com/bdepolicy
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

### -MoreInfoUrl

Specify a URL for your organization's internal security policy about your disk encryption requirements. BitLocker displays this link when it prompts users to encrypt a drive.

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

### -PolicyState

Use this parameter to configure the policy.

- `Enabled`: If you enable this policy, configure the URL for the **Security Policy** link.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, BitLocker doesn't display this link for users.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### Microsoft.ConfigurationManagement.AdminConsole.BitlockerManagement.PolicyObject
## NOTES

## RELATED LINKS

[New-CMBlmSetting](New-CMBlmSetting.md)

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#url-for-the-security-policy-link)
