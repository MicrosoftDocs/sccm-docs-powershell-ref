---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 009BA9A5-AB9A-4512-99D9-D2788C7FE02A
online version: https://go.microsoft.com/fwlink/?linkid=834257
schema: 2.0.0
---

# Sync-CMSoftwareUpdate

## SYNOPSIS
Synchronizes software updates.

## SYNTAX

```
Sync-CMSoftwareUpdate -FullSync <Boolean> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Sync-CMSoftwareUpdate** cmdlet retrieves metadata for software updates.
Software updates synchronization in Configuration Manager uses Microsoft Update to retrieve software updates metadata.
You can use this cmdlet to retrieve metadata for all software updates or only recent changes to software updates.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Perform a full synchronization for all software updates
```
PS XYZ:\> Sync-CMSoftwareUpdate -FullSync $True
```

This command performs a complete metadata synchronization for all software updates.

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

### -FullSync
Indicates whether to perform a complete synchronization of all updates or a delta synchronization.

```yaml
Type: Boolean
Parameter Sets: (All)
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

[Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md)

[Save-CMSoftwareUpdate](Save-CMSoftwareUpdate.md)

[Set-CMSoftwareUpdate](Set-CMSoftwareUpdate.md)


