---
description: Changes properties of Configuration Manager alerts.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMAlert
---

# Set-CMAlert

## SYNOPSIS
Changes properties of Configuration Manager alerts.

## SYNTAX

### SetByValue (Default)
```
Set-CMAlert [-Comment <String>] -InputObject <IResultObject> [-NewName <String>] [-ParameterValue <String>]
 [-Severity <Severities>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMAlert [-Comment <String>] -Id <String> [-NewName <String>] [-ParameterValue <String>]
 [-Severity <Severities>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByName
```
Set-CMAlert [-Comment <String>] -Name <String> [-NewName <String>] [-ParameterValue <String>]
 [-Severity <Severities>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAlert** cmdlet changes the properties of one or more Configuration Manager alerts.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set alert properties
```
PS XYZ:\> Set-CMAlert -Id "16777223" -Comments "Editing severity" -Severity 2
```

This command changes the values of the *Comments* and *Severity* properties for an alert that has the ID 16777223.

### Example 2: Set alert properties by using alert object variable
```
PS XYZ:\> $AlertObj = Get-CMAlert -Id "16777221"
PS XYZ:\> Set-CMAlert -InputObject $AlertObj -Comments "Updating alert"
```

The first command gets an alert object that has the ID 16777221, and then stores it in the $AlertObj variable.

The second command changes the *Comments* property of the alert stored in the $AlertObj variable.

## PARAMETERS

### -Comment
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
Specifies an alert ID.
You can obtain the ID of an alert by using the [Get-CMAlert](Get-CMAlert.md) cmdlet.

```yaml
Type: String
Parameter Sets: SetById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMAlert** object.
To obtain a **CMAlert** object, use **Get-CMAlert**.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: Alert

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an alert name.
You can obtain the name of an alert by using **Get-CMAlert**.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the alert.

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

### -ParameterValue
```yaml
Type: String
Parameter Sets: (All)
Aliases: ParameterValues

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Severity
Specifies the severity of an alert.
The acceptable values for this parameter are:

- 1: Error
- 2: Warning
- 3: Informational

```yaml
Type: Severities
Parameter Sets: (All)
Aliases:
Accepted values: Error, Warning, Informational

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

[Enable-CMAlert](Enable-CMAlert.md)

[Get-CMAlert](Get-CMAlert.md)

[Remove-CMAlert](Remove-CMAlert.md)

[Suspend-CMAlert](Suspend-CMAlert.md)

[Disable-CMAlert](Disable-CMAlert.md)


