---
description: Removes a PFX client certificate.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMClientCertificatePfx
---

# Remove-CMClientCertificatePfx

## SYNOPSIS
Removes a PFX client certificate.

## SYNTAX

### ByValue (Default)
```
Remove-CMClientCertificatePfx [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMClientCertificatePfx [-CertificateProfilePfx <IResultObject>] [-Force] [-Thumbprint <String>]
 -UserName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMClientCertificatePFX** removes a client Personal Information Exchange (PFX) certificate from a site server.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a PFX client certificate by using the pipeline
```
PS XYZ:\> Get-CMClientCertificatePfx -UserName (Get-CMUser -Name "Contoso\Administrator01").SMSID -Thumbprint e1c2fff14282b61f79f78fbfca6721f0517ab767 | Remove-CMClientCertificatePfx
```

This command gets the client Pfx certificate object for the user named Administrator01 with the specified thumbprint and uses the pipeline operator to pass the object to **Remove-CMClientCertificatePfx**, which removes the certificate.

### Example 2: Remove a PFX client certificate by name
```
PS XYZ:\> Remove-CMClientCertificatePfx -Username (Get-CMUser -Name "Contoso\Administrator02").SMSID -Thumbprint e1c2fff14282b61f79f78fbfca6721f0517ab767
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
To set a value to the parameter, you can use `(get-cmuser -name domain\username).SMSID`.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMCertificateProfilePfx](Get-CMCertificateProfilePfx.md)

[Get-CMClientCertificatePfx](Get-CMClientCertificatePfx.md)

[Get-CMUser](Get-CMUser.md)

[Import-CMClientCertificatePfx](Import-CMClientCertificatePfx.md)
