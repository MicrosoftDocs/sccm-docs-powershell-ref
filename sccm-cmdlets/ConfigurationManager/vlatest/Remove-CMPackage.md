---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834159
schema: 2.0.0
ms.assetid: 48839870-57C3-4450-B538-67066B32E2A3
---

# Remove-CMPackage

## SYNOPSIS
Removes a Configuration Manager package.

## SYNTAX

### SearchByValue (Default)
```
Remove-CMPackage -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMPackage -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMPackage -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMPackage** cmdlet removes a package in Microsoft System Center Configuration Manager.
You can delete a package from the site where it was created.
System Center Configuration Manager cannot delete a package from a distribution point if a user has locked a network file.

When you remove a package, System Center Configuration Manager removes it from the database.
If the package was sent to child sites, System Center Configuration Manager removes the package information at those child sites.
If a compressed version of source files for the package exists, System Center Configuration Manager deletes the compressed file from the site server.

## EXAMPLES

### Example 1: Remove a package
```
PS C:\>Remove-CMPackage -Id "CM10000D"
```

This command removes the package that has the ID CM10000D.

### Example 2: Remove a package by using an object variable
```
PS C:\>$Pkg = Get-CMPackage -Id "CM10000D"
PS C:\> Remove-CMPackage -InputObject $Pkg
```

The first command gets the package that has the ID CM10000D, and then stores the results to the $Pkg variable.

The second command removes the package stored in the $Pkg variable.

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

### -InputObject
Specifies a **CMPackage** object.
To obtain a **CMPackage** object, use the [Get-CMPackage](./Get-CMPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of package names.

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

[Export-CMPackage](./Export-CMPackage.md)

[Get-CMPackage](./Get-CMPackage.md)

[Import-CMPackage](./Import-CMPackage.md)

[New-CMPackage](./New-CMPackage.md)

[Set-CMPackage](./Set-CMPackage.md)


