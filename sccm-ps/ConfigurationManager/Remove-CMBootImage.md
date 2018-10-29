---
external help file: AdminUI.PS.Osd.dll-Help.xml
ms.assetid: BFB60354-1427-48AB-B27B-86FFABCCA9C5
online version: https://go.microsoft.com/fwlink/?linkid=833924
schema: 2.0.0
---

# Remove-CMBootImage

## SYNOPSIS
Removes an operating system boot image.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMBootImage -InputObject <IResultObject> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMBootImage -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMBootImage -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMBootImage** cmdlet removes a Windows Preinstallation Environment (Windows PE) operating system boot image from Microsoft System Center Configuration Manager.

You must run **Remove-CMBootImage** on the computer that is running the Systems Management Server (SMS) provider.
The computer account of the computer that is running the SMS provider must have Read and Write access to the package source of the boot image.
For more information about the SMS provider, see [Planning for the SMS Provider in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=263566) on TechNet.

## EXAMPLES

### Example 1: Remove a boot image object that is identified by using its ID
```
PS C:\> Remove-CMBootImage -Id "CM100004" -Confirm
```

This command removes a boot image object that is identified by using its ID.
You must confirm the action before the command performs it.

### Example 2: Remove a boot image object that is identified by using its name
```
PS C:\> Remove-CMBootImage -Name "Boot image (86)" -Confirm
```

This command removes a boot image object that is identified by using its name.
You must confirm the action before the command performs it.

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
Specifies an array of boot images identifiers.
You can get a boot image object by using the [Get-CMBootImage](Get-CMBootImage.md) cmdlet.

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
Specifies a boot image object.

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
Specifies a name of a boot image.

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

[Planning for the SMS Provider in Configuration Manager](http://go.microsoft.com/fwlink/?LinkID=263566)

[Get-CMBootImage](Get-CMBootImage.md)

[New-CMBootImage](New-CMBootImage.md)

[Set-CMBootImage](Set-CMBootImage.md)


