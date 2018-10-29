---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: 381B444E-D2CA-4351-9EDF-036291F23E7D
online version: https://go.microsoft.com/fwlink/?linkid=833975
schema: 2.0.0
---

# Get-CMUser

## SYNOPSIS
Gets a Configuration Manager user.

## SYNTAX

### ByName (Default)
```
Get-CMUser [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValueMandatory
```
Get-CMUser -InputObject <IResultObject> [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMUser -CollectionId <String> [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Get-CMUser -CollectionName <String> [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ById
```
Get-CMUser -ResourceId <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUser** cmdlet gets a Microsoft System Center Configuration Manager user object.

## EXAMPLES

### Example 1: Get a user by name
```
PS C:\> Get-CMUser -CollectionName "All Users" -Name "Contoso\username01"
```

This command gets the user named username01 from the All Users collection.

### Example 2: Pass a collection and get a user from it
```
PS C:\> Get-CMCollection -Name "All Users" | Get-CMUser -Name "Contoso\testuser01"
```

This command gets the collection object named All Users and uses the pipeline operator to pass the object to **Get-CMUser**, which gets the user named testuser01 from the collection object.

## PARAMETERS

### -CollectionId
Specifies the ID of a user collection.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a user collection.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: True
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

### -InputObject
Specifies a collection object.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a user.

```yaml
Type: String
Parameter Sets: ByName, SearchByValueMandatory, SearchByIdMandatory, SearchByNameMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the resource ID of a user.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: Id, UserId

Required: True
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

[Add-CMUserCollectionDirectMembershipRule](Add-CMUserCollectionDirectMembershipRule.md)

[Get-CMCollection](Get-CMCollection.md)

[Get-CMUserCollection](Get-CMUserCollection.md)

[Remove-CMUser](Remove-CMUser.md)
