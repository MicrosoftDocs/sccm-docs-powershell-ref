---
description: Get a Windows 10 edition upgrade policy.
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2020
schema: 2.0.0
title: Get-CMWindowsEditionUpgradeConfigurationItem
---

# Get-CMWindowsEditionUpgradeConfigurationItem

## SYNOPSIS

Get a Windows 10 edition upgrade policy.

## SYNTAX

### ByValue (Default)
```
Get-CMWindowsEditionUpgradeConfigurationItem [-Fast] [<CommonParameters>]
```

### ById
```
Get-CMWindowsEditionUpgradeConfigurationItem [-Id] <Int32> [-Fast] [<CommonParameters>]
```

### ByName
```
Get-CMWindowsEditionUpgradeConfigurationItem [-Name] <String> [-Fast] [<CommonParameters>]
```

## DESCRIPTION

Get a Windows 10 edition upgrade policy.

## EXAMPLES

### Example 1

```powershell
Get-CMWindowsEditionUpgradeConfigurationItem -Name "Enterprise"
```

## PARAMETERS

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

Specify the ID of the Windows 10 edition upgrade policy. This ID is the **CI ID** of the policy, for example: `552481`.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the Windows 10 edition upgrade policy.

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMWindows10EditionUpgrade](New-CMWindows10EditionUpgrade.md)

[Remove-CMWindows10EditionUpgrade](Remove-CMWindows10EditionUpgrade.md)

[Set-CMWindows10EditionUpgrade](Set-CMWindows10EditionUpgrade.md)

[Upgrade Windows devices to a new edition with Configuration Manager](/mem/configmgr/compliance/deploy-use/upgrade-windows-version)
