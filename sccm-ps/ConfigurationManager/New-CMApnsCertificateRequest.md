---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
ms.assetid: B955A6FD-38A4-4AEA-889D-A4AF76CFCEB0
online version: https://go.microsoft.com/fwlink/?linkid=834245
schema: 2.0.0
---

# New-CMApnsCertificateRequest

## SYNOPSIS
Creates an APNS certificate request.

## SYNTAX

```
New-CMApnsCertificateRequest -IntuneCredential <PSCredential> [-OutputPath <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMApnsCertificateRequest** cmdlet downloads an Apple Push Notification Service (APNS) certificate signing request. You should upload this request (.csr) file to the Apple Push Certificates Portal in order to download an APN certificate. Provide a Microsoft Intune organizational account by using the *IntuneCredential* parameter.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Create an APNS certificate signing request
```
PS XYZ:\> $SecPasswd = ConvertTo-SecureString "P@ssW0rD!" -AsPlainText -Force
PS XYZ:\> $MyCreds = New-Object System.Management.Automation.PSCredential ("UserName@CompanyName.onmicrosoft.com", $SecPasswd)
PS XYZ:\> New-CMApnsCertificateRequest -IntuneCredential $MyCreds -Path "C:\Certificates\test.csr"
```

The first command converts the password into a secure string and stores the secure string in the $SecPasswd variable.

The second command creates a **PSCredential** object with the Microsoft Intune organizational account and the password stored in $SecPasswd.
The command then stores the **PSCredential** object in the $MyCreds variable.

The last command downloads an APN certificate signing request (.csr) by using the Microsoft Intune credentials stored in $MyCreds, and saves the downloaded certificate signing request (.csr) file to the specified path.

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
Aliases: ApnsCertificateRequestPath, Path

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Configuration Manager Cmdlets](ConfigurationManager.md)
