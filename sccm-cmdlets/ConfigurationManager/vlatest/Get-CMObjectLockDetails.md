---
external help file: AdminUI.PS.Common.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833781
schema: 2.0.0
ms.assetid: 2CA8797E-6B30-4B19-A6A5-7FC938EC28A4
---

# Get-CMObjectLockDetails

## SYNOPSIS
Gets object lock details.

## SYNTAX

```
Get-CMObjectLockDetails [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMObjectLockDetails** cmdlet gets the object lock details for an object.

## EXAMPLES

### Example 1: Get object lock details by passing an application object through the pipeline
```
PS ABC:\> Get-CMApplication -Name "Application01" | Get-CMObjectLockDetails
```

This command gets the application object named Application01 and uses the pipeline operator to pass the object to **Get-CMObjectLockDetails**, which gets the object lock details for the application.

### Example 2: Get object lock details by getting an application object
```
PS ABC:\> $AppObject = Get-CMApplication -Name "testApp"
PS ABC:\> Get-CMObjectLockDetails -InputObject $AppObject
```

The first command gets the application object named testApp and stores the object in the $AppObject variable.

The second object gets the object lock details for the application stored in $AppObject.

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

### -InputObject
Specifies a Configuration Manager object output from another cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Lock-CMObject](./Lock-CMObject.md)

[Unlock-CMObject](./Unlock-CMObject.md)
