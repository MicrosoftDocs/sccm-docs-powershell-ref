---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: BECE8291-8231-49F6-B161-C95BD24AC705
online version: https://go.microsoft.com/fwlink/?linkid=833588
schema: 2.0.0
---

# New-CMCollection

## SYNOPSIS
Creates a Configuration Manager collection.

## SYNTAX

### ByName (Default)
```
New-CMCollection -CollectionType <CollectionType> [-Comment <String>] -LimitingCollectionName <String>
 -Name <String> [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValue
```
New-CMCollection -CollectionType <CollectionType> [-Comment <String>] -InputObject <IResultObject>
 -Name <String> [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
New-CMCollection -CollectionType <CollectionType> [-Comment <String>] -LimitingCollectionId <String>
 -Name <String> [-RefreshSchedule <IResultObject>] [-RefreshType <CollectionRefreshType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMCollection** cmdlet creates a collection in Microsoft System Center Configuration Manager.

Configuration Manager collections provide a way to manage users, computers, and other resources in your organization. They not only give you a means to organize your resources, but they also give you a means to distribute Configuration Manager packages to clients and users.

## EXAMPLES

### Example 1: Create a collection and specify its scope
```
PS C:\> New-CMCollection -CollectionType User -LimitingCollectionName "All Users" -Name "testUser"
```

This command creates a user collection named testUser that establishes the All Users collection as the scope from which you can add members.

### Example 2: Create a collection based on an existing one
```
PS C:\> Get-CMCollection -Name "All Users" | New-CMCollection -Name "testUser" -CollectionType "User"
```

This command gets the collection object named All Users and uses the pipeline operator to pass the object to **New-CMCollection**.
**New-CMCollection** creates a collection named testUser that is based on the membership of the All Users collection.

## PARAMETERS

### -CollectionType
Specifies a type for the collection.
Valid values are:

- Root
- User
- Device
- Unknown

```yaml
Type: CollectionType
Parameter Sets: (All)
Aliases: 
Accepted values: User, Device

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Comment
Specifies a comment for the collection.

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

### -InputObject
Specifies a collection object to use as a scope for this collection.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: LimitingCollection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LimitingCollectionId
Specifies the ID of a collection to use as a scope for this collection.

```yaml
Type: String
Parameter Sets: ById
Aliases: LimitToCollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LimitingCollectionName
Specifies the name of a collection to use as a scope for this collection.

```yaml
Type: String
Parameter Sets: ByName
Aliases: LimitToCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the collection.

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

### -RefreshSchedule
Specifies a schedule that determines when Configuration Manager refreshes the collection.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshType
Specifies how Configuration Manager refreshes the collection.
Valid values are:

- None
- Manual
- Periodic
- Continuous
- Both

```yaml
Type: CollectionRefreshType
Parameter Sets: (All)
Aliases: 
Accepted values: None, Manual, Periodic, Continuous, Both

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

### IResultObject#SMS_Collection

## NOTES

## RELATED LINKS

[Export-CMCollection](Export-CMCollection.md)

[Get-CMCollection](Get-CMCollection.md)

[Import-CMCollection](Import-CMCollection.md)

[Remove-CMCollection](Remove-CMCollection.md)

[Set-CMCollection](Set-CMCollection.md)


