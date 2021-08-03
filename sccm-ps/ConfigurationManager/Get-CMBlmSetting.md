---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Get-CMBlmSetting

## SYNOPSIS

Get one or all the BitLocker management policies from the site.

## SYNTAX

```
Get-CMBlmSetting [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Get one or all the BitLocker management policies from the site. Use [New-CMBlmSetting](New-CMBlmSetting.md) to create a new management policy.

## EXAMPLES

### Example 1: Get all the BitLocker management policies and filter by description

This example gets all policies and then uses the pipe operator to filter the results for the object with the matching description.

```powershell
Get-CMBlmSetting | Where-Object { $_.Description -eq "Unique Description" }
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

### -Name

Specify the name of the policy to get.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.BitLockerManagement.BlmSettings
## NOTES

## RELATED LINKS

[Copy-CMBlmSetting](Copy-CMBlmSetting.md)

[New-CMBlmSetting](New-CMBlmSetting.md)

[Remove-CMBlmSetting](Remove-CMBlmSetting.md)

[Set-CMBlmSetting](Set-CMBlmSetting.md)

[New-CMSettingDeployment](New-CMSettingDeployment.md)

[Deploy BitLocker management](/mem/configmgr/protect/deploy-use/bitlocker/deploy-management-agent)
