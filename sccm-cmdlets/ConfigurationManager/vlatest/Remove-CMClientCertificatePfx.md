---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833952
schema: 2.0.0
ms.assetid: 37712E99-06A4-4F70-B7C2-1CE8156D44F8
---

# Remove-CMClientCertificatePfx

## SYNOPSIS
Removes a PFX client certificate.

## SYNTAX

### ByValue (Default)
```
Remove-CMClientCertificatePfx -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMClientCertificatePfx -UserName <String> [-Thumbprint <String>]
 [-CertificateProfilePfx <IResultObject>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMClientCertificatePFX** removes a client Personal Information Exchange (PFX) certificate from a site server.

## EXAMPLES

### Example 1: Remove a PFX client certificate by using the pipeline
```
PS C:\> Get-CMClientCertificatePfx -UserName (Get-CMUser -Name "Contoso\Administrator01").SMSID -Thumbprint e1c2fff14282b61f79f78fbfca6721f0517ab767 | Remove-CMClientCertificatePfx
```

This command gets the client Pfx certificate object for the user named Administrator01 with the specified thumbprint and uses the pipeline operator to pass the object to **Remove-CMClientCertificatePfx**, which removes the certificate.

### Example 2: Remove a PFX client certificate by name
```
PS C:\> Remove-CMClientCertificatePfx -Username (Get-CMUser -Name "Contoso\Administrator02").SMSID -Thumbprint e1c2fff14282b61f79f78fbfca6721f0517ab767
```

This command removes the client Pfx certificate for the user named Administrator02 with the specified thumbprint.

## PARAMETERS

### -CertificateProfilePfx
Specifies a PFX certificate profile object.
To obtain a PFX certificate object, use the Get-CMCertificateProfilePfx cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByName
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Forces the command to run without asking for user confirmation.

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
Indicates that wildcard handling is enabled.

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
Specifies a client PFX certificate object.
To obtain a client PFX certificate object, use the Get-CMClientCertificatePfx cmdlet.

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

### -Thumbprint
Specifies the thumbprint of a client PFX certificate.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName
Specifies the user for whom you want to remove a client PFX certificate.
To set a vaule to the parameter, you can use `(get-cmuser -name domain\username).SMSID`.

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

## NOTES

## RELATED LINKS

[Get-CMCertificateProfilePfx](./Get-CMCertificateProfilePfx.md)

[Get-CMClientCertificatePfx](./Get-CMClientCertificatePfx.md)

[Get-CMUser](./Get-CMUser.md)

[Import-CMClientCertificatePfx](./Import-CMClientCertificatePfx.md)
