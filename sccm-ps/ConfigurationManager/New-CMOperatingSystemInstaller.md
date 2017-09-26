---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: 5FA48701-395D-4A6C-BE90-B6A3B5D010FA
online version: https://go.microsoft.com/fwlink/?linkid=833713
schema: 2.0.0
---

# New-CMOperatingSystemInstaller

## SYNOPSIS
Adds an operating system installer.

## SYNTAX

```
New-CMOperatingSystemInstaller [-Name <String>] -Path <String> [-Description <String>] [-Version <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMOperatingSystemInstaller** cmdlet adds an operating system installer to a Microsoft System Center Configuration Manager site.
An operating system installer is an installation package that contains all the files that Microsoft System Center Configuration Manager needs to install a Windows operating system on a reference computer.

## EXAMPLES

### Example 1: Add an operating system installer
```
PS C:\> New-CMOperatingSystemInstaller -Name "INSTALL01" -Path "\\Contoso01\CM\Win8Install"
```

This command adds an operating system installer named INSTALL01 and specifies the network path to the installation source files of the operating system installer.

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

### -Description
Specifies a description for an operating system installer.

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

### -Name
Specifies a name of the operating system installer.

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

### -Path
Specifies the network path to the installation source files of an operating system installer.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Version
Specifies the version of an operating system installer.

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

[Get-CMOperatingSystemInstaller](Get-CMOperatingSystemInstaller.md)

[Remove-CMOperatingSystemInstaller](Remove-CMOperatingSystemInstaller.md)

[Set-CMOperatingSystemInstaller](Set-CMOperatingSystemInstaller.md)


