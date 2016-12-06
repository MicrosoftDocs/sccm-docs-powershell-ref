---
external help file: AdminUI.PS.Dcm.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834210
schema: 2.0.0
ms.assetid: 9F810236-8954-43EB-BE04-B119088905B9
---

# Start-CMConfigurationPolicyDeployment

## SYNOPSIS
Deploys policies for a Configuration Manager collection.

## SYNTAX

### DeployFWPolicyByValueMandatory (Default)
```
Start-CMConfigurationPolicyDeployment -FirewallPolicy <IResultObject> -CollectionName <String>
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByNameMandatory
```
Start-CMConfigurationPolicyDeployment -UserDataAndProfileName <String> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByIdMandatory
```
Start-CMConfigurationPolicyDeployment -UserDataAndProfileId <String> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByValueMandatory
```
Start-CMConfigurationPolicyDeployment -UserDataAndProfile <IResultObject> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployFWPolicyByNameMandatory
```
Start-CMConfigurationPolicyDeployment -FirewallPolicyName <String> -CollectionName <String>
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployFWPolicyByIdMandatory
```
Start-CMConfigurationPolicyDeployment -FirewallPolicyId <String> -CollectionName <String>
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByNameMandatory
```
Start-CMConfigurationPolicyDeployment -RemoteConnectionProfileName <String> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByIdMandatory
```
Start-CMConfigurationPolicyDeployment -RemoteConnectionProfileId <String> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByValueMandatory
```
Start-CMConfigurationPolicyDeployment -RemoteConnectionProfile <IResultObject> -CollectionName <String>
 [-EnableEnforcement <Boolean>] [-OverrideServiceWindow <Boolean>] [-GenerateAlert <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDate <DateTime>] [-PostponeTime <DateTime>] [-MonitoredByScom <Boolean>]
 [-Schedule <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMConfigurationPolicyDeployment** cmdlet deploys specified policies for a Microsoft System Center Configuration Manager collection.
You can deploy firewall policies or user session management policies.

You can specify a firewall policy by name or by ID or use another cmdlet to get firewall policy object.

You can specify System Center 2016 - Operations Manager monitoring criteria.

## EXAMPLES

### Example 1: Start deployment of a firewall policy
```
PS C:\>Start-CMConfigurationPolicyDeployment -CollectionName "Desktop systems" -FirewallPolicyName "General firewall policy"
```

This command starts the configuration policy deployment for a collection named Desktop systems.
The command specifies a firewall policy named General firewall policy.

## PARAMETERS

### -CollectionName
Specifies the name of a collection.
The deployment applies to this Configuration Manager collection.

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

### -Confirm
Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf
Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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
Indicates whether to enable enforcement for the deployment.
During enforcement, a client reports compliance information about a deployment.

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
Specifies a firewall policy object.

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
Specifies an ID for a firewall policy.

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
Specifies a name for a firewall policy.

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
Indicates that wildcard handling is enabled.

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
Specifies whether Configuration Manager generates alerts during the deployment.

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
Specifies whether Operations Manager monitoring criteria applies during the deployment.

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
Specifies whether to override the service window while deploying policies.

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
Specifies an integer value.
This is the parameter value.

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

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

### -PostponeDate
Specifies a date, as a **DateTime** object.
To get a **DateTime** object, use the Get-Date cmdlet.
For more information, type `Get-Help Get-Date`.
This is the date for the deployment if postponed.

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

### -PostponeTime
Specifies a time, as a **DateTime** object.
To obtain a **DateTime** object, use the Get-Date cmdlet.
This is the time for the deployment if postponed.

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
Specifies the remote connection profile that this cmdlet deploys configuration policy on.

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
Specifies the remote connection profile ID that this cmdlet deploys configuration policy for.

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
Specifies the remote connection profile name that this cmdlet deploys configuration policy for.

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
Specifies a schedule object.
This is the schedule for evaluating the policy.

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
Specifies a user data and profile object.
To obtain a user data and profile object, use the Get-CMUserDataAndProfileConfigurationItem cmdlet.

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
Specifies an ID for a user data and profile object.

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
Specifies a name for a user data and profile object.

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Set-CMConfigurationPolicyDeployment](./Set-CMConfigurationPolicyDeployment.md)


