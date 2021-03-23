---
description: Creates a configuration policy deployment.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: New-CMConfigurationPolicyDeployment
---

# New-CMConfigurationPolicyDeployment

## SYNOPSIS
Creates a configuration policy deployment.

## SYNTAX

### DeployFWPolicyByValueMandatory (Default)
```
New-CMConfigurationPolicyDeployment -FirewallPolicy <IResultObject> [-Schedule <IResultObject>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployCoMgmtPolicyByValueMandatory
```
New-CMConfigurationPolicyDeployment -CoManagementPolicy <IResultObject> [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployCoMgmtPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment -CoManagementPolicyId <String> [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployCoMgmtPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment -CoManagementPolicyName <String> [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployCommonPolicyByValueMandatory
```
New-CMConfigurationPolicyDeployment -CommonProfile <IResultObject> [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>]
 [-Schedule <IResultObject>] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployCommonPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment -CommonProfileId <String> [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>]
 [-Schedule <IResultObject>] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployCommonPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment -CommonProfileName <String> [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-ParameterValue <Int32>] [-PostponeDateTime <DateTime>]
 [-Schedule <IResultObject>] [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] -UserDataAndProfileId <String>
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] -UserDataAndProfileName <String>
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployUSMPolicyByValueMandatory
```
New-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] [-Schedule <IResultObject>] -UserDataAndProfile <IResultObject>
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] -RemoteConnectionProfileId <String> [-Schedule <IResultObject>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] -RemoteConnectionProfileName <String> [-Schedule <IResultObject>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployRCPolicyByValueMandatory
```
New-CMConfigurationPolicyDeployment [-EnableEnforcement <Boolean>] [-GenerateAlert <Boolean>]
 [-MonitoredByScom <Boolean>] [-OverrideServiceWindow <Boolean>] [-ParameterValue <Int32>]
 [-PostponeDateTime <DateTime>] -RemoteConnectionProfile <IResultObject> [-Schedule <IResultObject>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployFWPolicyByIdMandatory
```
New-CMConfigurationPolicyDeployment -FirewallPolicyId <String> [-Schedule <IResultObject>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeployFWPolicyByNameMandatory
```
New-CMConfigurationPolicyDeployment -FirewallPolicyName <String> [-Schedule <IResultObject>]
 [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

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

### -CoManagementPolicy
{{ Fill CoManagementPolicy Description }}

```yaml
Type: IResultObject
Parameter Sets: DeployCoMgmtPolicyByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CoManagementPolicyId
{{ Fill CoManagementPolicyId Description }}

```yaml
Type: String
Parameter Sets: DeployCoMgmtPolicyByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CoManagementPolicyName
{{ Fill CoManagementPolicyName Description }}

```yaml
Type: String
Parameter Sets: DeployCoMgmtPolicyByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommonProfile
{{ Fill CommonProfile Description }}

```yaml
Type: IResultObject
Parameter Sets: DeployCommonPolicyByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -CommonProfileId
{{ Fill CommonProfileId Description }}

```yaml
Type: String
Parameter Sets: DeployCommonPolicyByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CommonProfileName
{{ Fill CommonProfileName Description }}

```yaml
Type: String
Parameter Sets: DeployCommonPolicyByNameMandatory
Aliases:

Required: True
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
```yaml
Type: Boolean
Parameter Sets: DeployUSMPolicyByIdMandatory, DeployUSMPolicyByNameMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByValueMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FirewallPolicy
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
```yaml
Type: Boolean
Parameter Sets: DeployCommonPolicyByValueMandatory, DeployCommonPolicyByIdMandatory, DeployCommonPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByNameMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByValueMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MonitoredByScom
```yaml
Type: Boolean
Parameter Sets: DeployCommonPolicyByValueMandatory, DeployCommonPolicyByIdMandatory, DeployCommonPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByNameMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByValueMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
```yaml
Type: Boolean
Parameter Sets: DeployUSMPolicyByIdMandatory, DeployUSMPolicyByNameMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByValueMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParameterValue
```yaml
Type: Int32
Parameter Sets: DeployCommonPolicyByValueMandatory, DeployCommonPolicyByIdMandatory, DeployCommonPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByNameMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByValueMandatory
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
Parameter Sets: DeployCommonPolicyByValueMandatory, DeployCommonPolicyByIdMandatory, DeployCommonPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByNameMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByValueMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoteConnectionProfile
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
```yaml
Type: IResultObject
Parameter Sets: DeployFWPolicyByValueMandatory, DeployCommonPolicyByValueMandatory, DeployCommonPolicyByIdMandatory, DeployCommonPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByNameMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByValueMandatory, DeployFWPolicyByIdMandatory, DeployFWPolicyByNameMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserDataAndProfile
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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
