---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-CMResultantSettings

## SYNOPSIS
Gets a resultant settings

## SYNTAX

### ByName (Default)
```
Get-CMResultantSettings -Name <String> -SettingsType <ResultantSettingsType> [-Setting <SettingType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMResultantSettings -Id <String> -SettingsType <ResultantSettingsType> [-Setting <SettingType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMResultantSettings -InputObject <IResultObject> -SettingsType <ResultantSettingsType>
 [-Setting <SettingType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1
```
PS XYZ:\>  
```

 

## PARAMETERS

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

### -Id
 

```yaml
Type: String
Parameter Sets: ById
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
 

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Device, User

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
 

```yaml
Type: String
Parameter Sets: ByName
Aliases: DeviceName, UserName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Setting
 

```yaml
Type: SettingType
Parameter Sets: (All)
Aliases: 
Accepted values: BackgroundIntelligentTransfer, Cloud, ClientCache, ClientPolicy, ComplianceSettings, ComputerAgent, ComputerRestart, EndpointProtection, HardwareInventory, MeteredNetwork, MobileDevice, NetworkAccessProtection, PowerManagement, RemoteTools, SoftwareDeployment, SoftwareInventory, SoftwareMetering, SoftwareUpdates, StateMessaging, UserAndDeviceAffinity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingsType
 

```yaml
Type: ResultantSettingsType
Parameter Sets: (All)
Aliases: 
Accepted values: Device, User

Required: True
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

