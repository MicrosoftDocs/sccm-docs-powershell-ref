---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMClientSettingWindowsAnalytics

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingWindowsAnalytics [-CommercialIdKey <String>] [-Enable <Boolean>]
 [-EnableEarlierTelemetry <Boolean>] [-IEDataCollectionOption <InternetExplorerTelemetryLevelType>]
 [-Win10Telemetry <Win10TelemetryLevelType>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingWindowsAnalytics [-CommercialIdKey <String>] [-Enable <Boolean>]
 [-EnableEarlierTelemetry <Boolean>] [-IEDataCollectionOption <InternetExplorerTelemetryLevelType>]
 [-Win10Telemetry <Win10TelemetryLevelType>] [-DefaultSetting] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingWindowsAnalytics [-CommercialIdKey <String>] [-Enable <Boolean>]
 [-EnableEarlierTelemetry <Boolean>] [-IEDataCollectionOption <InternetExplorerTelemetryLevelType>]
 [-Win10Telemetry <Win10TelemetryLevelType>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -CommercialIdKey
{{ Fill CommercialIdKey Description }}

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

### -DefaultSetting
{{ Fill DefaultSetting Description }}

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

### -Enable
{{ Fill Enable Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableWindowsAnalyticsManagement

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableEarlierTelemetry
{{ Fill EnableEarlierTelemetry Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableWindows81AndEarlierTelemetry

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

### -IEDataCollectionOption
{{ Fill IEDataCollectionOption Description }}

```yaml
Type: InternetExplorerTelemetryLevelType
Parameter Sets: (All)
Aliases: EnableWindows81AndEarlierInternetExplorerDataCollectionFor
Accepted values: Disable, LocalIntranetAndTrustedSitesAndMachineLocal, InternetAndRestrictedSites, AllZones

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

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

### -Name
{{ Fill Name Description }}

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

### -Win10Telemetry
{{ Fill Win10Telemetry Description }}

```yaml
Type: Win10TelemetryLevelType
Parameter Sets: (All)
Aliases: Windows10Telemetry
Accepted values: Basic, EnhancedLimited, Enhanced, Full

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

### System.Object
## NOTES

## RELATED LINKS
