---
external help file: AdminUI.PS.Accounts.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 759B2F3E-8C83-44AB-9857-2EFF8FDF3338
---

# New-CMAccount

## SYNOPSIS
Creates a Configuration Manager user account.

## SYNTAX

```
New-CMAccount -Password <SecureString> -UserName <String> [-SiteCode <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAccount** cmdlet creates a new user account in Microsoft System Center Configuration Manager.
A **CMAccount** is a user account that System Center Configuration Manager uses to connect to various system and network resources.
For more information about user accounts, see [Technical Reference for Accounts Used in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=248317) in the TechNet library.

## EXAMPLES

### Example 1: Create a user account by using name and password
```
PS C:\>$Secure = Read-Host -AsSecureString
PS C:\> $ConfirmSecure = Read-Host -AsSecureString
PS C:\> New-CMAccount -Name "TSQA\PFuller" -Password $Secure -ConfirmPassword $ConfirmSecure -SiteCode "CM2"
```

The first command creates a password as a secure string.

The second command creates a password confirmation as a secure string.

The third command creates an account by using the secure strings.

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

### -Password


```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode


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


```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

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

[Get-CMAccount](./Get-CMAccount.md)

[Remove-CMAccount](./Remove-CMAccount.md)

[Set-CMAccount](./Set-CMAccount.md)


