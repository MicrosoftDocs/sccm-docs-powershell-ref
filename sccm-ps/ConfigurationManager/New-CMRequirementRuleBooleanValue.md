---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
online version:
schema: 2.0.0
---

# New-CMRequirementRuleBooleanValue

## SYNOPSIS

Create a requirement rule to evaluate a boolean global condition on an application deployment type.

## SYNTAX

```
New-CMRequirementRuleBooleanValue -Value <Boolean> [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a requirement rule on an application deployment type that evaluates a boolean global condition. The global condition defines the specific criteria, and this requirement rule evaluates the boolean state of that global condition on the device.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Check for co-managed state

This example first uses the **Get-CMGlobalCondition** cmdlet to get the default **Co-managed device** global condition. Next it creates the requirement rule object to evaluate the global condition as `$true`. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$myGC = Get-CMGlobalCondition -Name "Co-managed device"
$myRule = New-CMRequirementRuleBooleanValue -GlobalCondition $myGC -Value $true

Set-CMScriptDeploymentType -ApplicationName "Central app" -DeploymentTypeName "Install" -AddRequirement $myRule
```

You can also use this example with the default **Primary device** global condition, which is the only default **User** type global condition.

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

### -InputObject

Specify a boolean global condition object to use as the basis for this requirement rule. To get this object, use the [Get-CMGlobalCondition](Get-CMGlobalCondition.md) cmdlet.

To see the list of available boolean global conditions at the site, use the following PowerShell command:

`Get-CMGlobalCondition | Where-Object DataType -eq "Boolean" | Select-Object LocalizedDisplayName`

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: GlobalCondition

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Value

Specify the boolean state that this requirement rule should evaluate the global condition on the device. In other words, if you want to require the global condition to be true on the device, set this parameter to `$true`.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
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

[New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
[New-CMRequirementRuleCMSiteValue](New-CMRequirementRuleCMSiteValue.md)
[New-CMRequirementRuleCommonValue](New-CMRequirementRuleCommonValue.md)
[New-CMRequirementRuleDeviceOwnershipValue](New-CMRequirementRuleDeviceOwnershipValue.md)
[New-CMRequirementRuleExistential](New-CMRequirementRuleExistential.md)
[New-CMRequirementRuleExpression](New-CMRequirementRuleExpression.md)
[New-CMRequirementRuleFileAttributeValue](New-CMRequirementRuleFileAttributeValue.md)
[New-CMRequirementRuleFilePermissionValue](New-CMRequirementRuleFilePermissionValue.md)
[New-CMRequirementRuleFreeDiskSpaceValue](New-CMRequirementRuleFreeDiskSpaceValue.md)
[New-CMRequirementRuleInputTypeValue](New-CMRequirementRuleInputTypeValue.md)
[New-CMRequirementRuleOperatingSystemLanguageValue](New-CMRequirementRuleOperatingSystemLanguageValue.md)
[New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
[New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
[New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
[New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)
[Get-CMGlobalCondition](Get-CMGlobalCondition.md)
[Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require)
[Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions)
