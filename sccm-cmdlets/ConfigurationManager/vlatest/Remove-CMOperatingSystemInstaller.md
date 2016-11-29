---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834151
schema: 2.0.0
ms.assetid: 3AA12DC1-E0BD-40C1-B5D3-3CB1C394045B
---

# Remove-CMOperatingSystemInstaller

## SYNOPSIS
Removes operating system installers.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMOperatingSystemInstaller -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMOperatingSystemInstaller -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMOperatingSystemInstaller -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMOperatingSystemInstaller** cmdlet removes one or more operating system installers from a Microsoft System Center Configuration Manager site.
An operating system installer is an installation package that contains all the files that System Center Configuration Manager needs to install a Windows operating system on a reference computer.

After you remove an operating system installer, you cannot distribute the installation source files that are associated with the operating system installer to distribution points.

## EXAMPLES

### Example 1: Remove an operating system installer
```
PS C:\>Remove-CMOperatingSystemInstaller -Name "INSTALL01"
```

This command removes the operating system installer named INSTALL01.

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
Specifies an array of IDs of operating system installers.

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
Specifies a **CMOperatingSystemInstaller** object.
To obtain a **CMOperatingSystemInstaller** object, use the Get-CMOperatingSystemInstaller cmdlet.

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
Specifies the name of an operating system installer.

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

[Get-CMOperatingSystemInstaller](./Get-CMOperatingSystemInstaller.md)

[New-CMOperatingSystemInstaller](./New-CMOperatingSystemInstaller.md)

[Set-CMOperatingSystemInstaller](./Set-CMOperatingSystemInstaller.md)


