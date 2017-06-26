---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: 38B9CB0B-A9F5-4F3A-A89A-550B7DE849C3
online version: https://go.microsoft.com/fwlink/?linkid=834079
schema: 2.0.0
---

# Remove-CMDriver

## SYNOPSIS
Removes a device driver from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMDriver -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMDriver -Id <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMDriver -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMDriver** cmdlet removes a device driver from the Driver Catalog.
The source is not affected.

## EXAMPLES

### Example 1: Remove a driver specified by a driver object
```
PS C:\> $Driver = Get-CMDriver -Name "Driver01"
PS C:\> Remove-CMDriver -InputObject $Driver -Force
```

The first command gets the driver object named Driver01 and stores the object in the $Driver variable.

The second command removes the driver stored in $Driver.
Specifying the *Force* parameter indicates that the user is not prompted before the driver is removed.

### Example 2: Remove a driver by using the pipeline
```
PS C:\> Get-CMDriver -Name "Driver02" | Remove-CMDriver -Force
```

This command gets the driver object named Driver02 and uses the pipeline operator to pass the object to **Remove-CMDriver**, which removes the driver object.
Specifying the *Force* parameter indicates that the user is not prompted before the driver is removed.

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

### -Id
Specifies the ID of a driver.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a driver object.
To obtain a driver object, use the [Get-CMDriver](./Get-CMDriver.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a driver.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

Required: True
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

[Disable-CMDriver](./Disable-CMDriver.md)

[Enable-CMDriver](./Enable-CMDriver.md)

[Get-CMDriver](./Get-CMDriver.md)

[Import-CMDriver](./Import-CMDriver.md)

[Set-CMDriver](./Set-CMDriver.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)


