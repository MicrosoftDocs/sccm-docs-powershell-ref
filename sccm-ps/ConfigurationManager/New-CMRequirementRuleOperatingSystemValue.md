---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/04/2021
online version:
schema: 2.0.0
---

# New-CMRequirementRuleOperatingSystemValue

## SYNOPSIS

Create an OS requirement rule for an application deployment type.

## SYNTAX

```
New-CMRequirementRuleOperatingSystemValue [-Platform <IResultObject[]>] [-PlatformString <String[]>]
 -RuleOperator <RuleExpressionOperator> [-SelectFullPlatform <FullPlatformOption>]
 [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create an OS requirement rule for an application deployment type.

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a requirement rule for an OS by platform

This example first uses the **Get-CMGlobalCondition** cmdlet to get the default **Operating system** global condition for non-mobile Windows devices. It then uses the **Get-CMConfigurationPlatform** cmdlet to define variables for two platforms for Windows Server 2016 and Windows Server 2019. Next it creates the requirement rule object to include these two platforms. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$myGC = Get-CMGlobalCondition -Name "Operating System" | Where-Object PlatformType -eq 1

$platformA = Get-CMConfigurationPlatform -Name "All Windows Server 2019 and higher (64-bit)"

$platformB = Get-CMConfigurationPlatform -Name "All Windows Server 2016 and higher (64-bit)"

$myRule = $myGC | New-CMRequirementRuleOperatingSystemValue -RuleOperator OneOf -Platform $platformA, $platformB

Set-CMScriptDeploymentType -ApplicationName "Central App" -DeploymentTypeName "Install" -AddRequirement $myRule
```

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

Specify a global condition object to use as the basis for this requirement rule. To get this object, use the [Get-CMGlobalCondition](Get-CMGlobalCondition.md) cmdlet.

In most instances, you'll use the default **Operating system** global condition for non-mobile Windows devices. For example: `Get-CMGlobalCondition -Name "Operating System" | Where-Object PlatformType -eq 1`.

> [!NOTE]
> By default, Configuration Manager has two global conditions named **Operating system**. You can distinguish them by device type using the **PlatformType** property:
>
> |PlatformType|Device type|
> |---------|---------|
> |`1`|Windows|
> |`2`|Mobile|

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

### -Platform

Specify an array of one or more OS platform objects. To get this object, use the [Get-CMConfigurationPlatform](Get-CMConfigurationPlatform.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Platforms

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PlatformString

Instead of using the **Get-CMConfigurationPlatform** cmdlet with the **Platform** parameter, you can use this parameter to specify an array of one or more known **CI_ID** strings. For example, the **CI_ID** for the platform **All Windows Server 2019 and higher (64-bit)** is `287650`.

Use a command similar to the following to discover the CI_ID for a platform:

`Get-CMConfigurationPlatform -Name "*Server 2019*" | Select-Object LocalizedDisplayName, CI_ID`

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: PlatformStrings, PlatformCIUniqueID, PlatformCIUniqueIDs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RuleOperator

Specify the operator to compare the device's setting with the expected value.

```yaml
Type: RuleExpressionOperator
Parameter Sets: (All)
Aliases:
Accepted values: OneOf, NoneOf

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SelectFullPlatform

Use this parameter to select all platforms of the specified type.

```yaml
Type: FullPlatformOption
Parameter Sets: (All)
Aliases:
Accepted values: Windows, Nokia, WindowsMobile, IOs, IOsDeepLink, Android, AndroidDeepLink, Mac, WinPhone8, WinPhone8DeepLink, MobileMsi

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

[Get-CMConfigurationPlatform](Get-CMConfigurationPlatform.md)

[New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
[New-CMRequirementRuleBooleanValue](New-CMRequirementRuleBooleanValue.md)
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
[New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
[New-CMRequirementRuleRegistryKeyPermissionValue](New-CMRequirementRuleRegistryKeyPermissionValue.md)
[New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)
[Get-CMGlobalCondition](Get-CMGlobalCondition.md)
[Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require)
[Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions)
