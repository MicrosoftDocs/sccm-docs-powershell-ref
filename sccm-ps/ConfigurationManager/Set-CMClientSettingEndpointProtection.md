---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMClientSettingEndpointProtection

## SYNOPSIS
Sets a client setting endpoint protection

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingEndpointProtection [-Enable <Boolean>] [-InstallEndpointProtectionClient <Boolean>]
 [-RemoveThirdParty <Boolean>] [-SuppressReboot <Boolean>] [-ForceRebootHr <Int32>]
 [-DisableFirstSignatureUpdate <Boolean>] [-PersistInstallation <Boolean>]
 [-OverrideMaintenanceWindow <Boolean>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingEndpointProtection [-Enable <Boolean>] [-InstallEndpointProtectionClient <Boolean>]
 [-RemoveThirdParty <Boolean>] [-SuppressReboot <Boolean>] [-ForceRebootHr <Int32>]
 [-DisableFirstSignatureUpdate <Boolean>] [-PersistInstallation <Boolean>]
 [-OverrideMaintenanceWindow <Boolean>] [-DefaultSetting] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingEndpointProtection [-Enable <Boolean>] [-InstallEndpointProtectionClient <Boolean>]
 [-RemoveThirdParty <Boolean>] [-SuppressReboot <Boolean>] [-ForceRebootHr <Int32>]
 [-DisableFirstSignatureUpdate <Boolean>] [-PersistInstallation <Boolean>]
 [-OverrideMaintenanceWindow <Boolean>] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

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

### -DefaultSetting
{{Fill DefaultSetting Description}}

```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableFirstSignatureUpdate
{{Fill DisableFirstSignatureUpdate Description}}

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

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -Enable
{{Fill Enable Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableEndpointProtection

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceRebootHr
{{Fill ForceRebootHr Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ForceRebootPeriod, ForceRebootHours

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -InputObject
{{Fill InputObject Description}}

```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InstallEndpointProtectionClient
{{Fill InstallEndpointProtectionClient Description}}

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

### -Name
{{Fill Name Description}}

```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideMaintenanceWindow
{{Fill OverrideMaintenanceWindow Description}}

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

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -PersistInstallation
{{Fill PersistInstallation Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: CommitEndpointProtectionClientInstallation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveThirdParty
{{Fill RemoveThirdParty Description}}

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

### -SuppressReboot
{{Fill SuppressReboot Description}}

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

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

