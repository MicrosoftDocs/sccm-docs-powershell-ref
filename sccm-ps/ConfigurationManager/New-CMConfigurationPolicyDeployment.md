---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMConfigurationPolicyDeployment

## SYNOPSIS
Creates a configuration policy deployment

## SYNTAX

### DeployFWPolicyByValueMandatory (Default)
```
New-CMConfigurationPolicyDeployment -FirewallPolicy <IResultObject> [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment -UserDataAndProfileName <String> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment -UserDataAndProfileId <String> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByValueMandatory
```
New-CMConfigurationPolicyDeployment -UserDataAndProfile <IResultObject> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployFWPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment -FirewallPolicyName <String> [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployFWPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment -FirewallPolicyId <String> [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment -RemoteConnectionProfileName <String> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment -RemoteConnectionProfileId <String> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByValueMandatory
```
New-CMConfigurationPolicyDeployment -RemoteConnectionProfile <IResultObject> [-EnableEnforcement <Boolean>]
 [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-MonitoredByScom <Boolean>] [-Schedule <IResultObject>]
 [-CollectionName <String>] [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling]
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

### -Collection
{{Fill Collection Description}}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
{{Fill CollectionId Description}}

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

### -CollectionName
{{Fill CollectionName Description}}

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

### -EnableEnforcement
{{Fill EnableEnforcement Description}}

```yaml
Type: Boolean
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
{{Fill FirewallPolicy Description}}

```yaml
Type: IResultObject
Parameter Sets: DeployFWPolicyByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -FirewallPolicyId
{{Fill FirewallPolicyId Description}}

```yaml
Type: String
Parameter Sets: DeployFWPolicyByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyName
{{Fill FirewallPolicyName Description}}

```yaml
Type: String
Parameter Sets: DeployFWPolicyByNameMandatory
Aliases: 

Required: True
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

### -GenerateAlert
{{Fill GenerateAlert Description}}

```yaml
Type: Boolean
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitoredByScom
{{Fill MonitoredByScom Description}}

```yaml
Type: Boolean
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
{{Fill OverrideServiceWindow Description}}

```yaml
Type: Boolean
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParameterValue
{{Fill ParameterValue Description}}

```yaml
Type: Int32
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PostponeDateTime
{{Fill PostponeDateTime Description}}

```yaml
Type: DateTime
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteConnectionProfile
{{Fill RemoteConnectionProfile Description}}

```yaml
Type: IResultObject
Parameter Sets: DeployRCPolicyByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoteConnectionProfileId
{{Fill RemoteConnectionProfileId Description}}

```yaml
Type: String
Parameter Sets: DeployRCPolicyByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteConnectionProfileName
{{Fill RemoteConnectionProfileName Description}}

```yaml
Type: String
Parameter Sets: DeployRCPolicyByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
{{Fill Schedule Description}}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDataAndProfile
{{Fill UserDataAndProfile Description}}

```yaml
Type: IResultObject
Parameter Sets: DeployUSMPolicyByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UserDataAndProfileId
{{Fill UserDataAndProfileId Description}}

```yaml
Type: String
Parameter Sets: DeployUSMPolicyByIdMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDataAndProfileName
{{Fill UserDataAndProfileName Description}}

```yaml
Type: String
Parameter Sets: DeployUSMPolicyByNameMandatory
Aliases: 

Required: True
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

