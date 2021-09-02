---
description: Suspends monitoring alerts.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Suspend-CMAlert
---

# Suspend-CMAlert

## SYNOPSIS
Suspends monitoring alerts.

## SYNTAX

### SearchByValueMandatory (Default)
```
Suspend-CMAlert [-Comment <String>] -InputObject <IResultObject> [-PassThru] -SkipUntil <DateTime>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Suspend-CMAlert [-Comment <String>] -Id <String> [-PassThru] -SkipUntil <DateTime> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Suspend-CMAlert [-Comment <String>] -Name <String> [-PassThru] -SkipUntil <DateTime> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Suspend-CMAlert** cmdlet suspends monitoring of an alert until a specified date.
At that time, Configuration Manager updates the state of the alert.
You can suspend an alert only when it is enabled.
If you do not specify the *SkipUntil* parameter, the alert is suspended indefinitely.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Suspend an alert by using ID
```
PS XYZ:\> Suspend-CMAlert -Id "16777219" -Comments "Postponing alert evaluation" -SkipUntil "Wednesday, August 20, 2012 4:03:17 PM"
```

This command suspends an alert that has the Id 16777219 until the time specified by *SkipUntil*, and adds a comment to the alert.

### Example 2: Suspend an alert by using alert object variable
```
PS XYZ:\> $AlertObj = Get-CMAlert -Id "16777221"
PS XYZ:\> Suspend-CMAlert -InputObject $AlertObj -Comments "Postponing alert evaluation" -SkipUntil "4/8/2012 8:04:39 PM"
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
Aliases:

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
Parameter Sets: SearchByIdMandatory
Aliases:

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
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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
Aliases:

Required: True
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

[Set-CMAlert](Set-CMAlert.md)

[Disable-CMAlert](Disable-CMAlert.md)
