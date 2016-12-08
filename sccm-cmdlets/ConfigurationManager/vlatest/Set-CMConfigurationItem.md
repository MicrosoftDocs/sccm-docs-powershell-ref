---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833767
schema: 2.0.0
ms.assetid: 51B2F354-3AD4-4A67-B567-E76938D445E5
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
For more information about configuration items, see [Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014) on TechNet.

## EXAMPLES

### Example 1: Change the name of a configuration item
```
PS C:\>Set-CMConfigurationItem -Name "CITest" -NewName "CITest01"
```

This command changes the name of the configuration item named CITest to CITest01.

### Example 2: Set item settings
```
PS C:\>Set-CMConfigurationItem -Name "CITest01" -SecurityScopeAction AddMembership -SecurityScopeName "DefaultScope"
```

This command sets the security scope action to AddMembership and the security scope name to DefaultScope for the item named CITest01.

### Example 3: Change item settings
```
PS C:\>Set-CMConfigurationItem -Name "CITest01" -SecurityScopeAction RemoveMembership -SecurityScopeName "DefaultScope"
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
To obtain a configuration item object, you can use the [Get-CMConfigurationItem](./Get-CMConfigurationItem.md) cmdlet.

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
Returns an object representing the item with which you are working.
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

[Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014)

[Export-CMConfigurationItem](./Export-CMConfigurationItem.md)

[Get-CMConfigurationItem](./Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](./Get-CMConfigurationItemXMLDefinition.md)

[Import-CMConfigurationItem](./Import-CMConfigurationItem.md)

[New-CMConfigurationItem](./New-CMConfigurationItem.md)

[Remove-CMConfigurationItem](./Remove-CMConfigurationItem.md)

[Get-CMConfigurationItemHistory](./Get-CMConfigurationItemHistory.md)
