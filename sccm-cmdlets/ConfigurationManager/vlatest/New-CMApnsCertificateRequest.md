---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834245
schema: 2.0.0
ms.assetid: B955A6FD-38A4-4AEA-889D-A4AF76CFCEB0
---

# New-CMApnsCertificateRequest

## SYNOPSIS
Creates an APNS certificate request.

## SYNTAX

```
New-CMApnsCertificateRequest -IntuneCredential <PSCredential> [-Path <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMApnsCertificateRequest** cmdlet downloads an Apple Push Notification Service (APNS) certificate signing request. You should upload this request (.csr) file to the Apple Push Certificates Portal in order to download an APN certificate. Provide a Microsoft Intune organizational account by using the *IntuneCredential* parameter.

## EXAMPLES

### Example 1: Create an APNS certificate signing request
```
PS C:\> $SecPasswd = ConvertTo-SecureString "P@ssW0rD!" -AsPlainText -Force
PS C:\> $MyCreds = New-Object System.Management.Automation.PSCredential ("UserName@CompanyName.onmicrosoft.com", $SecPasswd)
PS C:\> New-CMApnsCertificateRequest -IntuneCredential $MyCreds -Path "C:\Certificates\test.csr"
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

### -PassThru
Returns an object representing the item with which you are working.
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

### -Path
Specifies a location where the cmdlet saves the downloaded certificate signing request (.csr) file.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApnsCertificateRequestPath
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

[ConfMgr2016_Cmdlets](./ConfigurationManager.md)
