---
description: Changes settings for a Configuration Manager configuration item.
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 11/29/2018
schema: 2.0.0
title: Set-CMConfigurationItem
---

# Set-CMConfigurationItem

## SYNOPSIS

Changes settings for a Configuration Manager configuration item.

## SYNTAX

### SetByIdMandatory (Default)
```
Set-CMConfigurationItem [-Id] <Int32> [-NewName <String>] [-Description <String>] [-AddCategory <String[]>]
 [-RemoveCategory <String[]>] [-DigestPath <String>] [-DigestXml <String>] [-Digest <ConfigurationItem>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMConfigurationItem [-Name] <String> [-NewName <String>] [-Description <String>] [-AddCategory <String[]>]
 [-RemoveCategory <String[]>] [-DigestPath <String>] [-DigestXml <String>] [-Digest <ConfigurationItem>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMConfigurationItem [-InputObject] <IResultObject> [-NewName <String>] [-Description <String>]
 [-AddCategory <String[]>] [-RemoveCategory <String[]>] [-DigestPath <String>] [-DigestXml <String>]
 [-Digest <ConfigurationItem>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Set-CMConfigurationItem** cmdlet changes settings for a Microsoft System Center Configuration Manager configuration item.

Configuration items contain one or more settings, along with compliance rules.
Items usually define a unit of configuration you want to monitor.
For more information about configuration items, see [Introduction to Compliance Settings in Configuration Manager](/previous-versions/system-center/system-center-2012-R2/gg682139(v=technet.10)) on TechNet.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Change the name of a configuration item

```powershell
PS XYZ:\> Set-CMConfigurationItem -Name "CITest" -NewName "CITest01"
```

This command changes the name of the configuration item named CITest to CITest01.

### Example 2: Set item settings

```powershell
PS XYZ:\> Set-CMConfigurationItem -Name "CITest01" -SecurityScopeAction AddMembership -SecurityScopeName "DefaultScope"
```

This command sets the security scope action to AddMembership and the security scope name to DefaultScope for the item named CITest01.

### Example 3: Change item settings

```powershell
PS XYZ:\> Set-CMConfigurationItem -Name "CITest01" -SecurityScopeAction RemoveMembership -SecurityScopeName "DefaultScope"
```

This command sets the security scope action to RemoveMembership and the security scope name to DefaultScope for the item named CITest01.

## PARAMETERS

### -AddCategory

Specifies an array of localized names of the categories to which the configuration item belongs.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specifies a description for a configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Digest

Specifies the Digest that contain the configuration item.

```yaml
Type: ConfigurationItem
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DigestPath

Specifies the path of the Digest.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DesiredConfigurationDigestPath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DigestXml

Specifies the XML definition.

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

Specifies an array of identifiers for one or more configuration items.
You can use a comma separated list.

```yaml
Type: Int32
Parameter Sets: SetByIdMandatory
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
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specifies an array of names for configuration items.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specifies a new name for a configuration item.

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

### -PassThru

Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -RemoveCategory

Specifies an array of localized names of the categories from which to remove the configuration item.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

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

[Remove-CMConfigurationItem](Remove-CMConfigurationItem.md)

[Import-CMConfigurationItem](Import-CMConfigurationItem.md)

[Export-CMConfigurationItem](Export-CMConfigurationItem.md)

[ConvertTo-CMConfigurationItem](ConvertTo-CMConfigurationItem.md)

[ConvertFrom-CMConfigurationItem](ConvertFrom-CMConfigurationItem.md)
