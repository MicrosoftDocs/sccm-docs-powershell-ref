---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# New-CMDuplicateHardwareIdMacAddress

## SYNOPSIS

Add duplicate hardware identifiers by MAC address.

## SYNTAX

```
New-CMDuplicateHardwareIdMacAddress -MacAddress <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to add duplicate hardware identifiers by MAC address. Configuration Manager ignores these MAC addresses for PXE boot and client registration. For more information, see [Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers).

>[!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a duplicate hardware entry for a MAC address

This example adds a duplicate hardware entry to the site by the device's network MAC address.

```powershell
New-CMDuplicateHardwareIdMacAddress -MacAddress '01:02:03:04:05:E0'
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

### -MacAddress

Specify the MAC address of the machine as a string with colon (`:`) delimiters. For example, `'01:02:03:04:05:E0'`

```yaml
Type: String
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

### IResultObject#SMS_CommonMacAddresses
## NOTES

This cmdlet returns the **SMS_CommonMacAddresses** WMI class object.

## RELATED LINKS

[Get-CMDuplicateHardwareIdMacAddress](Get-CMDuplicateHardwareIdMacAddress.md)
[Remove-CMDuplicateHardwareIdMacAddress](Remove-CMDuplicateHardwareIdMacAddress.md)

[New-CMDuplicateHardwareIdGuid](New-CMDuplicateHardwareIdGuid.md)

[Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers)
