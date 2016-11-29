---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833604
schema: 2.0.0
ms.assetid: 3F7587DE-C592-49E8-8B14-8A9AA4DF93DC
---

# New-CMConfigurationItem

## SYNOPSIS
Creates a configuration item.

## SYNTAX

### NewChild (Default)
```
New-CMConfigurationItem -Name <String> [-Description <String>] [-Category <String[]>]
 -ParentConfigurationItem <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### New
```
New-CMConfigurationItem -Name <String> [-Description <String>] [-Category <String[]>]
 -CreationType <CICreationType> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMConfigurationItem** cmdlet creates a configuration item in Microsoft System Center Configuration Manager.
Create configuration items to define configurations that you want to manage and assess for compliance on devices.

You can specify the *ParentConfigurationItem* parameter to create a child configuration item.
Child configuration items in System Center Configuration Manager are copies of configuration items that retain a relationship to the original configuration item; therefore, they inherit the original configuration from the parent configuration item.
You cannot create child configuration items for mobile devices.

## EXAMPLES

### Example 1: Create a configuration item
```
PS C:\>New-CMConfigurationItem -CreationType MobileDevice -Name "MD_Config88"
```

This command creates a configuration item for mobile devices named MD_Config88.

## PARAMETERS

### -Category
Specifies an array of localized names of the categories to which the configuration item belongs.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: LocalizedCategoryInstanceNames

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

### -CreationType
Specifies the type of configuration item.
The acceptable values for this parameter are:

- MacOS
- MobileDevice
- None
- WindowsApplication
- WindowsOS

```yaml
Type: CICreationType
Parameter Sets: New
Aliases: 
Accepted values: None, WindowsApplication, WindowsOS, MacOS, MobileDevice

Required: True
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

### -Name
Specifies a name for the configuration item.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentConfigurationItem
Specifies a parent **CMConfigurationItem** object.
To obtain a **CMConfigurationItem** object, use the Get-CMConfigurationItem cmdlet.

```yaml
Type: IResultObject
Parameter Sets: NewChild
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

[Get-CMConfigurationItem](./Get-CMConfigurationItem.md)

[Set-CMConfigurationItem](./Set-CMConfigurationItem.md)

[Import-CMConfigurationItem](./Import-CMConfigurationItem.md)

[Remove-CMConfigurationItem](./Remove-CMConfigurationItem.md)

[Export-CMConfigurationItem](./Export-CMConfigurationItem.md)


