---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/13/2020
online version:
schema: 2.0.0
---

# New-CMBMSUserExemptionPolicy

## SYNOPSIS

Create a policy to configure instructions for users to request exemption from BitLocker protection.

## SYNTAX

```
New-CMBMSUserExemptionPolicy [-PolicyState <State>] [-MaxDays <UInt32>] [-ContactMethod <ContactMethod>]
 [-ContactDetail <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a policy to configure instructions for users to request exemption from BitLocker protection. These instructions include a URL, email address, or phone number.

## EXAMPLES

### Example 1: Create a policy with URL as contact method

This example creates a policy that's enabled with the following attributes:

- An exemption deadline of six days
- A custom URL for the user to submit the request

```powershell
New-CMBMSUserExemptionPolicy -PolicyState Enabled -MaxDays 6 -ContactMethod Url -ContactDetail "https://contoso.com/bitlockerexemption"
```

### Example 2: Create a policy with email as contact method

This example creates a policy that's enabled with the following attributes:

- An exemption deadline of four days
- A custom email address for the user to submit the request

```powershell
New-CMBMSUserExemptionPolicy -PolicyState Enabled -MaxDays 4 -ContactMethod Email -ContactDetail "bitlockerexemption@contoso.com"
```

### Example 3: Create a policy with phone as contact method

This example creates a policy that's enabled with the following attributes:

- An exemption deadline of 16 days
- A custom phone number for the user to submit the request

```powershell
New-CMBMSUserExemptionPolicy -PolicyState Enabled -MaxDays 16 -ContactMethod Phone -ContactDetail "515-555-8127"
```

## PARAMETERS

### -ContactDetail

Based on the **-ContactMethod** parameter, use this parameter to specify the specific string to include. For example, if **-ContactMethod** is `Phone`, specify a value phone number as the value of this parameter. The URL and email address display as links.

- The URL format is `"https://YourExemptionWebSite"`

- The email address format is `"alias@domain.tld"` 

    BitLocker automatically creates a link with the following format: `mailto: xyz@abc.com?subject=Request exemption from BitLocker protection"`

- The phone number format is as necessary for your local standard. For example, in the United States: `"123-456-7890"`

    BitLocker displays the following message: **Please call 123-456-7890 for applying exemption**

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

### -ContactMethod

Select how users submit an exemption request. Use the **-ContactDetail** parameter to specify the custom string for this method.

```yaml
Type: ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Url, Email, Phone

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

### -MaxDays

Use this parameter to specify how many days the user can postpone an enforced policy. By default, this value is `7` days (one week).

```yaml
Type: UInt32
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

- `Enabled`: If you enable this policy, and provide a URL, email address, or phone number, the user can apply for exemption. BitLocker displays instructions on how to apply for  exemption from BitLocker protection. Use the **-ContactMethod** and **ContactDetail** parameters to configure the specific method.

- `Disabled` or `NotConfigured`: If you disable or don't configure this policy, Windows doesn't display the exemption request instructions to users.

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

[BitLocker settings reference](/mem/configmgr/protect/tech-ref/bitlocker/settings#user-exemption-policy)
