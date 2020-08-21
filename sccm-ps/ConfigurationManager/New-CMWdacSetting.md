---
external help file: AdminUI.PS.EP.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
ms.date: 08/20/2020
---

# New-CMWdacSetting

## SYNOPSIS

Create a Microsoft Defender Application Control settings policy object.

## SYNTAX

```
New-CMWdacSetting [-EnforcementMode <CMWDACEnforcementMode>] [-EnforceRestart <Boolean>]
 [-EnableIntelligentSecurityGraph] [-TrustedFolders <DirectoryInfo[]>] [-TrustedFiles <FileInfo[]>]
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Create a Microsoft Defender Application Control settings policy object.

Use the [New-CMSettingDeployment](New-CMSettingDeployment.md) cmdlet to deploy this setting to a collection.

## EXAMPLES

### Example 1: New audit mode Application Control policy

This example creates a new policy object to put Application Control in audit mode.

```powershell
New-CMWdacSetting -Name "NewAudit" -EnforcementMode AuditMode
```

### Example 2: New policy that doesn't reboot the client

This example creates a new policy that doesn't force the client to restart when it applies the policy.

```powershell
New-CMWdacSetting -Name "NewNoReboot" -EnforceRestart $false
```

### Example 3: New policy custom trusted binaries

This example creates a new policy that adds specific files to the list of trusted files.

```powershell
New-CMWdacSetting -Name "NewTrustedFiles" -TrustedFiles "abc.exe", "xyz.dll"
```

## PARAMETERS

### -Description

Specify an optional description to better identify this policy.

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

### -EnableIntelligentSecurityGraph

Add this parameter to authorize software that the Microsoft Intelligent Security Graph trusts. This service includes Windows Defender SmartScreen and other Microsoft services. For this software to be trusted, the device must be running Windows Defender SmartScreen and Windows 10 version 1709 or later.

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

### -EnforceRestart

After the client processes the policy, a restart is scheduled on the client. It follows the client settings for **Computer Restart**. Applications currently running on the device won't have the new Application Control policy applied to them until after the device restarts.

Set this parameter to `$true` to force the device to restart after the client applies the policy.

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

### -EnforcementMode

Choose one of the following enforcement methods for Microsoft Defender Application Control:

- `EnforceMode`: Only trusted executables can run.
- `AuditMode`: Allow all executables to run. Add an entry to the Windows event log when untrusted executables run.

```yaml
Type: CMWDACEnforcementMode
Parameter Sets: (All)
Aliases:
Accepted values: AuditMode, EnforceMode

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

Specify a name for this policy to identify it.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustedFiles

Add trust for specific files.

```yaml
Type: FileInfo[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrustedFolders

Add trust for specific folders.

```yaml
Type: DirectoryInfo[]
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

### None

## OUTPUTS

### Microsoft.ConfigurationManagement.Cmdlets.BitLockerManagement.Commands.CMWdacSettings

## NOTES

## RELATED LINKS

[Copy-CMWdacSetting](Copy-CMWdacSetting.md)

[Get-CMWdacSetting​](Get-CMWdacSetting​.md)

[Remove-CMWdacSetting](Remove-CMWdacSetting.md)

[Set-CMWdacSetting](Set-CMWdacSetting.md)

[New-CMSettingDeployment](New-CMSettingDeployment.md)

[Windows Defender Application Control management with Configuration Manager](/mem/configmgr/protect/deploy-use/use-device-guard-with-configuration-manager)
