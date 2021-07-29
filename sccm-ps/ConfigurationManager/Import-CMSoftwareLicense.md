---
description: Imports a software license.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Import-CMSoftwareLicense
---

# Import-CMSoftwareLicense

## SYNOPSIS
Imports a software license.

## SYNTAX

```
Import-CMSoftwareLicense -ImportType <ImportType> -MlsFilePath <String> [-Timeout <TimeSpan>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMSoftwareLicense** cmdlet imports Microsoft and non-Microsoft licensing information into the Asset Intelligence catalog in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import a software license
```
PS XYZ:\>Import-CMSoftwareLicense -MlsFilePath "\\ContosoFS01\Mid\SWLicense01.xml" -ImportType MicrosftVolumeLicenseStatement
```

This command imports a MVLS license statement from the licensing information file named SWLicense01.xml.

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

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

### -ImportType
Specifies an import type for the software license.
The acceptable values for this parameter are: GeneralLicenseStatement and MicrosoftVolumeLicenseStatement.

A general license statement contains information about the purchased licenses for any publisher.
A Microsoft Volume License Statement (MVLS) license statement contains information about the license entitlements, or number of purchased licenses, for Microsoft products.

```yaml
Type: ImportType
Parameter Sets: (All)
Aliases:
Accepted values: MicrosoftVolumeLicenseStatement, GeneralLicenseStatement

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MlsFilePath
Specifies the Universal Naming Convention (UNC) path of a valid XML-formatted licensing information file.

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

### -Timeout
{{ Fill Timeout Description }}

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
