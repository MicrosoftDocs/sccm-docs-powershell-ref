---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/20/2020
online version:
schema: 2.0.0
---

# Set-CMWdacSetting

## SYNOPSIS

Modify an existing Microsoft Defender Application Control policy.

## SYNTAX

```
Set-CMWdacSetting [-WdacSettings] <CMWdacSettings> [-EnforcementMode <CMWDACEnforcementMode>]
 [-EnforceRestart <Boolean>] [-EnableIntelligentSecurityGraph <Boolean>] [-TrustedFolders <DirectoryInfo[]>]
 [-TrustedFiles <FileInfo[]>] [-PassThru] [-Name <String>] [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Modify an existing Microsoft Defender Application Control policy. Use [New-CMWdacSetting](New-CMWdacSetting.md) to create a new management policy, and [Get-CMWdacSetting](Get-CMWdacSetting.md) to get an existing management policy.

## EXAMPLES

### Example 1: Add trusted binaries to an existing setting

This example gets an existing Microsoft Defender Application Control policy by name. It then passes that object to the **Set-CMWdacSetting** cmdlet to add two new trusted files.

```powershell
Get-CMWdacSetting -Name "My App Control setting" | Set-CMWdacSetting -TrustedFiles "xyz.exe", "abc.dll"
```

## PARAMETERS

### -Description

Specify a new description for the policy object.

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

Use this parameter to authorize software that the Microsoft Intelligent Security Graph trusts. This service includes Windows Defender SmartScreen and other Microsoft services. For this software to be trusted, the device must be running Windows Defender SmartScreen and Windows 10 version 1709 or later.

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

Use this parameter to change the name of the specified policy object.

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

### -WdacSettings

Specify a policy object to modify. Use the **Get-CMWdacSettings** cmdlet to get this object.

```yaml
Type: CMWdacSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.WDAC.CMWdacSettings
## OUTPUTS

### Microsoft.ConfigurationManagement.PowerShell.Cmdlets.EP.WDAC.CMWdacSettings
## NOTES

## RELATED LINKS

[Copy-CMWdacSetting](Copy-CMWdacSetting.md)

[Get-CMWdacSetting](Get-CMWdacSetting.md)

[New-CMWdacSetting](New-CMWdacSetting.md)

[Remove-CMWdacSetting](Remove-CMWdacSetting.md)

[Windows Defender Application Control management with Configuration Manager](/mem/configmgr/protect/deploy-use/use-device-guard-with-configuration-manager)
