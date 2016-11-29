---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834275
schema: 2.0.0
ms.assetid: 57EC8E6E-2E33-4198-966D-9A5E6A27D397
---

# Get-CMConfigurationItemXMLDefinition

## SYNOPSIS
Gets an XML definition of a configuration item in Configuration Manager.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMConfigurationItemXMLDefinition [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMConfigurationItemXMLDefinition [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMConfigurationItemXMLDefinition [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMConfigurationItemXMLDefinition** cmdlet gets an XML definition of a configuration item object as a string.
You can specify a configuration item with the configuration item ID, the configuration item name, or using the Get-CMConfigurationItem cmdlet.

## EXAMPLES

### Example 1: Get XML formatted item using an ID
```
PS C:\>Get-CMConfigurationItemXMLDefinition -Id "16777568"
```

This command gets a configuration item formatted in XML for the item that has the specified identifier.

### Example 2: Get XML formatted item using a name
```
PS C:\>Get-CMConfigurationItemXMLDefinition -Name "ConfigItem76"
```

This command gets a configuration item formatted in XML for the item named ConfigItem76.

### Example 3: Get XML formatted item using a variable
```
PS C:\>$CIObj=Get-CMConfigurationItem -Id "16777568"
PS C:\> Get-CMConfigurationItemXMLDefinition -InputObject $CIObj
```

The first command uses the Get-CMConfigurationItem cmdlet to get a configuration item with the specified ID, and then stores it in the $CIObj variable.

The second command gets a configuration item formatted in XML for the item stored in $CIObj.

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
To get a configuration item object, use the Get-CMConfigurationItem cmdlet.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Export-CMConfigurationItem](./Export-CMConfigurationItem.md)

[Get-CMConfigurationItem](./Get-CMConfigurationItem.md)

[Get-CMConfigurationItemHistory](./Get-CMConfigurationItemHistory.md)

[Remove-CMConfigurationItem](./Remove-CMConfigurationItem.md)

[Set-CMConfigurationItem](./Set-CMConfigurationItem.md)


