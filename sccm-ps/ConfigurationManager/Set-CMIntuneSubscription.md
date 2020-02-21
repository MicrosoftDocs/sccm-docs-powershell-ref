---
author: aczechowski
description: Sets the properties of a Microsoft Intune subscription in Configuration Manager.
external help file: AdminUI.PS.Hybrid.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: Set-CMIntuneSubscription
titleSuffix: Configuration Manager
---

# Set-CMIntuneSubscription

## SYNOPSIS
Sets the properties of a Microsoft Intune subscription in Configuration Manager.

## SYNTAX

```
Set-CMIntuneSubscription [-ColorScheme <Color>] [-CompanyLogoPath <String>] [-CompanyLogoThemedPath <String>]
 [-CompanyName <String>] [-CompanyNameWithLogo <Boolean>] [-ContactAdditional <String>]
 [-ContactEmail <String>] [-ContactName <String>] [-ContactPhoneNumber <String>] [-MaximumUserDevice <Int32>]
 [-MultifactorEnabled <Boolean>] [-NoCompanyLogo] [-OnPremOnly <Boolean>] [-PassThru] [-PrivacyUrl <String>]
 [-SupportSiteName <String>] [-SupportUrl <String>] [-UserCollection <IResultObject>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMIntuneSubscription** cmdlet sets the properties of a Microsoft Intune subscription in Microsoft System Center Configuration Manager.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Set the properties for a Microsoft Intune subscription
```
PS XYZ:\> Set-CMIntuneSubscription -ContactAdditional "Contact Additional Information" -ContactEmail "ITContact@Contoso.com" -ContactPhoneNumber "123456789"
```

This command adds an IT contact email, phone number, and additional information to the Microsoft Intune subscription for the site.

## PARAMETERS

### -ColorScheme
Specifies a color scheme for the company portal.

```yaml
Type: Color
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CompanyLogoPath
Specifies the path to the company logo to use when the company portal background is white.

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

### -CompanyLogoThemedPath
Specifies the path to the company logo to use when the company portal background has a color scheme.

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

### -CompanyName
Specifies a company name.

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

### -CompanyNameWithLogo
Indicates whether the company name is displayed next to the company logo.

```yaml
Type: Boolean
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

### -ContactAdditional
Specifies additional company contact information.

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

### -ContactEmail
Specifies the IT department email address.

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

### -ContactName
Specifies the IT department contact name.

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

### -ContactPhoneNumber
Specifies the IT department phone number.

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

### -MaximumUserDevice
Specifies the maximum number of devices that a user can enroll.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MultifactorEnabled
Indicates whether multi-factor authentication is enabled.
This applies to Windows 8.1 or later and Windows Phone 8.1 or later device enrollment.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoCompanyLogo
Indicates that the company logo is not included on the company portal.

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

### -OnPremOnly
Indicates whether only devices on premises are managed.
Information from devices on premises do not replicate to the cloud.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

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

### -PrivacyUrl
Specifies the URL to company privacy documentation.

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

### -SupportSiteName
Specifies the name of the support website.
The website name is displayed to users.

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

### -SupportUrl
Specifies the URL to the support website.
The URL is not displayed to users.

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

### -UserCollection
Specifies a user collection.
To obtain a user collection object, use the [Get-CMUserCollection](Get-CMUserCollection.md) or [Get-CMCollection](Get-CMCollection.md) cmdlet.
Members of this user collection will be able to enroll their devices for management.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Collection

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

[Add-CMIntuneSubscription](Add-CMIntuneSubscription.md)

[Get-CMCollection](Get-CMCollection.md)

[Get-CMIntuneSubscription](Get-CMIntuneSubscription.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Remove-CMIntuneSubscription](Remove-CMIntuneSubscription.md)
