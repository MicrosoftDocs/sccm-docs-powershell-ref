---
description: Gets Configuration Manager global condition objects.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/07/2019
schema: 2.0.0
title: Get-CMGlobalCondition
---

# Get-CMGlobalCondition

## SYNOPSIS

Gets Configuration Manager global condition objects.

## SYNTAX

### SearchByName (Default)
```
Get-CMGlobalCondition [-AsDcmSdkObject] [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMGlobalCondition [-AsDcmSdkObject] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMGlobalCondition** cmdlet gets global condition objects.
You can pass the results of this cmdlet to the **Set-CMGlobalCondition** cmdlet or the **Remove-CMGlobalCondition** cmdlet.

Configuration Manager uses global conditions to represent business or technical conditions.
Global conditions specify how to provide and deploy applications to client devices.

You can get global conditions by name, ID, or security scope.
You can also specify one or more security scope names with either names or IDs.
For instance, you might specify an array of global condition names and specify a security scope to narrow your results.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a global condition by name

```powershell
PS XYZ:\> Get-CMGlobalCondition -Name "CPU speed"
```

This command gets the global condition named CPU speed.

### Example 2: Get a global condition by id (CI_ID)

```powershell
PS XYZ:\> $test = Get-CMGlobalCondition -Id 16777504
        $test.CI_ID
```

## PARAMETERS

### -AsDcmSdkObject

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

Specifies an array of identifiers of global conditions.
This value corresponds to the **CI_ID** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specifies an array of names for global conditions.
This value corresponds to the **LocalizedDisplayName** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_GlobalCondition
### IResultObject#SMS_GlobalCondition
### ConfigurationItem
## NOTES

## RELATED LINKS

[New-CMGlobalCondition](./Get-CMGlobalCondition.md)

[Set-CMGlobalCondition](./Set-CMGlobalCondition.md)

[Remove-CMGlobalCondition](./Remove-CMGlobalCondition.md)
