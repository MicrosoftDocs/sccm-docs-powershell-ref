---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Get-CMDuplicateHardwareIdGuid

## SYNOPSIS

View duplicate hardware identifiers by GUID.

## SYNTAX

### SearchByName (Default)
```
Get-CMDuplicateHardwareIdGuid [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDuplicateHardwareIdGuid -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to view duplicate hardware identifiers by GUID. Configuration Manager ignores these GUIDs for PXE boot and client registration. For more information, see [Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers).

>[!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: View all GUIDs

This example displays all duplicate hardware GUIDs from the site.

```powershell
Get-CMDuplicateHardwareIdGuid | Select-Object SMBIOS_GUID
```

### Example 2: Test for a specific GUID

The following example script checks if a specific GUID is found, and then writes a message based on the result.

```powershell
$guid = "AB83D231-8C12-9413-FEBA-C0F9888B9290"

if ( Get-CMDuplicateHardwareIdGuid -Id $guid ) {
  Write-Host $guid "exists in the site"
} else {
  Write-Host $guid "doesn't exist!"
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

Specify a duplicate hardware ID. The format of this value is a standard GUID, for example, `"feff51c2-9266-4da7-adec-4252c56a1713"`.

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

### IResultObject[]#SMS_CommonSmbiosGuids
### IResultObject#SMS_CommonSmbiosGuids
## NOTES

This cmdlet returns the **SMS_CommonSmbiosGuids** WMI class object.

## RELATED LINKS

[New-CMDuplicateHardwareIdGuid](New-CMDuplicateHardwareIdGuid.md)
[Remove-CMDuplicateHardwareIdGuid](Remove-CMDuplicateHardwareIdGuid.md)

[Get-CMDuplicateHardwareIdMacAddress](Get-CMDuplicateHardwareIdMacAddress.md)

[Manage duplicate hardware identifiers](/mem/configmgr/core/clients/manage/manage-clients#manage-duplicate-hardware-identifiers)
