---
description: Sets a Configuration Manager user account.
external help file: AdminUI.PS.Accounts.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMAccount
---

# Set-CMAccount

## SYNOPSIS
Sets a Configuration Manager user account.

## SYNTAX

### SetAccountByName (Default)
```
Set-CMAccount [-Password <SecureString>] [-SiteCode <String>] -UserName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetAccountByObject
```
Set-CMAccount -InputObject <IResultObject> [-Password <SecureString>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAccount** cmdlet sets a user account in Configuration Manager.
A **CMAccount** is a user account that Configuration Manager uses to connect to various system and network resources.
For more information about user accounts, see [Technical Reference for Accounts Used in Configuration Manager](https://docs.microsoft.com/mem/configmgr/core/plan-design/hierarchy/accounts).

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Set an account by using name and password
```
PS XYZ:\> $Secure = ConvertTo-SecureString -String "Pas$W0rd02" -AsPlainText -Force
PS XYZ:\> Set-CMAccount -Name "TSQA\PFuller" -Password $Secure -SiteCode "CM2"
```

The first command creates a variable as a secure string.

The second command sets the password for the account.

## PARAMETERS

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

### -InputObject
Specifies a user account object.
You can get a user account object by using the Get-CMAccount cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetAccountByObject
Aliases: Account

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Password
Specifies a secure string that contains the password for the user account.

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

### -SiteCode
Specifies a Configuration Manager site code.

```yaml
Type: String
Parameter Sets: SetAccountByName
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
Parameter Sets: SetAccountByName
Aliases: Name

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

[Get-CMAccount](Get-CMAccount.md)

[New-CMAccount](New-CMAccount.md)

[Remove-CMAccount](Remove-CMAccount.md)
