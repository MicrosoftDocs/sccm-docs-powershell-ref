---
description: Gets the previous versions of a configuration item in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/29/2018
schema: 2.0.0
title: Get-CMConfigurationItemHistory
---

# Get-CMConfigurationItemHistory

## SYNOPSIS

Gets the previous versions of a configuration item in Configuration Manager.

## SYNTAX

### SearchByNameMandatoryNoWildcards (Default)
```
Get-CMConfigurationItemHistory [-Name] <String> [-Revision <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMConfigurationItemHistory [-Id] <Int32> [-Revision <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMConfigurationItemHistory [-InputObject] <IResultObject> [-Revision <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMConfigurationItemHistory** cmdlet gets the previous versions of a configuration item.

Configuration Manager updates configuration items based on configuration management, software updates management, and operating system deployment.
Configuration Manager stores the previous version of the item.
The server removes previous versions, by default, when the data is more than 90 days old.

This cmdlet gets the history of an item for a specified item name.
This cmdlet also gets the history for a specified revision of an item.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get item history by name

```powershell
PS XYZ:\> Get-CMConfigurationItemHistory -Name "CMCI07"
```

This command gets the history for a configuration item named CMCI07.

### Example 2: Get item history by ID

```powershell
PS XYZ:\> Get-CMConfigurationItemHistory -Id "16777568"
```

This command gets the previous version of a configuration item with the specified ID.

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

Specifies an ID for a configuration item revision.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies a configuration item object.
To obtain a configuration item object, use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies an array of names of configuration items.

```yaml
Type: String
Parameter Sets: SearchByNameMandatoryNoWildcards
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Revision

Specifies the version of a configuration item as an integer.

```yaml
Type: Int32
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

### IResultObject[]#SMS_ConfigurationItem
### IResultObject#SMS_ConfigurationItem
## NOTES

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](/mem/configmgr/compliance/understand/ensure-device-compliance)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](Get-CMConfigurationItemXMLDefinition.md)

[New-CMConfigurationItem](New-CMConfigurationItem.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)
