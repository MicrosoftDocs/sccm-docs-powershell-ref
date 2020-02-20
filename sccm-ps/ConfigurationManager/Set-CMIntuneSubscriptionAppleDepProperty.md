---
author: aczechowski
description: Updates a Microsoft Intune subscription to enable the Apple DEP.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMIntuneSubscriptionAppleDepProperty
titleSuffix: Configuration Manager
---

# Set-CMIntuneSubscriptionAppleDepProperty

## SYNOPSIS
Updates a Microsoft Intune subscription to enable the Apple DEP.

## SYNTAX

```
Set-CMIntuneSubscriptionAppleDepProperty [-Enable <Boolean>] [-DepTokenPath <String>] [-AppleId <String>]
 [-IntuneCredential <PSCredential>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscriptionAppleDepProperty** cmdlet updates the settings of a Microsoft Intune subscription to enable the Apple Device Enrollment Program (DEP).

## EXAMPLES

### Example 1: Enable the Apple DEP
```
PS XYZ:\> $SecPasswd = ConvertTo-SecureString "P@ssW0rD!" -AsPlainText -Force
PS XYZ:\> $Creds = New-Object System.Management.Automation.PSCredential ("AccountName@CompanyName.onmicrosoft.com", $SecPasswd)
PS XYZ:\> Set-CMIntuneSubscriptionAppleDepProperty -Enable $True -AppleId "AppleID01" -DepTokenPath "C:\tokens\DepToken.p7m" -IntuneCredential $Creds
```

The first command creates a secure password object and stores the object in the $SecPasswd variable.

The second command creates a **PSCredential** object containing a Microsoft Intune organizational account and the password stored in $SecPasswd.
The command stores the object in the $Creds variable.

The last command enables the Apple Device Enrollment Program for the Microsoft Intune subscription.

## PARAMETERS

### -AppleId
Specifies an Apple ID.

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

### -DepTokenPath
Specifies the path to the Device Enrollment program (DEP) token.

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

### -Enable
Indicates whether the Apple Device Enrollment program is enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableDep, Enabled

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
Specifies, as a **PSCredential** object, a Microsoft Intune organizational account and password.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: Credentials, Credential

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMIntuneSubscriptionAndroidProperty](Set-CMIntuneSubscriptionAndroidProperty.md)

[Set-CMIntuneSubscriptionAppleProperty](Set-CMIntuneSubscriptionAppleProperty.md)

[Set-CMIntuneSubscriptionPassportForWorkProperty](Set-CMIntuneSubscriptionPassportForWorkProperty.md)

[Set-CMIntuneSubscriptionWindowsPhoneProperty](Set-CMIntuneSubscriptionWindowsPhoneProperty.md)

[Set-CMIntuneSubscriptionWindowsProperty](Set-CMIntuneSubscriptionWindowsProperty.md)
