---
description: Sets a wireless profile.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMWirelessProfile
---

# Set-CMWirelessProfile

## SYNOPSIS
Sets a wireless profile.

## SYNTAX

### ByValue (Default)
```
Set-CMWirelessProfile -InputObject <IResultObject> [-Description <String>] [-Severity <NoncomplianceSeverity>]
 [-ClearSupportedPlatform] [-AddSupportedPlatform <IResultObject[]>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-NetworkName <String>] [-Ssid <String>]
 [-ConnectAutoNetworkInRange <Boolean>] [-LookOtherNetworkWhileConnected <Boolean>]
 [-ConnectEvenNotBroadcasting <Boolean>] [-AuthenticationMode <AuthenticationMode>]
 [-EnableSingleSignOn <Boolean>] [-SingleSignOnImmediatelyBefore <Boolean>] [-SingleSignOnMaxDelaySec <Int32>]
 [-SingleSignOnAdditionalDialogs <Boolean>] [-SingleSignOnVlan <Boolean>] [-EnablePmkCaching <Boolean>]
 [-PmkTimeToLiveMins <Int32>] [-PmkCacheMaxEntries <Int32>] [-PreAuthentication <Boolean>]
 [-PreAuthAttempts <Int32>] [-EnableFipsCompliance <Boolean>] [-ConfigureProxy <Boolean>]
 [-AutoDetectProxy <Boolean>] [-AutoScriptUrl <String>] [-ProxyAddress <String>] [-ProxyPort <Int32>]
 [-BypassProxy <String>] [-SecurityAuthentication <SecurityAuthentication>]
 [-SecurityEncryption <SecurityEncryption>] [-EapType <EapType>] [-TrustedServerCertSubjectNames <String>]
 [-RememberCredentials] [-RememberUserCredentials <Boolean>] [-RootCertificate <IResultObject[]>]
 [-ClientCertificate <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMWirelessProfile -Id <Int32> [-Description <String>] [-Severity <NoncomplianceSeverity>]
 [-ClearSupportedPlatform] [-AddSupportedPlatform <IResultObject[]>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-NetworkName <String>] [-Ssid <String>]
 [-ConnectAutoNetworkInRange <Boolean>] [-LookOtherNetworkWhileConnected <Boolean>]
 [-ConnectEvenNotBroadcasting <Boolean>] [-AuthenticationMode <AuthenticationMode>]
 [-EnableSingleSignOn <Boolean>] [-SingleSignOnImmediatelyBefore <Boolean>] [-SingleSignOnMaxDelaySec <Int32>]
 [-SingleSignOnAdditionalDialogs <Boolean>] [-SingleSignOnVlan <Boolean>] [-EnablePmkCaching <Boolean>]
 [-PmkTimeToLiveMins <Int32>] [-PmkCacheMaxEntries <Int32>] [-PreAuthentication <Boolean>]
 [-PreAuthAttempts <Int32>] [-EnableFipsCompliance <Boolean>] [-ConfigureProxy <Boolean>]
 [-AutoDetectProxy <Boolean>] [-AutoScriptUrl <String>] [-ProxyAddress <String>] [-ProxyPort <Int32>]
 [-BypassProxy <String>] [-SecurityAuthentication <SecurityAuthentication>]
 [-SecurityEncryption <SecurityEncryption>] [-EapType <EapType>] [-TrustedServerCertSubjectNames <String>]
 [-RememberCredentials] [-RememberUserCredentials <Boolean>] [-RootCertificate <IResultObject[]>]
 [-ClientCertificate <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMWirelessProfile -Name <String> [-Description <String>] [-Severity <NoncomplianceSeverity>]
 [-ClearSupportedPlatform] [-AddSupportedPlatform <IResultObject[]>]
 [-RemoveSupportedPlatform <IResultObject[]>] [-NetworkName <String>] [-Ssid <String>]
 [-ConnectAutoNetworkInRange <Boolean>] [-LookOtherNetworkWhileConnected <Boolean>]
 [-ConnectEvenNotBroadcasting <Boolean>] [-AuthenticationMode <AuthenticationMode>]
 [-EnableSingleSignOn <Boolean>] [-SingleSignOnImmediatelyBefore <Boolean>] [-SingleSignOnMaxDelaySec <Int32>]
 [-SingleSignOnAdditionalDialogs <Boolean>] [-SingleSignOnVlan <Boolean>] [-EnablePmkCaching <Boolean>]
 [-PmkTimeToLiveMins <Int32>] [-PmkCacheMaxEntries <Int32>] [-PreAuthentication <Boolean>]
 [-PreAuthAttempts <Int32>] [-EnableFipsCompliance <Boolean>] [-ConfigureProxy <Boolean>]
 [-AutoDetectProxy <Boolean>] [-AutoScriptUrl <String>] [-ProxyAddress <String>] [-ProxyPort <Int32>]
 [-BypassProxy <String>] [-SecurityAuthentication <SecurityAuthentication>]
 [-SecurityEncryption <SecurityEncryption>] [-EapType <EapType>] [-TrustedServerCertSubjectNames <String>]
 [-RememberCredentials] [-RememberUserCredentials <Boolean>] [-RootCertificate <IResultObject[]>]
 [-ClientCertificate <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -AddSupportedPlatform
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AuthenticationMode
```yaml
Type: AuthenticationMode
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, MachineOrUser, Machine, User, Guest

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoDetectProxy
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AutoScriptUrl
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

### -BypassProxy
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

### -ClearSupportedPlatform
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

### -ClientCertificate
{{ Fill ClientCertificate Description }}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConfigureProxy
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectAutoNetworkInRange
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectEvenNotBroadcasting
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
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
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -EapType
```yaml
Type: EapType
Parameter Sets: (All)
Aliases:
Accepted values: AKA, AKAprime, FAST, LEAP, PEAP, SIM, TLS, TTLS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableFipsCompliance
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnablePmkCaching
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSingleSignOn
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
```yaml
Type: Int32
Parameter Sets: ById
Aliases: CI_ID, CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
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

### -LookOtherNetworkWhileConnected
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkName
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

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -PmkCacheMaxEntries
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PmkTimeToLiveMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreAuthAttempts
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreAuthentication
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProxyAddress
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

### -ProxyPort
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RememberCredentials
{{ Fill RememberCredentials Description }}

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

### -RememberUserCredentials
{{ Fill RememberUserCredentials Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSupportedPlatform
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSupportedPlatforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RootCertificate
{{ Fill RootCertificate Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RootCertificates

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityAuthentication
```yaml
Type: SecurityAuthentication
Parameter Sets: (All)
Aliases:
Accepted values: Undefined, Open, WPA_Personal, WPA2_Personal, WPA_Enterprise, WPA2_Enterprise, Shared, WEP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecurityEncryption
```yaml
Type: SecurityEncryption
Parameter Sets: (All)
Aliases:
Accepted values: Undefined, None, WEP, TKIP, AES

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Severity
```yaml
Type: NoncomplianceSeverity
Parameter Sets: (All)
Aliases:
Accepted values: None, Informational, Warning, Critical, CriticalWithEvent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SingleSignOnAdditionalDialogs
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SingleSignOnImmediatelyBefore
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SingleSignOnMaxDelaySec
```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SingleSignOnVlan
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ssid
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

### -TrustedServerCertSubjectNames
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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_commonparameters?view=powershell-7).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
