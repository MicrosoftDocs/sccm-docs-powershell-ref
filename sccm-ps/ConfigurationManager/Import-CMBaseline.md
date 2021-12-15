---
description: Imports Configuration Manager baselines.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Import-CMBaseline
---

# Import-CMBaseline

## SYNOPSIS
Imports Configuration Manager baselines.

## SYNTAX

```
Import-CMBaseline [-DuplicateWhileImporting] -FileName <String[]> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMBaseline** cmdlet imports Configuration Manager baselines from files.
A baseline is a collection of configuration items that Configuration Manager uses to evaluate whether a computer complies with software requirements.
After you import a baseline, you can deploy it to a collection so that devices in that collection download the configuration baseline and assess compliance with it.

You can import a configuration baseline from a .cab file that conforms to the Service Modeling Language (SML) schema.
For example, you might import data previously exported from Configuration Manager or best practices included in a Monitoring Pack for Configuration Manager.

When you import a baseline configuration, you have the option of creating a local copy.
You can modify that baseline in the future.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import a baseline
```
PS XYZ:\>Import-CMBaseline -FileName "\\ContosoServer01\Public\CM\BaselineW2K8.cab"
```

This command imports a baseline from a file named BaselineW2K8.cab.

### Example 2: Import multiple baselines
```
PS XYZ:\>Import-CMBaseline -FileName "\\ContosoServer01\Public\CM\BaselineW2K8.cab","\\ContosoServer01\Public\CM\BaselineWin7.cab" -DuplicateWhileImporting
```

This command imports baselines from .cab files named BaselineW2K8.cab and BaselineWin7.cab.
This command uses the *DuplicateWhileImporting* parameter, so the command creates an editable version of the configuration baselines.

## PARAMETERS

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

### -DuplicateWhileImporting
Indicates that the cmdlet duplicates a baseline while it imports the baseline.
If you duplicate a baseline, you can modify that baseline in the future.

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
Specifies an array of .cab file names.
Each file contains Configuration Manager configuration items.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: FilePath, ImportFilePath, Path, FileNames, FilePaths, ImportFilePaths, Paths

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

[Disable-CMBaseline](Disable-CMBaseline.md)

[Enable-CMBaseline](Enable-CMBaseline.md)

[Export-CMBaseline](Export-CMBaseline.md)

[Get-CMBaseline](Get-CMBaseline.md)

[New-CMBaseline](New-CMBaseline.md)

[Remove-CMBaseline](Remove-CMBaseline.md)

[Set-CMBaseline](Set-CMBaseline.md)


