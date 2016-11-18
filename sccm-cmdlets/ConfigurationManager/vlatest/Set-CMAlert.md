---
external help file: AdminUI.PS.Alerts.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 2DF24DAB-8C8C-4F9B-9E44-4CA624C522F3
---

# Set-CMAlert

## SYNOPSIS
Changes properties of Configuration Manager alerts.

## SYNTAX

### SetByValue (Default)
```
Set-CMAlert -InputObject <IResultObject> [-NewName <String>] [-Severity <Severities>]
 [-ParameterValue <String>] [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMAlert -Name <String> [-NewName <String>] [-Severity <Severities>] [-ParameterValue <String>]
 [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetById
```
Set-CMAlert -Id <String> [-NewName <String>] [-Severity <Severities>] [-ParameterValue <String>]
 [-Comment <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAlert** cmdlet changes the properties of one or more Microsoft System Center Configuration Manager alerts.

## EXAMPLES

### Example 1: Set alert properties
```
PS C:\>Set-CMAlert -Id "16777223" -Comments "Editing severity" -Severity 2
```

This command changes the values of the *Comments* and *Severity* properties for an alert that has the ID 16777223.

### Example 2: Set alert properties by using alert object variable
```
PS C:\>$AlertObj = Get-CMAlert -Id "16777221"
PS C:\> Set-CMAlert -InputObject $AlertObj -Comments "Updating alert"
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
Specifies an alert ID.
You can obtain the ID of an alert by using the Get-CMAlert cmdlet.

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

[Enable-CMAlert](./Enable-CMAlert.md)

[Get-CMAlert](./Get-CMAlert.md)

[Remove-CMAlert](./Remove-CMAlert.md)

[Suspend-CMAlert](./Suspend-CMAlert.md)

[Disable-CMAlert](./Disable-CMAlert.md)


