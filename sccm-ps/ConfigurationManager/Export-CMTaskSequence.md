---
description: Export a task sequence.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Export-CMTaskSequence
---

# Export-CMTaskSequence

## SYNOPSIS

Export a task sequence.

## SYNTAX

### SearchPackageByNameMandatory (Default)
```
Export-CMTaskSequence [-Comment <String>] -ExportFilePath <String> [-Force] -Name <String>
 [-WithContent <Boolean>] [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMTaskSequence [-Comment <String>] -ExportFilePath <String> [-Force] -InputObject <IResultObject>
 [-WithContent <Boolean>] [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchPackageByIdMandatory
```
Export-CMTaskSequence [-Comment <String>] -ExportFilePath <String> [-Force] -TaskSequencePackageId <String>
 [-WithContent <Boolean>] [-WithDependence <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to export a task sequence from Configuration Manager. You can use the [Import-CMTaskSequence](Import-CMTaskSequence.md) cmdlet to import a task sequence to another site.

> [!IMPORTANT]
> This cmdlet doesn't support [PowerShell 7](/powershell/sccm/overview#support-for-powershell-version-7).<!-- 6337796 --> It requires the .NET Framework instead of .NET Core that's used with PowerShell version 7.
>
> Starting in version 2103, if you try to use this cmdlet in a PowerShell version 7 session, it fails with the following error: `This cmdlet only supports the ".NET Framework" runtime.`

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a task sequence and export it

The first command gets the task sequence object named TaskSequence01 and stores the object in the $TaskSequence variable.

The second command exports the task sequence stored in $TaskSequence to the specified location.

```powershell
$TaskSequence = Get-CMTaskSequence -Name "TaskSequence01"
Export-CMTaskSequence -InputObject $TaskSequence -ExportFilePath "\\Server1\TS\TaskSequence01.zip"
```

### Example 2: Get a task sequence and use the pipeline to export it

This command gets the task sequence object named TaskSequence02 and uses the pipeline operator to pass the object to **Export-CMTaskSequence**, which exports the task sequence object to the specified location.

```powershell
Get-CMTaskSequence -Name "TaskSequence02" | Export-CMTaskSequence -ExportFilePath "\\Server1\TS\TaskSequence02.zip"
```

## PARAMETERS

### -Comment

Specify an optional administrator comment. This comment displays in the Import Task Sequence Wizard.

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

### -ExportFilePath

Specify the network path for the task sequence. The path needs to specify the file, including the `.zip` extension.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FileName, FilePath, Path

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Run the command without asking for confirmation.

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

### -InputObject

Specify a task sequence object to export. To get this object, use the [Get-CMTaskSequence](Get-CMTaskSequence.md) cmdlet.

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

Specify the name of a task sequence to export.

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

Specify the task sequence ID to export. This value is the standard package ID, for example `XYZ00123`.

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

### -WithContent

Set this parameter to **$true** to export all content for the task sequence and dependencies.

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

Set this parameter to **$true** to export all task sequence dependencies.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMTaskSequence](New-CMTaskSequence.md)
[Get-CMTaskSequence](Get-CMTaskSequence.md)
[Set-CMTaskSequence](Set-CMTaskSequence.md)
[Copy-CMTaskSequence](Copy-CMTaskSequence.md)
[Import-CMTaskSequence](Import-CMTaskSequence.md)
[Remove-CMTaskSequence](Remove-CMTaskSequence.md)
