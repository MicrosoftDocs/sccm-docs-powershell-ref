---
description: Creates an Apple DEP token reqeust.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMDepTokenRequest
---

# New-CMDepTokenRequest

## SYNOPSIS
Creates an Apple DEP token reqeust.

## SYNTAX

```
New-CMDepTokenRequest -IntuneCredential <PSCredential> [-OutputPath <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-DepTokenRequest** cmdlet requests a public certificate from Microsoft Intune that can be used to download an encrypted DEP token from the Apple Deployment Program portal. Apple uses the public token to encrypt the DEP token. You need to provide a Microsoft Intune organizational account by using the *IntuneCredential* parameter.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a DEP token request
```
PS XYZ:\> $SecPasswd = ConvertTo-SecureString "password" -AsPlainText -Force
PS XYZ:\> $IntuneCreds = New-Object System.Management.Automation.PSCredential ("Username@CompanyName.onmicrosoft.com", $SecPasswd)
PS XYZ:\> New-CMDepTokenRequest -IntuneCredential $IntuneCreds -Path "c:\test.pem"
```

The first command converts a password to a secure string and stores it in the $SecPasswd variable.

The second command creates a **PSCredential** object that contains the Intune organizational account and the password stored in $SecPasswd.
The command stores the **PSCredential** object in the $IntuneCreds variable.

The last command downloads a DEP token request using the Intune credentials stored in $IntuneCreds and stores the downloaded file at the specified path.

## PARAMETERS

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

### -IntuneCredential
Specifies a **PSCredential** object that contains a Microsoft Intune organizational account and password.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Credential

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputPath
```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
