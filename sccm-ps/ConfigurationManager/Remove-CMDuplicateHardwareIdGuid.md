---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Remove-CMDuplicateHardwareIdGuid

## SYNOPSIS

Use this cmdlet to remove duplicate hardware identifiers by GUID.

## SYNTAX

### ByValue (Default)
```
Remove-CMDuplicateHardwareIdGuid -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Remove-CMDuplicateHardwareIdGuid -Id <Guid> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1910, use this cmdlet to remove duplicate hardware identifiers by GUID.

## EXAMPLES

### Example 1: Specify an explicit ID to remove

This example removes a hardware identifier for the specified GUID.

```powershell
Remove-CMDuplicateHardwareIdGuid -Id 24D0F753-B2E2-4D9C-B07C-099C4FC1EF3C
```

### Example 2: Remove an ID for an input object

This example removes a hardware identifier for an input object `$myGuid`. This variable stores the identifier as `IResultObject#SMS_CommonSmbiosGuids`.

```powershell
Remove-CMDuplicateHardwareIdGuid -InputObject $myGuid
```

## PARAMETERS

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify the GUID of the hardware identifier to remove from the site.

```yaml
Type: Guid
Parameter Sets: ByName
Aliases: DuplicateId, DuplicateHardwareId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a GUID object for the hardware identifier to remove from the site. This object is of type `IResultObject#SMS_CommonSmbiosGuids`.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
