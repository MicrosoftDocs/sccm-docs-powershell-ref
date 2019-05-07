---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: 60C6778B-12CB-4F15-846D-3B8ED4AC58A8
online version: https://go.microsoft.com/fwlink/?linkid=834230
schema: 2.0.0
---

# Get-CMCollectionMember

## SYNOPSIS
Gets a member of a Configuration Manager collection.

## SYNTAX

### ByCollectionName (Default)
```
Get-CMCollectionMember -CollectionName <String> [-Name <String>] [-SmsId <String>] [-ResourceId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollectionId
```
Get-CMCollectionMember -CollectionId <String> [-Name <String>] [-SmsId <String>] [-ResourceId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByCollection
```
Get-CMCollectionMember -InputObject <IResultObject> [-Name <String>] [-SmsId <String>] [-ResourceId <Int32>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMCollectionMember** cmdlet gets a member of a Microsoft System Center Configuration Manager collection. Configuration Manager collections provide a way to manage users, computers, and other resources in your organization.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get a member of a collection by using the pipeline operator
```
PS XYZ:\> Get-CMCollection -Name "UserCol1" | Get-CMCollectionMember
```

This command gets the collection object named UserCol1 and uses the pipeline operator to pass the object to **Get-CMCollectionMember**, which gets all members in UserCol1.

### Example 2: Get a member of a collection by name
```
PS XYZ:\> Get-CMCollectionMember -CollectionName "DeviceCol1" -Name "domain*"
```

This command gets the all members of the device collection named DeviceCol1 that have a name beginning with domain.

## PARAMETERS

### -CollectionId
Specifies the ID of a collection.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName
Specifies the name of a collection.

```yaml
Type: String
Parameter Sets: ByCollectionName
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
To obtain a collection object, use the Get-CMCollection, Get-CMDeviceCollection or Get-CMUserCollection cmdlets.

```yaml
Type: IResultObject
Parameter Sets: ByCollection
Aliases: Collection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a resource.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the ID of a resource.

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

### -SmsId
Specifies the SMSID of a resource.

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

[Get-CMCollection](Get-CMCollection.md)

[Get-CMDeviceCollection](Get-CMDeviceCollection.md)

[Get-CMUserCollection](Get-CMUserCollection.md)


