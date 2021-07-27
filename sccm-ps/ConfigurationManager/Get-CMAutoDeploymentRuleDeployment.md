---
description: Gets the deployments associated with an automatic deployment rule.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMAutoDeploymentRuleDeployment
---

# Get-CMAutoDeploymentRuleDeployment

## SYNOPSIS
Gets the deployments associated with an automatic deployment rule.

## SYNTAX

### ByName (Default)
```
Get-CMAutoDeploymentRuleDeployment [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ById
```
Get-CMAutoDeploymentRuleDeployment [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ByValue
```
Get-CMAutoDeploymentRuleDeployment [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMAutoDeploymentRuleDeployment** cmdlet gets the deployments associated with an automatic deployment rule.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a deployment object for an automatic deployment rule
```
PS XYZ:\>Get-CMAutoDeploymentRuleDeployment -Name "AutoDeploymentRule01"
```

This command gets the deployment object for the automatic deployment rule named AutoDeploymentRule01.

### Example 2: Get a deployment object for an automatic deployment rule using the pipeline
```
PS XYZ:\>Get-CMSoftwareUpdateAutoDeploymentRule -Name "TestRule01" | Get-CMAutoDeploymentRuleDeployment
```

This command gets the automatic deployment rule object named TestRule01 and uses the pipeline operator to pass the object to **Get-CMAutoDeploymentRuleDeployment**, which gets the deployments associated with the automatic deployment rule named TestRule01.

## PARAMETERS

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

### -Id
Specifies the ID of the automatic deployment rule associated with the deployment.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: AutoDeploymentID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the auto deployment rule object associated with the deployment.
To obtain an auto deployment rule object, use the [Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: AutoDeploymentRule

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of the automatic deployment rule associated with the deployment.

```yaml
Type: String
Parameter Sets: ByName
Aliases: AutoDeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject#SMS_AdrDeploymentSettings
## NOTES

## RELATED LINKS

[New-CMAutoDeploymentRuleDeployment](New-CMAutoDeploymentRuleDeployment.md)

[Remove-CMAutoDeploymentRuleDeployment](Remove-CMAutoDeploymentRuleDeployment.md)

[Set-CMAutoDeploymentRuleDeployment](Set-CMAutoDeploymentRuleDeployment.md)

[Get-CMSoftwareUpdateAutoDeploymentRule](Get-CMSoftwareUpdateAutoDeploymentRule.md)
