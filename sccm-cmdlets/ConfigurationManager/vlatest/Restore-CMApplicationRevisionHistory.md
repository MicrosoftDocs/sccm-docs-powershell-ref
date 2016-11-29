---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834300
schema: 2.0.0
ms.assetid: C76A60B1-D65B-4F19-BD71-E96060E497AA
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

## EXAMPLES

### Example 1: Restore an application
```
PS C:\>Restore-CMApplicationRevisionHistory -Name "MSXML 6.0 Parser" -Revision 6.05
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

### -Id


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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMApplicationRevisionHistory](./Get-CMApplicationRevisionHistory.md)

[Remove-CMApplicationRevisionHistory](./Remove-CMApplicationRevisionHistory.md)


