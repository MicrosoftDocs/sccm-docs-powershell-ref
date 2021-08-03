---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# New-CMDuplicateHardwareIdGuid

## SYNOPSIS

Add duplicate hardware identifiers by GUID.

## SYNTAX

```
New-CMDuplicateHardwareIdGuid -Id <Guid> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add duplicate hardware identifiers by GUID. Configuration Manager ignores these GUIDs for PXE boot and client registration. For more information, see [Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers).

>[!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a duplicate hardware entry for a GUID

This example adds a new duplicate hardware entry to the site by the device's GUID.

```powershell
New-CMDuplicateHardwareIdGuid -Id 24D0F753-B2E2-4D9C-B07C-099C4FC1EF3C
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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

Specify the hardware GUID, for example, `feff51c2-9266-4da7-adec-4252c56a1713`.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: DuplicateId, DuplicateHardwareId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### None
## OUTPUTS

### IResultObject#SMS_CommonSmbiosGuids
## NOTES

This cmdlet returns the **SMS_CommonSmbiosGuids** WMI class object.

## RELATED LINKS

[Get-CMDuplicateHardwareIdGuid](Get-CMDuplicateHardwareIdGuid.md)
[Remove-CMDuplicateHardwareIdGuid](Remove-CMDuplicateHardwareIdGuid.md)

[New-CMDuplicateHardwareIdMacAddress](New-CMDuplicateHardwareIdMacAddress.md)

[Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers)
