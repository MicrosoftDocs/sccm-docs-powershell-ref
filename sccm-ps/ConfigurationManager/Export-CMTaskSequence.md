---
author: mumian
description: Exports a Configuration Manager task sequence.
external help file: AdminUI.PS.Osd.dll-Help.xml
manager: dougeby
Module Name: ConfigurationManager
ms.author: jgao
ms.date: 11/30/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
schema: 2.0.0
title: Export-CMTaskSequence
titleSuffix: Configuration Manager
---

# Export-CMTaskSequence

## SYNOPSIS

Exports a Configuration Manager task sequence.

## SYNTAX

### SearchPackageByNameMandatory (Default)
```
Export-CMTaskSequence -Name <String> -ExportFilePath <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMTaskSequence -InputObject <IResultObject> -ExportFilePath <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Export-CMTaskSequence -TaskSequencePackageId <String> -ExportFilePath <String> [-WithDependence <Boolean>]
 [-WithContent <Boolean>] [-Comment <String>] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Export-CMTaskSequence** cmdlet exports a Microsoft System Center Configuration Manager task sequence to a .zip file.

## EXAMPLES

### Example 1: Get a task sequence and export it

```powershell
PS XYZ:\> $TaskSequence = Get-CMTaskSequence -Name "TaskSequence01"
PS XYZ:\> Export-CMTaskSequence -InputObject $TaskSequence -ExportFilePath "\\Server1\TS\TaskSequence01.zip"
```

The first command gets the task sequence object named TaskSequence01 and stores the object in the $TaskSequence variable.

The second command exports the task sequence stored in $TaskSequence to the specified location.

### Example 2: Get a task sequence and use the pipeline to export it

```powershell
PS XYZ:\> Get-CMTaskSequence -Name "TaskSequence02" | Export-CMTaskSequence -ExportFilePath "\\Server1\TS\TaskSequence02.zip"
```

This command gets the task sequence object named TaskSequence02 and uses the pipeline operator to pass the object to **Export-CMTaskSequence**, which exports the task sequence object to the specified location.

## PARAMETERS

### -Comment

Specifies a comment for the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

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

### -ExportFilePath

Specifies a path for the exported .zip file.

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

### -InputObject

Specifies a task sequence object.
To obtain a task sequence object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies a name for the task sequence.

```yaml
Type: String
Parameter Sets: SearchPackageByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequencePackageId

Specifies the ID of a task sequence.

```yaml
Type: String
Parameter Sets: SearchPackageByIdMandatory
Aliases: PackageId, Id

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

### -WithContent

Indicates whether to include content associated with the task sequence in the export .zip file.

If you specify a value of $True, the cmdlet copies the content from the package source to the export location, and uses the import path as the new package source location.

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

### -WithDependence

Indicates whether to include dependencies in the export .zip file.

Specify a value of $True to scan for all the related objects and export them with the task sequence that includes any dependencies for applications.
To export only the task sequence XML without the other referenced objects, set this parameter to $False.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[New-CMTaskSequence](Get-CMTaskSequence.md)
[Get-CMTaskSequence](Get-CMTaskSequence.md)
[Set-CMTaskSequence](Set-CMTaskSequence.md)
[Copy-CMTaskSequence](Copy-CMTaskSequence.md)
[Enable-CMTaskSequence](Enable-CMTaskSequence.md)
[Disable-CMTaskSequence](Disable-CMTaskSequence.md)
[Import-CMTaskSequence](Import-CMTaskSequence.md)
[Export-CMTaskSequence](Export-CMTaskSequence.md)
[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
