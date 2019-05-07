---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: 1C8CA4A9-A212-4C8C-95ED-E51675AE2F1A
online version: https://go.microsoft.com/fwlink/?linkid=833798
schema: 2.0.0
---

# Get-CMOperatingSystemInstaller

## SYNOPSIS
Gets operating system installers.

## SYNTAX

### SearchByName (Default)
```
Get-CMOperatingSystemInstaller [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMOperatingSystemInstaller -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMOperatingSystemInstaller** cmdlet gets one or more operating system installers.
An operating system installer is an installation package that contains all the files that Microsoft System Center Configuration Manager needs to install a Windows operating system on a reference computer.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Get an operating system installer
```
PS XYZ:\> Get-CMOperatingSystemInstaller -Name "OSInstPkg01"-SecuredScopeNames "SecScope02"
```

This command gets the operating system installer named OSInstPkg01 for the security scope named SecScope02.

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

### -Name
Specifies the name of an operating system installer.

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

[New-CMOperatingSystemInstaller](New-CMOperatingSystemInstaller.md)

[Remove-CMOperatingSystemInstaller](Remove-CMOperatingSystemInstaller.md)

[Set-CMOperatingSystemInstaller](Set-CMOperatingSystemInstaller.md)


