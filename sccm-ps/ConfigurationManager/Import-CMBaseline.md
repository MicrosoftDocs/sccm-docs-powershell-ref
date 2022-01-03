---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Import-CMBaseline
---

# Import-CMBaseline

## SYNOPSIS

Import a configuration baseline.

## SYNTAX

```
Import-CMBaseline [-DuplicateWhileImporting] -FileName <String[]> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to import one or more configuration baselines from files.

You can import a configuration baseline from a cabinet (`.cab`) file that conforms to the Service Modeling Language (SML) schema.
For example, you might import data previously exported from Configuration Manager or included in a configuration pack from a vendor.

When you import a baseline configuration, you have the option of creating a local copy. You can then modify that baseline copy.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import a baseline

This command imports a baseline from a file named **BaselineW2K8.cab**.

```powershell
Import-CMBaseline -FileName "\\ContosoServer01\Public\CM\BaselineW2K8.cab"
```

### Example 2: Import multiple baselines

This command imports baselines from .cab files named **BaselineW2K8.cab** and **BaselineWin7.cab**.
It uses the **DuplicateWhileImporting** parameter, so it creates an editable version of the configuration baselines.

```powershell
Import-CMBaseline -FileName "\\ContosoServer01\Public\CM\BaselineW2K8.cab","\\ContosoServer01\Public\CM\BaselineWin7.cab" -DuplicateWhileImporting
```

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

Add this parameter to duplicate the baseline when it imports.
When you duplicate a baseline, you can then modify it.

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

Specify an array of cabinet (`.cab`) file names to import.

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
