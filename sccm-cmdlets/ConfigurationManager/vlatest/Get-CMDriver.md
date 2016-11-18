---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 2B68441B-3BDC-44EF-9546-BC931AEE22CB
---

# Get-CMDriver

## SYNOPSIS
Gets a device driver.

## SYNTAX

### SearchByName (Default)
```
Get-CMDriver [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDriver -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDriverPackageIdMandatory
```
Get-CMDriver -DriverPackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDriverPackageNameMandatory
```
Get-CMDriver -DriverPackageName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDriverPackage
```
Get-CMDriver -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDriver** cmdlet gets a device driver.

## EXAMPLES

### Example 1: Get a device driver
```
PS C:\>Get-CMDriver -Name "Driver01"
```

This command gets the driver named Driver01.

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

### -DriverPackageId
Specifies the ID of a driver package.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DriverPackageName
Specifies the name of a driver package.

```yaml
Type: String
Parameter Sets: SearchByDriverPackageNameMandatory
Aliases: PackageName

Required: True
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
Specifies the ID of a driver.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, DriverId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a driver package object.
To obtain a driver package object, use the Get-CMDriverPackage cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByDriverPackage
Aliases: DriverPackage

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
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName, DriverName

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

[Disable-CMDriver](./Disable-CMDriver.md)

[Enable-CMDriver](./Enable-CMDriver.md)

[Import-CMDriver](./Import-CMDriver.md)

[Remove-CMDriver](./Remove-CMDriver.md)

[Set-CMDriver](./Set-CMDriver.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)


