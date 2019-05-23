---
external help file: AdminUI.PS.Collections-help.xml
ms.assetid: 8AD90CCA-3F40-4D64-8FD9-C9028A0E15E7
online version: https://go.microsoft.com/fwlink/?linkid=833980
schema: 2.0.0
---

# Get-CMUserCollection

## SYNOPSIS
Gets one or more user collections in the Configuration Manager hierarchy.

## SYNTAX

### ByName (Default)
```
Get-CMUserCollection [-Name <String>] [<CommonParameters>]
```

### ById
```
Get-CMUserCollection -Id <String> [<CommonParameters>]
```

### ByDPGroupName
```
Get-CMUserCollection -DistributionPointGroupName <String> [<CommonParameters>]
```

### ByDPGroupId
```
Get-CMUserCollection -DistributionPointGroupId <String> [<CommonParameters>]
```

### ByDPGroup
```
Get-CMUserCollection -DistributionPointGroup <IResultObject> [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMUserCollection** cmdlet retrieves collections that contain users in Microsoft System Center Configuration Manager.
For more information about collections, see [Introduction to Collections in Configuration Manager](http://go.microsoft.com/fwlink/p/?LinkID=259433) on TechNet.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get a user collection
```
PS XYZ:\> Get-CMUserCollection -CollectionId "9990000D"
```

This command gets the user collection that has the ID 9990000D.

## PARAMETERS

### -DistributionPointGroup
```yaml
Type: IResultObject
Parameter Sets: ByDPGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupId
```yaml
Type: String
Parameter Sets: ByDPGroupId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
```yaml
Type: String
Parameter Sets: ByDPGroupName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
```yaml
Type: String
Parameter Sets: ById
Aliases: CollectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: ByName
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

[New-CMUserCollection](New-CMUserCollection.md)


