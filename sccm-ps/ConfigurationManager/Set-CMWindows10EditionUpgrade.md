---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2020
online version:
schema: 2.0.0
---

# Set-CMWindows10EditionUpgrade

## SYNOPSIS

Configure a Windows 10 edition upgrade policy.

## SYNTAX

### SetByIdMandatory (Default)
```
Set-CMWindows10EditionUpgrade [-Description <String>] -Id <Int32> [-NewName <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMWindows10EditionUpgrade [-Description <String>] -InputObject <IResultObject> [-NewName <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMWindows10EditionUpgrade [-Description <String>] -Name <String> [-NewName <String>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Configure a Windows 10 edition upgrade policy.

## EXAMPLES

### Example 1

```powershell
$win10UpgradePolicyId = 16777523

$newDescription = "update description for the edition upgrade policy"

Set-CMWindows10EditionUpgrade -Id $win10UpgradePolicyId -Description $newDescription
```

## PARAMETERS

### -Description

Specify a new description for the edition upgrade policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

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

Specify the ID of the Windows 10 edition upgrade policy to configure. This ID is the **CI ID** of the policy, for example: `552481`.

```yaml
Type: Int32
Parameter Sets: SetByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for the Windows 10 edition upgrade policy to configure. To get this object, use the [Get-CMWindowsEditionUpgradeConfigurationItem](Get-CMWindowsEditionUpgradeConfigurationItem.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: Windows10EditionUpgradePolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the Windows 10 edition upgrade policy to configure.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename the edition upgrade policy.

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

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### IResultObject#SMS_ConfigurationPolicy
## NOTES

## RELATED LINKS

[Get-CMWindowsEditionUpgradeConfigurationItem](Get-CMWindowsEditionUpgradeConfigurationItem.md)

[New-CMWindows10EditionUpgrade](New-CMWindows10EditionUpgrade.md)

[Remove-CMWindows10EditionUpgrade](Remove-CMWindows10EditionUpgrade.md)

[Upgrade Windows devices to a new edition with Configuration Manager](/mem/configmgr/compliance/deploy-use/upgrade-windows-version)
