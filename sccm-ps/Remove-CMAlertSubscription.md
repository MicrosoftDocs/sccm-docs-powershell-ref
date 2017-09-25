---
external help file: AdminUI.PS.Alerts.dll-Help.xml
ms.assetid: AE138881-AB53-4272-B017-A936FD3DBF4C
online version: https://go.microsoft.com/fwlink/?linkid=833882
schema: 2.0.0
---

# Remove-CMAlertSubscription

## SYNOPSIS
Removes an alert subscription object.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAlertSubscription -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMAlertSubscription -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMAlertSubscription -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAlertSubscription** cmdlet removes an alert subscription from Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Remove an alert subscription by ID
```
PS C:\> Remove-CMAlertSubscription -Id "16777310"
```

This command removes an alert subscription by using its ID.

### Example 2: Remove an alert subscription by name
```
PS C:\> Remove-CMAlertSubscription -Name "Subscription01"
```

This command removes an alert subscription named Subscription01.

### Example 3: Remove an alert subscription by using the output from another cmdlet
```
PS C:\> $SubObj = Get-CMAlertSubscription -Id "16777310"
PS C:\> Remove-CMAlertSubscription -AlertSubscription $SubObj
```

The first command gets an alert subscription object that has the ID 16777310, and then stores the object in the $SubObj variable.

The second command deletes the alert subscription in $SubObj.

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
Specifies the ID of an alert subscription.

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
Specifies an alert notification object in Configuration Manager.

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
Specifies the name of an alert subscription.

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

[New-CMAlertSubscription](New-CMAlertSubscription.md)

[Get-CMAlertSubscription](Get-CMAlertSubscription.md)

[Set-CMAlertSubscription](Set-CMAlertSubscription.md)


