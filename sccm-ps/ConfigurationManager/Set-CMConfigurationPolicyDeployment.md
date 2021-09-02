---
description: Creates a configuration policy deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMConfigurationPolicyDeployment
---

# Set-CMConfigurationPolicyDeployment

## SYNOPSIS
Creates a configuration policy deployment.

## SYNTAX

### SetPoicyByValueMandatory (Default)
```
Set-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 -InputObject <IResultObject> [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetFWPolicyDeploymentByIdMandatory
```
Set-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] -FirewallPolicyId <String>
 [-GenerateAlert <Boolean>] [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetFWPolicyDeploymentByNameMandatory
```
Set-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] -FirewallPolicyName <String>
 [-GenerateAlert <Boolean>] [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>]
 [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetRemoteConnectionDeploymentByIdMandatory
```
Set-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] -RemoteConnectionProfileId <String> [-Schedule <IResultObject>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetRemoteConnectionDeploymentByNameMandatory
```
Set-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] -RemoteConnectionProfileName <String> [-Schedule <IResultObject>] [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetUSMPolicyDeploymentByIdMandatory
```
Set-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] -UserDataAndProfileId <String> [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetUSMPolicyDeploymentByNameMandatory
```
Set-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] -UserDataAndProfileName <String> [-PassThru]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMConfigurationPolicyDeployment** cmdlet creates a configuration policy deployment in Configuration Manager.
You can deploy firewall policies or user session management policies.
Use the [New-CMConfigurationPolicyDeployment](New-CMConfigurationPolicyDeployment.md) cmdlet to deploy specified policies for a Configuration Manager collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a configuration policy deployment
```
PS XYZ:\> Set-CMConfigurationPolicyDeployment -CollectionName "Regional Remote Users" -FirewallPolicyName "Remote Firewall Policy"
```

This command creates a configuration policy deployment named Remote Firewall Policy and deploys it to the collection named Regional Remote Users.

## PARAMETERS

### -Collection
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
Specifies the name of a collection.
The deployment applies to this collection.

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

### -EnableEnforcement
Indicates whether to enable enforcement for the deployment.
During enforcement, a client reports compliance information about a deployment.

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

### -FirewallPolicyId
Specifies the ID of a Windows Firewall policy.

```yaml
Type: String
Parameter Sets: SetFWPolicyDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicyName
Specifies the name of a Windows Firewall policy.

```yaml
Type: String
Parameter Sets: SetFWPolicyDeploymentByNameMandatory
Aliases:

Required: True
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

### -GenerateAlert
Indicates whether Configuration Manager generates alerts during the deployment.

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

### -InputObject
```yaml
Type: IResultObject
Parameter Sets: SetPoicyByValueMandatory
Aliases: UserDataAndProfile, FirewallPolicy, RemoteConnectionProfile, DeploymentSummary, Assignment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MonitoredByScom
Indicates whether System Center 2016 - Operations Manager monitoring criteria applies during the deployment.

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

### -OverrideServiceWindow
Indicates whether to override the service window while deploying policies.
Service windows are periods of time allocated for maintenance.

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

### -ParameterValue
Specifies the values of administrator-defined parameters, such as thresholds.
Configuration Manager stores the values in XML format.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
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

### -PostponeDateTime
```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteConnectionProfileId
```yaml
Type: String
Parameter Sets: SetRemoteConnectionDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteConnectionProfileName
```yaml
Type: String
Parameter Sets: SetRemoteConnectionDeploymentByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
Specifies a schedule object.
This is the schedule for deploying the configuration policy.
You can use the [New-CMSchedule](New-CMSchedule.md) cmdlet to create a schedule token.

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

### -UserDataAndProfileId
Specifies an ID of a user data and profile configuration item.

```yaml
Type: String
Parameter Sets: SetUSMPolicyDeploymentByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDataAndProfileName
Specifies a name of a user data and profile configuration item.

```yaml
Type: String
Parameter Sets: SetUSMPolicyDeploymentByNameMandatory
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

### -WhatIf

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMUserDataAndProfileConfigurationItem](Get-CMUserDataAndProfileConfigurationItem.md)

[Get-CMWindowsFirewallPolicy](Get-CMWindowsFirewallPolicy.md)

[New-CMSchedule](New-CMSchedule.md)

[New-CMConfigurationPolicyDeployment](New-CMConfigurationPolicyDeployment.md)
