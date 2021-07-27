---
description: Gets a Configuration Manager object that represents the revision history for an application.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMApplicationRevisionHistory
---

# Get-CMApplicationRevisionHistory

## SYNOPSIS
Gets a Configuration Manager object that represents the revision history for an application.

## SYNTAX

### SearchBySingleNameMandatory (Default)
```
Get-CMApplicationRevisionHistory [-Name] <String> [-Revision <UInt32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySingleIdMandatory
```
Get-CMApplicationRevisionHistory -Id <Int32> [-Revision <UInt32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMApplicationRevisionHistory -InputObject <IResultObject> [-Revision <UInt32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMApplicationRevisionHistory** cmdlet gets a Configuration Manager object that represents the revision history for an application.
When you revise an application or a deployment type contained in an application, Configuration Manager creates a new revision of the application.
You can use the revision history to display each revision made to an application, view the properties of a revision, restore a previous revision, or delete an old revision.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the revision history for an application
```
PS XYZ:\> Get-CMApplicationRevisionHistory -Name "MSXML 6.0 Parser"
```

This command gets the application revision history named MSXML 6.0 Parser.

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

### -Id
Specifies an array of IDs of application revision histories.

```yaml
Type: Int32
Parameter Sets: SearchBySingleIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application object.
To obtain an application object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Application

Required: True
Position: Named
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

### -Revision
Specifies the version number of an application revision.

```yaml
Type: UInt32
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_Application
### IResultObject#SMS_Application
## NOTES

## RELATED LINKS

[Remove-CMApplicationRevisionHistory](Remove-CMApplicationRevisionHistory.md)

[Restore-CMApplicationRevisionHistory](Restore-CMApplicationRevisionHistory.md)


