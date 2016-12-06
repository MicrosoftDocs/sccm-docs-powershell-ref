---
external help file: AdminUI.PS.Alerts.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834239
schema: 2.0.0
ms.assetid: 128C4EA4-CC60-44F1-8074-17BAEDBF60C1
---

# Suspend-CMAlert

## SYNOPSIS
Suspends monitoring alerts.

## SYNTAX

### SearchByValueMandatory (Default)
```
Suspend-CMAlert -InputObject <IResultObject> [-Comment <String>] -SkipUntil <DateTime>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Suspend-CMAlert -Id <String> [-Comment <String>] -SkipUntil <DateTime> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Suspend-CMAlert -Name <String> [-Comment <String>] -SkipUntil <DateTime> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Suspend-CMAlert** cmdlet suspends monitoring of an alert until a specified date.
At that time, Microsoft System Center Configuration Manager updates the state of the alert.
You can suspend an alert only when it is enabled.
If you do not specify the *SkipUntil* parameter, the alert is suspended indefinitely.

## EXAMPLES

### Example 1: Suspend an alert by using ID
```
PS C:\>Suspend-CMAlert -Id "16777219" -Comments "Postponing alert evaluation" -SkipUntil "Wednesday, August 20, 2012 4:03:17 PM"
```

This command suspends an alert that has the Id 16777219 until the time specified by *SkipUntil*, and adds a comment to the alert.

### Example 2: Suspend an alert by using alert object variable
```
PS C:\>$AlertObj = Get-CMAlert -Id "16777221"
PS C:\> Suspend-CMAlert -InputObject $AlertObj -Comments "Postponing alert evaluation" -SkipUntil "4/8/2012 8:04:39 PM"
```

The first command gets the alert object that has the ID 16777221, and then stores the object in the $AlertObj variable.

The second command suspends the alert stored in $AlertObj until the time specified by *SkipUntil*, and adds a comment to the alert.

## PARAMETERS

### -Comment
Specifies a comment to add to the alert.
You can use the comment to record the explanation for suspending the alert.

```yaml
Type: String
Parameter Sets: (All)
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Specifies an alert ID.
You can obtain the ID of an alert by using the [Get-CMAlert](./Get-CMAlert.md) cmdlet.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMAlert** object.
To obtain a **CMAlert** object, use the **Get-CMAlert** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Alert
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of an alert.
You can obtain the name of an alert by using **Get-CMAlert**.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipUntil
Specifies a specific date and time to start evaluation of the alert.
Enter a **DateTime** object or a string that can be converted to a time, such as April 19, 2012 15:00, 12/31/2013 9:00 PM, or 3am.
To obtain a **DateTime** object, use the **Get-Date** cmdlet.
For more information, type `Get-Help Get-Date`.

If you do not specify an element of the **DateTime** object, such as seconds, that element of the job trigger is not changed.
If the original job trigger did not include a **DateTime** object and you omit an element, the job trigger is created with the corresponding element from the current date and time.

**DateTime** objects, and strings that are converted to **DateTime** objects, are automatically adjusted to be compatible with the date and time formats selected for the local computer in **Region and Language** in Control Panel.

```yaml
Type: DateTime
Parameter Sets: (All)
<<<<<<< HEAD
Aliases:

=======
Aliases: 
>>>>>>> master
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

[Enable-CMAlert](./Enable-CMAlert.md)

[Get-CMAlert](./Get-CMAlert.md)

[Remove-CMAlert](./Remove-CMAlert.md)

[Set-CMAlert](./Set-CMAlert.md)

[Disable-CMAlert](./Disable-CMAlert.md)
