---
description: Restores a previous version of a Configuration Manager application from the application revision history.
external help file: AdminUI.PS.AppMan.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Restore-CMApplicationRevisionHistory
---

# Restore-CMApplicationRevisionHistory

## SYNOPSIS
Restores a previous version of a Configuration Manager application from the application revision history.

## SYNTAX

### SearchByValueMandatory (Default)
```
Restore-CMApplicationRevisionHistory [-InputObject] <IResultObject> [-Revision] <UInt32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySingleNameMandatory
```
Restore-CMApplicationRevisionHistory [-Name] <String> [-Revision] <UInt32> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySingleIdMandatory
```
Restore-CMApplicationRevisionHistory [-Id] <UInt32> [-Revision] <UInt32> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Restore-CMApplicationRevisionHistory** cmdlet restores a previous version of a Microsoft System Center Configuration Manager application.
You can use the revision history that System Center Configuration Manager creates and maintains for each application to choose the version of the application that you want to restore.

If you restore an application version from the history, System Center Configuration Manager might automatically replace currently installed copies of the application the next time it evaluates the deployment schedule.
For more control over application replacement, create a new application that supersedes the application that you want to replace, and then deploy this application to the required collection.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Restore an application
```
PS XYZ:\> Restore-CMApplicationRevisionHistory -Name "MSXML 6.0 Parser" -Revision 6.05
```

This command restores the application MSXML 6.0 Parser, version 6.05.

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
Specifies an array of IDs of application revision histories.

```yaml
Type: UInt32
Parameter Sets: SearchBySingleIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an object that contains an application revision history.
To get this object, use the Get-CMApplicationRevisionHistory cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Application

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of application revision histories.

```yaml
Type: String
Parameter Sets: SearchBySingleNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -Revision
Specifies the version number of the application revision that you restore.

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMApplicationRevisionHistory](Get-CMApplicationRevisionHistory.md)

[Remove-CMApplicationRevisionHistory](Remove-CMApplicationRevisionHistory.md)
