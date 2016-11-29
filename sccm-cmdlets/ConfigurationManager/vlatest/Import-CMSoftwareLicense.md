---
external help file: AdminUI.PS.AssetIntelligence.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834078
schema: 2.0.0
ms.assetid: 7B354232-530E-4DD6-A439-4183A9320EE3
---

# Import-CMSoftwareLicense

## SYNOPSIS
Imports a software license.

## SYNTAX

```
Import-CMSoftwareLicense -MlsFilePath <String> -ImportType <ImportType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMSoftwareLicense** cmdlet imports Microsoft and non-Microsoft licensing information into the Asset Intelligence catalog in Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Import a software license
```
PS C:\>Import-CMSoftwareLicense -MlsFilePath "\\ContosoFS01\Mid\SWLicense01.xml" -ImportType MicrosftVolumeLicenseStatement
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


