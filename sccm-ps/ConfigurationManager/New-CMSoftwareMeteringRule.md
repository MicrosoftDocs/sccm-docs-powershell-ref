---
author: aczechowski
description: Creates a Configuration Manager software metering rule.
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMSoftwareMeteringRule
titleSuffix: Configuration Manager
---

# New-CMSoftwareMeteringRule

## SYNOPSIS
Creates a Configuration Manager software metering rule.

## SYNTAX

### New (Default)
```
New-CMSoftwareMeteringRule -ProductName <String> [-FileName <String>] [-OriginalFileName <String>]
 [-FileVersion <String>] [-LanguageId <Int32>] [-Comment <String>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewFromPath
```
New-CMSoftwareMeteringRule [-ProductName <String>] [-SiteCode <String>] -Path <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMSoftwareMeteringRule** cmdlet creates a Microsoft System Center Configuration Manager software metering rule.
A software metering rule specifies a piece of software, along with version information.
You can obtain necessary file information from Windows Explorer.

Software metering monitors and collects software usage data from System Center Configuration Manager clients, such as when clients began using a particular software program and how long users have worked with that software.
You can create software metering rules that specify which software to monitor.

For more information about software metering in System Center Configuration Manager, see [Introduction to Software Metering in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682005(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a software metering rule
```
PS XYZ:\> New-CMSoftwareMeteringRule -Path "Notepad.exe" -SiteCode "CM1" -FileVersion "6.1.7600.16385" -OriginalFileName "NOTEPAD.EXE" -ProductName "Microsoft Windows Operating System"
ApplyToChildSites : True
Comment           :
Enabled           : True
FileName          : Notepad.exe
FileVersion       : 6.1.7600.16385
LanguageID        :
LastUpdateTime    :
OriginalFileName  : NOTEPAD.EXE
ProductName       : Microsoft Windows Operating System
RuleID            :
SecurityKey       :
SiteCode          : CM1
SourceSite        :
```

This command creates a software metering rule for the System Center Configuration Manager site named CM1.
The command specifies the file name, version, original file name, and product name for the software product.

## PARAMETERS

### -Comment
Specifies a comment for a software metering rule.

```yaml
Type: String
Parameter Sets: New
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

### -FileName
```yaml
Type: String
Parameter Sets: New
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileVersion
Specifies a version of the software that a rule meters.

```yaml
Type: String
Parameter Sets: New
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

### -LanguageId
Specifies a LocaleID of the software that a rule meters.
For more information and a list of locale identifiers, see the Locale IDs Assigned by Microsoft topic at [https://go.microsoft.com/fwlink/?LinkId=262651](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).

```yaml
Type: Int32
Parameter Sets: New
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OriginalFileName
Specifies an original file name of the software that a rule meters.
This parameter can differ from the *Path* parameter if a user changed the name.

```yaml
Type: String
Parameter Sets: New
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies a file path of the software that a rule meters.

```yaml
Type: String
Parameter Sets: NewFromPath
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductName
Specifies a name for a product that a rule meters.

```yaml
Type: String
Parameter Sets: New
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: NewFromPath
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a site code for a Configuration Manager site.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Disable-CMSoftwareMeteringRule](Disable-CMSoftwareMeteringRule.md)

[Enable-CMSoftwareMeteringRule](Enable-CMSoftwareMeteringRule.md)

[Get-CMSoftwareMeteringRule](Get-CMSoftwareMeteringRule.md)

[Remove-CMSoftwareMeteringRule](Remove-CMSoftwareMeteringRule.md)

[Set-CMSoftwareMeteringRule](Set-CMSoftwareMeteringRule.md)


