---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833632
schema: 2.0.0
ms.assetid: 02B40786-6500-4F35-B8DC-531AAF099381
---

# New-CMDriverPackage

## SYNOPSIS
Creates a driver package.

## SYNTAX

```
New-CMDriverPackage -Name <String> -Path <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMDriverPackage** cmdlet creates a driver package.

## EXAMPLES

### Example 1: Create a new driver package
```
PS C:\> New-CMDriverPackage -Name "Pckg01" -Path "\\Contoso01\Users\pattifuller\Desktop\pckg"
```

This command creates a new driver package named Pckg01.

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
Specifies a description of a driver package.

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

### -Name
Specifies a name for a driver package.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
Specifies a file path to the location where Configuration Manager stores the compressed version of the source files on the site server.

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

[Export-CMDriverPackage](./Export-CMDriverPackage.md)

[Get-CMDriverPackage](./Get-CMDriverPackage.md)

[Import-CMDriverPackage](./Import-CMDriverPackage.md)

[Remove-CMDriverPackage](./Remove-CMDriverPackage.md)

[Set-CMDriverPackage](./Set-CMDriverPackage.md)
