---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834249
schema: 2.0.0
ms.assetid: E7E7069A-5044-431D-8906-91031BCBB6F3
---

# Remove-CMTaskSequence

## SYNOPSIS
Removes a task sequence.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMTaskSequence -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMTaskSequence -TaskSequencePackageId <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMTaskSequence -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMTaskSequence** cmdlet removes a task sequence from Microsoft System Center Configuration Manager.

NOTE:  All related deployments are automatically removed.

## EXAMPLES

### Example 1: Remove a task sequence by using a variable
```
PS C:\>$TaskSequence = Get-CMTaskSequence -Name "TaskSequence01"
PS C:\> Remove-CMTaskSequence -InputObject $TaskSequence -Force
Remove
Are you sure you wish to remove TaskSequence: Name="General Sequence 11"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"):
```

The first command gets the task sequence object named TaskSequence01 and stores the object in the $TaskSequence variable.

The second command removes the task sequence object stored in $TaskSequence.
Specifying the *Force* parameter indicates that the user is not prompted before the task sequence is removed.

### Example 2: Remove a task sequence by using the pipeline
```
PS C:\>Get-CMTaskSequence -Name "TaskSequence02" | Remove-CMTaskSequence -Force
```

This command gets the task sequence object named TaskSequence02 and uses the pipeline operator to pass the object to **Remove-CMTaskSequence**, which removes the task sequence object.
Specifying the *Force* parameter indicates that the user is not prompted before the task sequence is removed.

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

### -InputObject
Specifies a task sequence object.
To obtain a task sequence object, use the Get-CMTaskSequence cmdlet.

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
Specifies a name of a task sequence.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequencePackageId
Specifies the package ID of a task sequence.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

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

[Disable-CMTaskSequence](./Disable-CMTaskSequence.md)

[Enable-CMTaskSequence](./Enable-CMTaskSequence.md)

[Export-CMTaskSequence](./Export-CMTaskSequence.md)

[Get-CMTaskSequence](./Get-CMTaskSequence.md)

[Import-CMTaskSequence](./Import-CMTaskSequence.md)

[New-CMTaskSequence](./New-CMTaskSequence.md)

[Set-CMTaskSequence](./Set-CMTaskSequence.md)


