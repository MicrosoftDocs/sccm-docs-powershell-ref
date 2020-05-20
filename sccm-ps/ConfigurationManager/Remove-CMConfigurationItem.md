---
description: Removes configuration items from Configuration Manager.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/29/2018
schema: 2.0.0
title: Remove-CMConfigurationItem
---

# Remove-CMConfigurationItem

## SYNOPSIS

Removes configuration items from Configuration Manager.

## SYNTAX

### SearchByIdMandatory (Default)
```
Remove-CMConfigurationItem [-Id] <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMConfigurationItem [-Name] <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMConfigurationItem [-InputObject] <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-CMConfigurationItem** cmdlet removes specified configuration items from Microsoft System Center Configuration Manager.
You can specify items by ID, name, or by use of the  cmdlet.

Configuration items contain one or more settings, along with compliance rules.
Items usually define a unit of configuration you want to.

If you remove a configuration item that has been deployed to a collection, the deployment will also be removed.

For more information about configuration items, see [Introduction to Compliance Settings in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682139(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Remove an item using an ID

```powershell
PS XYZ:\> Remove-CMConfigurationItem -Id "16777568"
```

This command removes a configuration item with the specified identifier.

### Example 2: Remove an item using a name

```powershell
PS XYZ:\> Remove-CMConfigurationItem -Name "ConfigItem76"
```

This command removes a configuration item named ConfigItem76.

### Example 3: Remove an item using a variable

```powershell
PS XYZ:\> $CIObj=Get-CMConfigurationItem -Id "16777568"
PS XYZ:\> Remove-CMConfigurationItem -InputObject $CIObj
```

The first command gets a configuration item with the specified identifier and stores it in the $CIObj variable.

The second command removes the item stored in the $CIObj variable.

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

Specifies an array of identifiers for one or more configuration items.
You can use a comma separated list.

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
To obtain a configuration item object, you can use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet.

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
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: 0
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

[Introduction to Compliance Settings in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682139(v=technet.10))

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](Get-CMConfigurationItemXMLDefinition.md)

[Get-CMConfigurationItemHistory](Get-CMConfigurationItemHistory.md)

[New-CMConfigurationItem](New-CMConfigurationItem.md)

[Set-CMConfigurationItem](Set-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)
