---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/03/2020
online version:
schema: 2.0.0
---

# New-CMWindows10EditionUpgrade

## SYNOPSIS

Create a Windows 10 edition upgrade policy.

## SYNTAX

```
New-CMWindows10EditionUpgrade [-Description <String>] [-EditionUpgradeWithClient <Boolean>]
 [-LicenseFile <String>] -Name <String> [-ProductKey <String>] [-WindowsEdition <WindowsEditionType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Create a Windows 10 edition upgrade policy. Specify a product key or license information to upgrade Windows 10 to a different edition. For more information, see [Upgrade Windows devices to a new edition with Configuration Manager](/mem/configmgr/compliance/deploy-use/upgrade-windows-version).

## EXAMPLES

### Example 1

```powershell
New-CMWindows10EditionUpgrade -Name "NewEditionPolicyByKey" -WindowsEdition Windows10Enterprise -ProductKey "123ab-cd456-789ef-2j3k4-0ghi1"
```

## PARAMETERS

### -Description

Specify an optional description for the policy.

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

### -EditionUpgradeWithClient

Use this parameter to specify the type of edition upgrade to create:

- `$true`: The policy is for devices managed with the Configuration Manager client. Use the **ProductKey** parameter to specify the license key.
- `$false`: This policy is for devices running Windows 10 Mobile that you manage with on-premises MDM. Use the **LicenseFile** parameter to provide the XML license file.

```yaml
Type: Boolean
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

### -LicenseFile

When you set the **EditionUpgradeWithClient** parameter to `$false`, use this parameter to specify the path to the XML license file. Get the license file from the Microsoft Volume Licensing Service Center (VLSC). This file contains the licensing information for the new version of Windows on all devices you target with the policy. Download the ISO file for **Windows 10 Mobile Enterprise**, which includes the licensing XML.

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

### -Name

Specify a name for this Windows 10 edition upgrade policy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProductKey

When you set the **EditionUpgradeWithClient** parameter to `$true`, use this parameter to specify a valid product key for the new version of Windows. This product key can be a multiple activation key (MAK), or a generic volume licensing key (GVLK). A GVLK is also referred to as a key management service (KMS) client setup key. For more information, see [Plan for volume activation](/windows/deployment/volume-activation/plan-for-volume-activation-client). For a list of KMS client setup keys, see [Appendix A](/windows-server/get-started/kmsclientkeys) of the Windows Server activation guide.

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

### -WindowsEdition

Specify the target edition of Windows 10 that corresponds with the **LicenseFile** or **ProductKey**.

```yaml
Type: WindowsEditionType
Parameter Sets: (All)
Aliases:
Accepted values: Windows10Enterprise, Windows10Education, Windows10EnterpriseN, Windows10EducationN, WindowsPhone10, HolographicEnterprise

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

### None
## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy
## NOTES

## RELATED LINKS

[Get-CMWindowsEditionUpgradeConfigurationItem](Get-CMWindowsEditionUpgradeConfigurationItem.md)

[Remove-CMWindows10EditionUpgrade](Remove-CMWindows10EditionUpgrade.md)

[Set-CMWindows10EditionUpgrade](Set-CMWindows10EditionUpgrade.md)

[Upgrade Windows devices to a new edition with Configuration Manager](/mem/configmgr/compliance/deploy-use/upgrade-windows-version)
