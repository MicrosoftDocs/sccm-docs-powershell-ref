---
external help file: AdminUI.PS.Migration.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833722
schema: 2.0.0
ms.assetid: 34B1F9D6-3D89-46FF-AA23-A9B40E4433B0
---

# Get-CMInitialModifiableSecuredCategory

## SYNOPSIS
Gets modifiable secured categories.

## SYNTAX

### SearchById (Default)
```
Get-CMInitialModifiableSecuredCategory [-Id <String>] [-ObjectTypeId <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByName
```
Get-CMInitialModifiableSecuredCategory [-ObjectTypeId <String>] [-Name <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMInitialModifiableSecuredCategory** cmdlet gets modifiable secured categories from Configuration Manager.

Note: This cmdlet was previously known as **Get-CMInitModifiableSecuredCategory** in System Center 2012 Configuration Manager SP1.

## EXAMPLES

### Example 1: Get information about all your modifiable secured categories
```
PS C:\>Get-CMInitialModifiableSecuredCategory
```

This command returns information about all your modifiable secured categories.

### Example 2: Get information about a specific modifiable secured category
```
PS C:\>Get-CMInitialModifiableSecuredCategory -ID "121989"
```

This command returns information about the modifiable secured category that has the ID 121989.

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
Specifies an identifier in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: CategoryId
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name in Configuration Manager.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CategoryName
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ObjectTypeId
Specifies an ID for an object type.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[ConfMgr2016_Cmdlets](./ConfigurationManager.md)


