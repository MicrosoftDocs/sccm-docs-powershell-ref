---
external help file: AdminUI.PS.Content.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834072
schema: 2.0.0
ms.assetid: 6633EFD1-D89B-4115-B23E-0A0A71BF5C02
---

# Remove-CMDistributionPointFromGroup

## SYNOPSIS
Removes a Configuration Manager distribution point from a distribution point group.

## SYNTAX

### RemoveDistributionPointFromGroupByObject_Object (Default)
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPoint <IResultObject>
 -DistributionPointGroup <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### RemoveDistributionPointFromGroupById_Object
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPointId <String>
 -DistributionPointGroup <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### RemoveDistributionPointFromGroupById_Id
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPointId <String> -DistributionPointGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDistributionPointFromGroupById_Name
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPointId <String> -DistributionPointGroupName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDistributionPointFromGroupByName_Object
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPointName <String>
 -DistributionPointGroup <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### RemoveDistributionPointFromGroupByName_Id
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPointName <String> -DistributionPointGroupId <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveDistributionPointFromGroupByName_Name
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPointName <String>
 -DistributionPointGroupName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDistributionPointFromGroupByObject_Name
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPoint <IResultObject>
 -DistributionPointGroupName <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### RemoveDistributionPointFromGroupByObject_Id
```
Remove-CMDistributionPointFromGroup [-Force] -DistributionPoint <IResultObject>
 -DistributionPointGroupId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDistributionPointFromGroup** cmdlet removes a Microsoft System Center Configuration Manager distribution point from a distribution point group.
Distribution point groups provide a logical grouping of distribution points for content distribution.

To remove a distribution point, specify both the distribution point to remove and the distribution point group.
You can specify these values by ID or name, or you can use the Get-CMDistributionPoint cmdlet or the Get-CMDistributionPointGroup cmdlet to obtain the relevant object.

## EXAMPLES

### Example 1: Remove a distribution point by using an ID
```
PS C:\>Remove-CMDistributionPointFromGroup -DistributionPointGroupId "SMS000067" -DistributionPointId "SMS000022"
```

This command removes a distribution point that has an ID of SMS000022 from a distribution point group that has the ID SMS000067.

### Example 2: Remove a distribution point by using a name
```
PS C:\>Remove-CMDistributionPointFromGroup -DistributionPointGroupId "SMS000067" -DistributionPointName "Western office distribution point" -Force
```

This command removes a distribution point, specified by its name, from a distribution point group that has the ID SMS000067.
This command uses the *Force* parameter, therefore, it does not prompt you before it removes the distribution point.

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

### -DistributionPoint
Specifies a distribution point object.
To obtain a distribution point object, use the **Get-CMDistributionPoint** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveDistributionPointFromGroupByObject_Object, RemoveDistributionPointFromGroupByObject_Name, RemoveDistributionPointFromGroupByObject_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroup
Specifies a distribution point group object.
To obtain a distribution point group object, use the **Get-CMDistributionPointGroup** cmdlet.

```yaml
Type: IResultObject
Parameter Sets: RemoveDistributionPointFromGroupByObject_Object, RemoveDistributionPointFromGroupById_Object, RemoveDistributionPointFromGroupByName_Object
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DistributionPointGroupId
Specifies the ID of a distribution point group.

```yaml
Type: String
Parameter Sets: RemoveDistributionPointFromGroupById_Id, RemoveDistributionPointFromGroupByName_Id, RemoveDistributionPointFromGroupByObject_Id
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointGroupName
Specifies the name of a distribution point group.

```yaml
Type: String
Parameter Sets: RemoveDistributionPointFromGroupById_Name, RemoveDistributionPointFromGroupByName_Name, RemoveDistributionPointFromGroupByObject_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointId
Specifies the ID of a distribution point.

```yaml
Type: String
Parameter Sets: RemoveDistributionPointFromGroupById_Object, RemoveDistributionPointFromGroupById_Id, RemoveDistributionPointFromGroupById_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DistributionPointName
Specifies the name of a distribution point.

```yaml
Type: String
Parameter Sets: RemoveDistributionPointFromGroupByName_Object, RemoveDistributionPointFromGroupByName_Id, RemoveDistributionPointFromGroupByName_Name
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

[Add-CMDistributionPointToGroup](./Add-CMDistributionPointToGroup.md)

[Get-CMDistributionPoint](./Get-CMDistributionPoint.md)

[Get-CMDistributionPointGroup](./Get-CMDistributionPointGroup.md)


