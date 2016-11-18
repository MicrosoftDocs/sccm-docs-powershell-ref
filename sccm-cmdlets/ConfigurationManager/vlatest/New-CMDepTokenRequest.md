---
external help file: AdminUI.PS.Hybrid.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 4046A417-80F5-4665-9258-AE12B85F6F09
---

# New-CMDepTokenRequest

## SYNOPSIS
Creates an Apple DEP token reqeust.

## SYNTAX

```
New-CMDepTokenRequest -IntuneCredential <PSCredential> [-Path <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-DepTokenRequest** cmdlet requests an Apple Device Enrollment Program (DEP) token request.
You need to provide a Microsoft Intune organizational account by using the *IntuneCredential* parameter.

## EXAMPLES

### Example 1: Create a DEP token request
```
PS C:\> $SecPasswd = ConvertTo-SecureString "password" -AsPlainText -Force
PS C:\> $IntuneCreds = New-Object System.Management.Automation.PSCredential ("Username@CompanyName.onmicrosoft.com", $SecPasswd)
PS C:\> New-CMDepTokenRequest -IntuneCredential $IntuneCreds -Path "c:\test.pem"
```

The first command converts a password to a secure string and stores it in the $SecPasswd variable.

The second command creates a **PSCredential** object that contains the Intune organizational account and the password stored in $SecPasswd.
The command stores the **PSCredential** object in the $IntuneCreds variable.

The last command creates a DEP token request using the Intune credentials stored inm $IntuneCreds and the DEP token request file stored at the specified path.

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
Specifies the path to the DEP token request (.pem) file.

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


