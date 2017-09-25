---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: 8C04D094-EAB1-4579-A0BF-51394304F2FD
online version: https://go.microsoft.com/fwlink/?linkid=833838
schema: 2.0.0
---

# Get-CMResource

## SYNOPSIS
Gets a resource.

## SYNTAX

```
Get-CMResource [[-ResourceId] <Int32>] [-Fast] [-ResourceType <ResourceType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMResource** cmdlet gets a resource.
A resource can be a user or a device.

## EXAMPLES

### Example 1: Get a resource by ID
```
PS C:\> Get-CMResource -ResourceID 2097152000 -Fast
```

This command gets the resource with the ID 2097152000.
It does not return lazy properties.

### Example 2: Get all user resources
```
PS C:\> Get-CMResource -ResourceType User -Fast
```

This command gets all user resources.
It does not return lazy properties.

## PARAMETERS

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

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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

### -ResourceId
Specifies the ID of a resource.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType
Specifies the resource type.
Valid values are: 

- None
- UnknownResource
- UserGroup
- User
- System

```yaml
Type: ResourceType
Parameter Sets: (All)
Aliases: 
Accepted values: None, UnknownResource, UserGroup, User, System

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

### IResultObject#SMS_Resource

## NOTES

## RELATED LINKS

[Remove-CMResource](Remove-CMResource.md)


