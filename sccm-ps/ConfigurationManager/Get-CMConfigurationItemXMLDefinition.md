---
title: Get-CMConfigurationItemXMLDefinition
titleSuffix: Configuration Manager
description: Gets an XML definition of a configuration item in Configuration Manager.
ms.date: 11/29/2018
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby

external help file: AdminUI.PS.AppMan.dll-Help.xml
---

# Get-CMConfigurationItemXMLDefinition

## SYNOPSIS

Gets an XML definition of a configuration item in Configuration Manager.

## SYNTAX

### SearchByNameMandatory (Default)

```powershell
Get-CMConfigurationItemXMLDefinition [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory

```powershell
Get-CMConfigurationItemXMLDefinition [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValueMandatory

```powershell
Get-CMConfigurationItemXMLDefinition [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMConfigurationItemXMLDefinition** cmdlet gets an XML definition of a configuration item object as a string.
You can specify a configuration item with the configuration item ID, the configuration item name, or using the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get XML formatted item using an ID

```powershell
PS XYZ:\> Get-CMConfigurationItemXMLDefinition -Id "16777568"
```

This command gets a configuration item formatted in XML for the item that has the specified identifier.

### Example 2: Get XML formatted item using a name

```powershell
PS XYZ:\> Get-CMConfigurationItemXMLDefinition -Name "ConfigItem76"
```

This command gets a configuration item formatted in XML for the item named ConfigItem76.

### Example 3: Get XML formatted item using a variable

```powershell
PS XYZ:\> $CIObj=Get-CMConfigurationItem -Id "16777568"
PS XYZ:\> Get-CMConfigurationItemXMLDefinition -InputObject $CIObj
```

The first command uses the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet to get a configuration item with the specified ID, and then stores it in the $CIObj variable.

The second command gets a configuration item formatted in XML for the item stored in $CIObj.

## PARAMETERS

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

Specifies an array of IDs of configuration items.
You can use a comma-separated list.

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
To get a configuration item object, use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

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
You can use a comma-separated list.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

[Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014)

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemHistory](Get-CMConfigurationItemHistory.md)

[New-CMConfigurationItem](New-CMConfigurationItem.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)
