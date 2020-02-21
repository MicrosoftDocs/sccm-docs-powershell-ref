---
title: New-CMAmtProvisioningAccount
titleSuffix: Configuration Manager
description: Creates an AMT Discovery and Provisioning Account.
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMAmtProvisioningAccount

## SYNOPSIS
Creates an AMT Discovery and Provisioning Account.

## SYNTAX

```
New-CMAmtProvisioningAccount -UserName <String> -Password <SecureString> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAmtProvisioningAccount** cmdlet creates an account for AMT provisioning and discovery for the Intel Active Management Technology (Intel AMT)-based computers that Microsoft System Center Configuration Manager manages out of band.

The server that runs the out of band service point role uses this account to manage some network interface features of AMT in System Center Configuration Manager, by using the out of band management feature.
The AMT Provisioning and Discovery Account that you specify in System Center Configuration Manager must match the AMT Remote Admin Account name and password of the BIOS extensions in the AMT-based computers.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create an AMT Discovery and Provisioning Account
```
PS XYZ:\> New-CMAmtProvisioningAccount -Username "AMT_Manager" -Password "S@mPle1Pswrd" -Description "Out-of-band management security group"
```

This command creates an AMT Discovery and Provisioning Account named AMT_Manager, and specifies a password and description for the account.

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

### -Description
Specifies a description for the AMT Discovery and Provisioning Account.

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
Specifies the password, as a secure string, for the AMT Discovery and Provisioning Account.

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

### -UserName
Specifies the name of the MEBx Account or Remote Admin Account of the BIOS extensions in the AMT-based computers.

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

## NOTES

## RELATED LINKS

[Enable-CMAutomaticAMTProvisioning](Enable-CMAutomaticAMTProvisioning.md)

[Invoke-CMAmtProvisioningDiscovery](Invoke-CMAmtProvisioningDiscovery.md)


