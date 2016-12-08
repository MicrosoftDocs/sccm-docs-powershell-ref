---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834021
schema: 2.0.0
ms.assetid: E3CA1A74-5568-4635-B0FB-68C09ACCE911
---

# Export-CMConfigurationItem

## SYNOPSIS
Saves a Configuration Manager configuration item to a file.

## SYNTAX

### SearchByNameMandatory (Default)
```
Export-CMConfigurationItem [-Name] <String> -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Export-CMConfigurationItem [-Id] <Int32> -Path <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMConfigurationItem [-InputObject] <IResultObject> -Path <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMConfigurationItem** cmdlet saves a Microsoft System Center Configuration Manager configuration item to a specified .cab file.
You can specify items by ID, name, or by use of the [Get-CMConfigurationItem](./Get-CMConfigurationItem.md) cmdlet.

Configuration items contain one or more settings, along with compliance rules.
For more information about configuration items, see [Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014) on TechNet.

## EXAMPLES

### Example 1: Export an item using an ID
```
PS C:\>Export-CMConfigurationItem -Id "16777568" -Path "C:\Exports\CI16777568.cab"
```

This command exports a configuration item with the identifier named 16777568 to the specified file.

### Example 2: Export an item using a name
```
PS C:\>Export-CMConfigurationItem -Name "ConfigItem76" -Path "C:\Exports\CIConfigItem76.cab"
```

This command exports a configuration item named ConfigItem76 to the specified file.

### Example 3: Export an item using a variable
```
PS C:\> $CIObj=Get-CMConfigurationItem -Id "16777568"
PS C:\> Export-CMConfigurationItem -InputObject $CIObj -Path "C:\Exports\CI16777568.cab"
```

The first command gets a configuration item with the specified identifier and stores it in the $CIObj variable.

The second command exports the item in the $CIObj variable to the specified file.

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
To obtain a configuration item object, you can use the **Get-CMConfigurationItem** cmdlet.

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
You can use a comma separated list.

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

### -Path
Specifies a full file path for an export file.

```yaml
Type: String
Parameter Sets: (All)
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

[Introduction to Compliance Settings in Configuration Manager](http://go.microsoft.com/fwlink/?LinkId=211014)

[Get-CMConfigurationItem](./Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](./Get-CMConfigurationItemXMLDefinition.md)

[Import-CMConfigurationItem](./Import-CMConfigurationItem.md)

[New-CMConfigurationItem](./New-CMConfigurationItem.md)

[Remove-CMConfigurationItem](./Remove-CMConfigurationItem.md)

[Set-CMConfigurationItem](./Set-CMConfigurationItem.md)

[Get-CMConfigurationItemHistory](./Get-CMConfigurationItemHistory.md)


