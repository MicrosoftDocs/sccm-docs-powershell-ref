---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834271
schema: 2.0.0
ms.assetid: 3717A6BD-D2E1-435B-8A8E-F3AF9B632108
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

Microsoft System Center Configuration Manager updates configuration items based on configuration management, software updates management, and operating system deployment.
Configuration Manager stores the previous version of the item.
The server removes previous versions, by default, when the data is more than 90 days old.

This cmdlet gets the history of an item for a specified item name.
This cmdlet also gets the history for a specified revision of an item.

## EXAMPLES

### Example 1: Get item history by name
```
PS C:\>Get-CMConfigurationItemHistory -Name "CMCI07"
```

This command gets the history for a configuration item named CMCI07.

### Example 2: Get item history by ID
```
PS C:\>Get-CMConfigurationItemHistory -Id "16777568"
```

This command gets the previous version of a configuration item with the specified ID.

## PARAMETERS

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
To obtain a configuration item object, use the [Get-CMConfigurationItem](./Get-CMConfigurationItem.md) cmdlet.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Export-CMConfigurationItem](./Export-CMConfigurationItem.md)

[Get-CMConfigurationItem](./Get-CMConfigurationItem.md)

[Get-CMConfigurationItemXMLDefinition](./Get-CMConfigurationItemXMLDefinition.md)

[Remove-CMConfigurationItem](./Remove-CMConfigurationItem.md)

[Set-CMConfigurationItem](./Set-CMConfigurationItem.md)


