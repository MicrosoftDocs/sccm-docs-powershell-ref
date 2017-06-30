---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 077E0748-86A4-460E-B829-4A21A61664EF
online version: https://go.microsoft.com/fwlink/?linkid=833857
schema: 2.0.0
---

# Publish-CMPrestageContentTaskSequence

## SYNOPSIS
Distributes the content that a task sequence uses to a distribution point.

## SYNTAX

### SearchByValueMandatory_TaskSequence (Default)
```
Publish-CMPrestageContentTaskSequence -TaskSequence <IResultObject> [-IgnoreApplicationDependency]
 -FolderName <String> [-Description <String>] -DistributionPointName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory_TaskSequence
```
Publish-CMPrestageContentTaskSequence -TaskSequenceId <String[]> [-IgnoreApplicationDependency]
 -FolderName <String> [-Description <String>] -DistributionPointName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory_TaskSequence
```
Publish-CMPrestageContentTaskSequence -TaskSequenceName <String[]> [-IgnoreApplicationDependency]
 -FolderName <String> [-Description <String>] -DistributionPointName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Publish-CMPrestageContentTaskSequence** cmdlet distributes the content that a task sequence uses to a distribution point.
Optionally, you can exclude the application dependencies for applications indicated in the task sequence.

## EXAMPLES

### Example 1: Publish content required by a task sequence
```
PS C:\>Publish-CMPrestageContentTaskSequence -DistributionPointName "distribution-server.contoso.com" -FolderName "ToBePublished" -TaskSequenceName "ContosoDeploymentSequence"
```

This command copies content required by the task sequence ContosoDeploymentSequence to the distribution point distribution-server.contoso.com.

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

### -Description
Specifies a description for the content to prestage.

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

### -DistributionPointName
Specifies the name of a distribution point that is associated with the task sequence.

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

### -FolderName
Specifies a folder name.
The folder that you specify contains prestaged content files.

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

### -IgnoreApplicationDependency
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableIncludeApplicationDependencies, IgnoreApplicationDependencies

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequence
Specifies a task sequence object.
To obtain a task sequence object, use the [Get-CMTaskSequence](./Get-CMTaskSequence.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory_TaskSequence
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceId
Specifies an array of IDs of task sequences.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory_TaskSequence
Aliases: TaskSequenceIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName
Specifies an array of names of task sequences.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory_TaskSequence
Aliases: TaskSequenceNames

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

[Get-CMTaskSequence](./Get-CMTaskSequence.md)

[Publish-CMPrestageContent](./Publish-CMPrestageContent.md)


