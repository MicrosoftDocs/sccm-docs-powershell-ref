---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMBLEncryptionMethodWithXts

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-CMBLEncryptionMethodWithXts [-PolicyState <State>] [-OSDriveEncryptionMethod <WindowsTenEncryptionMethod>]
 [-FixedDriveEncryptionMethod <WindowsTenEncryptionMethod>]
 [-RemovableDriveEncryptionMethod <WindowsTenEncryptionMethod>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

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

### -FixedDriveEncryptionMethod
{{ Fill FixedDriveEncryptionMethod Description }}

```yaml
Type: WindowsTenEncryptionMethod
Parameter Sets: (All)
Aliases:
Accepted values: AesXts128, AesXts256, AesCbc128, AesCbc256

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

### -OSDriveEncryptionMethod
{{ Fill OSDriveEncryptionMethod Description }}

```yaml
Type: WindowsTenEncryptionMethod
Parameter Sets: (All)
Aliases:
Accepted values: AesXts128, AesXts256, AesCbc128, AesCbc256

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicyState
{{ Fill PolicyState Description }}

```yaml
Type: State
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, NotConfigured

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemovableDriveEncryptionMethod
{{ Fill RemovableDriveEncryptionMethod Description }}

```yaml
Type: WindowsTenEncryptionMethod
Parameter Sets: (All)
Aliases:
Accepted values: AesXts128, AesXts256, AesCbc128, AesCbc256

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

### Microsoft.ConfigurationManagement.AdminConsole.BitlockerManagement.PolicyObject

## NOTES

## RELATED LINKS
