---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Get-CMDuplicateHardwareIdMacAddress

## SYNOPSIS

View duplicate hardware identifiers by MAC address.

## SYNTAX

### SearchByName (Default)
```
Get-CMDuplicateHardwareIdMacAddress [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDuplicateHardwareIdMacAddress -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to view duplicate hardware identifiers by network MAC address. Configuration Manager ignores these MAC addresses for PXE boot and client registration. For more information, see [Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers).

>[!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: View all MAC addresses

This example displays all duplicate addresses from the site.

```powershell
Get-CMDuplicateHardwareIdMacAddress | Select-Object MACAddress
```

### Example 2: Test for a specific MAC address

The following example script checks if a specific address is found, and then writes a message based on the result.

```powershell
$mac = "01:23:45:67:89:AB"

if ( Get-CMDuplicateHardwareIdMacAddress -Id $mac ) {
  Write-Host $mac "exists in the site"
} else {
  Write-Host $mac "doesn't exist!"
}
```

## PARAMETERS

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

Specify a duplicate hardware MAC address. The format of this value uses colon (`:`) delimiters, for example, `"01:23:45:67:89:AB"`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: DuplicateId, DuplicateHardwareId

Required: True
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

### IResultObject[]#SMS_CommonMacAddresses
### IResultObject#SMS_CommonMacAddresses
## NOTES

This cmdlet returns the **SMS_CommonMacAddresses** WMI class object.

## RELATED LINKS

[New-CMDuplicateHardwareIdMacAddress](New-CMDuplicateHardwareIdMacAddress.md)
[Remove-CMDuplicateHardwareIdMacAddress](Remove-CMDuplicateHardwareIdMacAddress.md)

[Get-CMDuplicateHardwareIdGuid](Get-CMDuplicateHardwareIdGuid.md)

[Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers)
