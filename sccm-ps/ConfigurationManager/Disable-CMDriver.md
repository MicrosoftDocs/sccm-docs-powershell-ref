---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: DC4B2713-2B9D-45B0-A595-00407274F314
online version: https://go.microsoft.com/fwlink/?linkid=833945
schema: 2.0.0
---

# Disable-CMDriver

## SYNOPSIS
Disables a device driver.

## SYNTAX

### SearchByValueMandatory (Default)
```
Disable-CMDriver -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Disable-CMDriver -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Disable-CMDriver -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Disable-CMDriver** cmdlet disables a device driver in Microsoft System Center Configuration Manager.
To enable the driver, use the [Enable-CMDriver](Enable-CMDriver.md) cmdlet.

## EXAMPLES

### Example 1: Disable a device driver
```
PS C:\> $Driver = Get-CMDriver -Name "Driver01"
PS C:\> Disable-CMDriver -InputObject $Driver
```

The first command gets the driver object named Driver01 and stores the object in the $Driver variable.

The second command disables the driver stored in $Driver.

### Example 2: Disable a device driver by using the pipeline
```
PS C:\> Get-CMDriver -Name "Driver02" | Disable-CMDriver
```

This command gets the driver object named Driver02 and uses the pipeline operator to pass the object to **Disable-CMDriver**, which disables the driver object.

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
To obtain a driver object, use the [Enable-CMDriver](Enable-CMDriver.md) cmdlet.

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

[Enable-CMDriver](Enable-CMDriver.md)

[Import-CMDriver](Import-CMDriver.md)

[Get-CMDriver](Get-CMDriver.md)

[Remove-CMDriver](Remove-CMDriver.md)

[Set-CMDriver](Set-CMDriver.md)

[Get-CMDriverPackage](Get-CMDriverPackage.md)
