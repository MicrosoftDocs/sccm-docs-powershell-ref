---
author: aczechowski
description: Creates a Configuration Manager user account.
external help file: AdminUI.PS.Accounts.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMAccount
titleSuffix: Configuration Manager
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
PS XYZ:\> $Secure = ConvertTo-SecureString -String "Pas$W0rd" -AsPlainText -Force
PS XYZ:\> New-CMAccount -Name "TSQA\PFuller" -Password $Secure -SiteCode "CM2"
```

The first command creates a password as a secure string.

The second command creates an account by using the secure string.

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

### -Password
Specifies a secure string that contains the password for the user account.

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
Specifies a Configuration Manager site code.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMAccount](Get-CMAccount.md)

[Remove-CMAccount](Remove-CMAccount.md)

[Set-CMAccount](Set-CMAccount.md)
