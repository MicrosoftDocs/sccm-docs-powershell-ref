---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: 80157719-BA02-42AD-9ACE-03D9112E3956
online version: https://go.microsoft.com/fwlink/?linkid=833902
schema: 2.0.0
---

# Remove-CMApplicationRevisionHistory

## SYNOPSIS
Removes a revision history from a Configuration Manager application.

## SYNTAX

### SearchByRevisionMandatory (Default)
```
Remove-CMApplicationRevisionHistory -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySingleNameMandatory
```
Remove-CMApplicationRevisionHistory -Name <String> [-Force] -Revision <UInt32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMApplicationRevisionHistory -InputObject <IResultObject> [-Force] -Revision <UInt32>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySingleIdMandatory
```
Remove-CMApplicationRevisionHistory [-Force] -Id <UInt32> -Revision <UInt32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMApplicationRevisionHistory** cmdlet removes a revision history from a Microsoft System Center Configuration Manager application.
The revision history contains a list of revisions to an application or a development type that the application contains.

## EXAMPLES

### Example 1: Remove a revision history
```
PS C:\> Remove-CMApplicationRevisionHistory -Name "MSXML 6.0 Parser"
```

This command removes the revision history named MSXML 6.0 Parser.

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

### -Id
Specifies an array of IDs that identify the application revision histories that you delete.

```yaml
Type: UInt32
Parameter Sets: SearchBySingleIdMandatory
Aliases: CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application object.
To get an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByRevisionMandatory, SearchByValueMandatory
Aliases: ApplicationRevision

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names for the application revision histories that you delete.

```yaml
Type: String
Parameter Sets: SearchBySingleNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Revision
Specifies the version number of the revision that you delete from the history.

```yaml
Type: UInt32
Parameter Sets: SearchBySingleNameMandatory, SearchByValueMandatory, SearchBySingleIdMandatory
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

[Get-CMApplicationRevisionHistory](Get-CMApplicationRevisionHistory.md)

[Restore-CMApplicationRevisionHistory](Restore-CMApplicationRevisionHistory.md)


