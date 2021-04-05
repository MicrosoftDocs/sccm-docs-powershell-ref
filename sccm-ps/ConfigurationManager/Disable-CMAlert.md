---
description: Disables alerts in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/29/2019
schema: 2.0.0
title: Disable-CMAlert
---

# Disable-CMAlert

## SYNOPSIS

Disables alerts in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Disable-CMAlert -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Disable-CMAlert -Id <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Disable-CMAlert -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Disable-CMAlert** cmdlet disables one or more alerts in Configuration Manager.

Configuration Manager does not evaluate the condition for a disabled alert and does not update a disabled alert, even if the state of the alert changes.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Disable an alert by using alert ID

```powershell
PS XYZ:\>Disable-CMAlert -Id "16777218"
```

This command disables an alert that has the ID 16777218.

### Example 2: Disable an alert by using alert object variable

```powershell
PS XYZ:\> $AlertObj = Get-CMAlert -Id "16777221"
PS XYZ:\> Disable-CMAlert -InputObject $AlertObj
```

The first command gets an alert object that has the ID 16777221, and then stores it in the $AlertObj variable.

The second command disables the alert stored in the $AlertObj variable.

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
To obtain a **CMAlert** object, use **Get-CMAlert**.

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

[Suspend-CMAlert](Suspend-CMAlert.md)
