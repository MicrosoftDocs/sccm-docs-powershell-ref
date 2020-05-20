---
description: Gets a configuration policy deployment.
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMConfigurationPolicyDeployment
---

# Get-CMConfigurationPolicyDeployment

## SYNOPSIS
Gets a configuration policy deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMConfigurationPolicyDeployment [-Name <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchById
```
Get-CMConfigurationPolicyDeployment [-SmsObjectId <Int32>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMConfigurationPolicyDeployment [-DeploymentId <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMConfigurationPolicyDeployment [-InputObject <IResultObject>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
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

### -DeploymentId
```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentUniqueID, ConfigurationPolicyDeploymentID

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
```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: ConfigurationPolicy

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ConfigurationPolicyName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SmsObjectId
```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, ConfigurationPolicyID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Summary
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_DeploymentSummary

### IResultObject#SMS_DeploymentSummary

### IResultObject[]#SMS_ConfigurationPolicyAssignment

### IResultObject#SMS_ConfigurationPolicyAssignment

## NOTES

## RELATED LINKS
