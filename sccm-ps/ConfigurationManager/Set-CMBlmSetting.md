---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Set-CMBlmSetting

## SYNOPSIS

Modify an existing BitLocker management policy setting.

## SYNTAX

```
Set-CMBlmSetting [-BlmSettings] <BlmSettings> [-Policies <PolicyObject[]>] [-PassThru] [-Name <String>]
 [-Description <String>] [-Precedence <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Modify an existing BitLocker management policy setting. Use [New-CMBlmSetting](New-CMBlmSetting.md) to create a new management policy, and [Get-CMBlmSetting](Get-CMBlmSetting.md) to get an existing management policy.

## EXAMPLES

### Example 1: Add a new policy to an existing setting

This example gets the existing BitLocker management policy by name. It then passes that object to the **Set-CMBlmSetting** cmdlet to add a new policy. The new policy is created by the **New-CMBMSOSDEncryptionPolicy** cmdlet.

```powershell
Get-CMBlmSetting -Name "My BitLocker settings" | Set-CMBlmSetting -Policies (New-CMBMSOSDEncryptionPolicy -PolicyState Enabled -Protector TpmOnly)
```

## PARAMETERS

### -BlmSettings

Specify a BitLocker management policy settings object to configure. Use the [Get-CMBlmSetting](Get-CMBlmSetting.md) to get this object.

```yaml
Type: BlmSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Description

Specify a new description for the BitLocker management policy object.

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

### -Name

Use this parameter to change the name of the specified BitLocker management policy object.

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

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### -Policies

Specify an array of BitLocker policies to include. For more information on the specific policy cmdlets, see the **Related links** in the [New-CMBlmSetting](New-CMBlmSetting.md) cmdlet.

If you don't specify any policies with the **-Policies** parameter, the default policy is a single, not configured, OS drive encryption policy. For more information on this default policy type, see [New-CMBMSOSDEncryptionPolicy](New-CMBMSOSDEncryptionPolicy.md).

```yaml
Type: PolicyObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Precedence

Change the priority order of this policy. If you deploy multiple policies to the same client, the lowest number takes precedence.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.BitLockerManagement.BlmSettings
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.BitLockerManagement.BlmSettings
## NOTES

## RELATED LINKS

[Copy-CMBlmSetting](Copy-CMBlmSetting.md)

[Get-CMBlmSetting](Get-CMBlmSetting.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[Remove-CMBlmSetting](Remove-CMBlmSetting.md)

[Deploy BitLocker management](/mem/configmgr/protect/deploy-use/bitlocker/deploy-management-agent)
