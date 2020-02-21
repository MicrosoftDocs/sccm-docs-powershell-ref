---
author: aczechowski
description: Creates an installation source file for Configuration Manager.
external help file: AdminUI.PS.HS.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: aaroncz
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
schema: 2.0.0
title: New-CMInstallationSourceFile
titleSuffix: Configuration Manager
---

# New-CMInstallationSourceFile

## SYNOPSIS
Creates an installation source file for Configuration Manager.

## SYNTAX

### NewInstallationSourceFilesByNetworkLocation (Default)
```
New-CMInstallationSourceFile [-CopyFromNetworkLocation] -UncPath <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewInstallationSourceFilesByParent
```
New-CMInstallationSourceFile [-CopyFromParentSiteServer] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewInstallationSourceFilesBySecondaryLocation
```
New-CMInstallationSourceFile [-CopyFromSecondarySiteLocation] -LocalPath <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMInstallationSourceFile** cmdlet creates an installation source file for Microsoft System Center Configuration Manager.
An installation source file is an object that contains installation source parameters for a secondary site installation.
A secondary site has no System Center Configuration Manager database of its own.
Instead, it forwards information that it gets from clients to a primary site that stores the data for all the secondary sites that are attached to it.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create an installation source file
```
PS XYZ:\> New-CMInstallationSourceFile -CopyFromParentSiteServer
```

This command creates an installation source file for a secondary site installation by copying the installation files from the primary site.

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

### -CopyFromNetworkLocation
Indicates that Configuration Manager copies the installation files for a secondary site installation from a specific Universal Naming Convention (UNC) path.

```yaml
Type: SwitchParameter
Parameter Sets: NewInstallationSourceFilesByNetworkLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CopyFromParentSiteServer
Indicates that Configuration Manager copies the installation files for a secondary site installation from the primary site.

```yaml
Type: SwitchParameter
Parameter Sets: NewInstallationSourceFilesByParent
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CopyFromSecondarySiteLocation
Indicates that the installation files for a secondary site installation reside on the secondary site server.

```yaml
Type: SwitchParameter
Parameter Sets: NewInstallationSourceFilesBySecondaryLocation
Aliases:

Required: True
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

### -LocalPath
Specifies a path to source files in the local file system of the secondary site server.

```yaml
Type: String
Parameter Sets: NewInstallationSourceFilesBySecondaryLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UncPath
Specifies a UNC path to source files in the local file system of the secondary site server.

```yaml
Type: String
Parameter Sets: NewInstallationSourceFilesByNetworkLocation
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
