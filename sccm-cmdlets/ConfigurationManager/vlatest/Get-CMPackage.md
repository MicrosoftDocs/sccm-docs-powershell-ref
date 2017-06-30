---
external help file: AdminUI.PS.AppModel.dll-Help.xml
ms.assetid: 4D76D4D0-5D21-4320-BEA6-335CE01284A7
online version: https://go.microsoft.com/fwlink/?linkid=833809
schema: 2.0.0
---

# Get-CMPackage

## SYNOPSIS
Gets Configuration Manager packages.

## SYNTAX

### SearchByName (Default)
```
Get-CMPackage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMPackage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMPackage** cmdlet gets Microsoft System Center Configuration Manager packages.
System Center Configuration Manager uses packages to distribute software to clients.
You can use the *SecuredScopeNames* parameter to specify the security scope of a package to get.

## EXAMPLES

### Example 1: Get all packages
```
PS C:\> Get-CMPackage
```

This command gets all Configuration Manager packages.

### Example 2: Get a package by using an ID
```
PS C:\> Get-CMPackage -Id "CM100002"
```

This command gets the program that has the ID CM100002.

### Example 3: Get a package by using a name
```
PS C:\> Get-CMPackage -Name "Configuration Manager Client Package"
```

This command gets the program named Configuration Manager Client Package.

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
Specifies an array of package IDs.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a package.

```yaml
Type: String
Parameter Sets: SearchByName
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

[Export-CMPackage](./Export-CMPackage.md)

[Import-CMPackage](./Import-CMPackage.md)

[New-CMPackage](./New-CMPackage.md)

[Remove-CMPackage](./Remove-CMPackage.md)

[Set-CMPackage](./Set-CMPackage.md)


