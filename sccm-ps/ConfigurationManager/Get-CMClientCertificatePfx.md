---
description: Get a client PFX certificate.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/23/2021
schema: 2.0.0
title: Get-CMClientCertificatePfx
---

# Get-CMClientCertificatePfx

## SYNOPSIS

Get a client PFX certificate.

## SYNTAX

```
Get-CMClientCertificatePfx [-Fast] [-InputObject <IResultObject>] [-Thumbprint <String>] [-UserName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a client Personal Information Exchange (PFX) certificate. For more information, see [Introduction to certificate profiles in Configuration Manager](/mem/configmgr/protect/deploy-use/introduction-to-certificate-profiles).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a client PFX certificate

This command gets the PFX client certificate for the user named **jqpublic** with the specified thumbprint.

```powershell
Get-CMClientCertificatePfx -UserName (Get-CMUser -Name "contoso\jqpublic").SMSID -Thumbprint e1c2fff14282b61f79f78fbfca6721f0517ab767
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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -InputObject

Specify a PFX certificate profile object. To get this object, use the [Get-CMCertificateProfilePfx](Get-CMCertificateProfilePfx.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: CertificateProfilePfx

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Thumbprint

Specify the thumbprint of the client PFX certificate. If you don't specify this parameter, it returns all certificates for the user.

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

### -UserName

Specify the name of the user whose client PFX certificate you want to get. To get a value for this parameter, you can use the following command: `(Get-CMUser -Name "contoso\jqpublic").SMSID`.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_ClientPfxCertificate
## NOTES

For more information on this return object and its properties, see [SMS_ClientPfxCertificate server WMI class](/mem/configmgr/develop/reference/core/clients/deploy/sms_clientpfxcertificate-server-wmi-class).

## RELATED LINKS

[Get-CMCertificateProfilePfx](Get-CMCertificateProfilePfx.md)

[Get-CMUser](Get-CMUser.md)

[Import-CMClientCertificatePfx](Import-CMClientCertificatePfx.md)

[Remove-CMClientCertificatePfx](Remove-CMClientCertificatePfx.md)
