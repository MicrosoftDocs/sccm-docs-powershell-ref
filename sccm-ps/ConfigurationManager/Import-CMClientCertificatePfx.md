---
external help file: AdminUI.PS.Dcm.dll-Help.xml
ms.assetid: AC569305-8C8B-4A6A-9BE8-4AC78003A7E9
online version: https://go.microsoft.com/fwlink/?linkid=834043
schema: 2.0.0
---

# Import-CMClientCertificatePfx

## SYNOPSIS
Imports a client PFX certificate.

## SYNTAX

```
Import-CMClientCertificatePfx -Path <String> -UserName <String> [-Password <SecureString>]
 -CertificateProfilePfx <IResultObject> [-PassThru] [-ForSmimeEncryption] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMClientCertificatePfx** cmdlet imports a client Personal Information Exchange (PFX) certificate to a site server.

## EXAMPLES

### Example 1: Import a client PFX certificate
```
PS C:\> Import-CMClientCertificatePfx -Path "\\server\ShareFolder\test.pfx" -UserName (Get-CMUser -Name "Contoso\Administrator").SMSID -Password (ConvertTo-SecureString -String "sccm" -AsPlainText -Force) -CertificateProfilePfx (Get-CMCertificateProfilePfx -Name "CertTest" -Fast )
```

This command imports a client PFX certificate for the user named administrator.

## PARAMETERS

### -CertificateProfilePfx
Specifies a PFX certificate profile object.
To obtain a PFX certificate profile object, use the Get-CMCertificateProfilePfx cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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
Default value: False
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

### -ForSmimeEncryption
{{Fill ForSmimeEncryption Description}}

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

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -Password
Specifies, as a secure string, the password that allows access to the imported PFX certificate.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies the path of the client PFX certificate.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificatePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the user that the imported PFX certificate targets.
To get the user value, you can use the following command: `(get-cmuser -name domain\username).SMSID`.

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

### IResultObject#SMS_ClientPfxCertificate

## NOTES

## RELATED LINKS

[Get-CMCertificateProfilePfx](Get-CMCertificateProfilePfx.md)

[Get-CMClientCertificatePfx](Get-CMClientCertificatePfx.md)

[Get-CMUser](Get-CMUser.md)

[Remove-CMClientCertificatePfx](Remove-CMClientCertificatePfx.md)
