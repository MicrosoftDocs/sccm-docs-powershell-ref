---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
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
Set-CMClientSettingWindowsAnalytics [-Enable <Boolean>] [-CommercialIdKey <String>]
 [-Win10Telemetry <Win10TelemetryLevelType>] [-EnableEarlierTelemetry <Boolean>]
 [-IEDataCollectionOption <InternetExplorerTelemetryLevelType>] -Name <String> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingWindowsAnalytics [-Enable <Boolean>] [-CommercialIdKey <String>]
 [-Win10Telemetry <Win10TelemetryLevelType>] [-EnableEarlierTelemetry <Boolean>]
 [-IEDataCollectionOption <InternetExplorerTelemetryLevelType>] [-DefaultSetting] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingWindowsAnalytics [-Enable <Boolean>] [-CommercialIdKey <String>]
 [-Win10Telemetry <Win10TelemetryLevelType>] [-EnableEarlierTelemetry <Boolean>]
 [-IEDataCollectionOption <InternetExplorerTelemetryLevelType>] -InputObject <IResultObject> [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

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
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill PassThru Description }}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
