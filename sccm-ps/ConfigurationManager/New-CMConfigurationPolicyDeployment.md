---
title: New-CMConfigurationPolicyDeployment
titleSuffix: Configuration Manager
description: Creates a configuration policy deployment.
ms.date: 05/05/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# New-CMConfigurationPolicyDeployment

## SYNOPSIS
Creates a configuration policy deployment.

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
 

## EXAMPLES

### Example 1
```
PS C:\>  
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
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
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
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
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
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
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
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
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
Parameter Sets: DeployUSMPolicyByNameMandatory, DeployUSMPolicyByIdMandatory, DeployUSMPolicyByValueMandatory, DeployRCPolicyByNameMandatory, DeployRCPolicyByIdMandatory, DeployRCPolicyByValueMandatory
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
Parameter Sets: (All)
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

