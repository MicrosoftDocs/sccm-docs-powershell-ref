---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 01/05/2021
online version:
schema: 2.0.0
---

# New-CMRequirementRuleRegistryKeyPermissionValue

## SYNOPSIS

Create a requirement rule to verify registry key permissions.

## SYNTAX

```
New-CMRequirementRuleRegistryKeyPermissionValue -ControlEntry <RegistryAccessControlEntry[]>
 [-Exclusive <Boolean>] [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a requirement rule on an application deployment type that verifies registry key permissions. It requires a custom global condition of data type **Registry key**.

> [!TIP]
> For comparison, if you manually create this requirement rule in the Configuration Manager console, select the following options:
>
> - Category: **Custom**
> - Condition: Select a custom global condition of data type **Registry key**
> - Rule type: **Value**
> - Property: **Permissions**

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a requirement rule for registry key permissions

This example first uses the **Get-CMGlobalCondition** cmdlet to get a custom global condition. Then it uses the **New-CMRegistryAccessControlEntry** cmdlet to create two access control entries for specific users. Next it creates the requirement rule object to check that the registry key has the permissions specified in the access control entries. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$myGC = Get-CMGlobalCondition -Name "LOB app registry key"

$userName = "contoso\jqpublic"
$ce = New-CMRegistryAccessControlEntry -GroupOrUserName $userName -AccessOption Allow -Permission Read,Write

$userName2 = "contoso\jdoe"
$ce2 = New-CMRegistryAccessControlEntry -GroupOrUserName $userName2 -AccessOption Allow -Permission Read

$myRule = $myGC | New-CMRequirementRuleRegistryKeyPermissionValue -Exclusive $false -ControlEntry $ce,$ce2

Set-CMScriptDeploymentType -ApplicationName "Central app" -DeploymentTypeName "Install" -AddRequirement $myRule
```

## PARAMETERS

### -ControlEntry

Specify an array of access control entry objects. An access control entry defines specific permissions for a specific user or group. To get this object, use the [New-CMRegistryAccessControlEntry](New-CMRegistryAccessControlEntry.md) cmdlet.

```yaml
Type: RegistryAccessControlEntry[]
Parameter Sets: (All)
Aliases: ControlEntries, RegistryAccessControlEntry, RegistryAccessControlEntries

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

### -Exclusive

If this parameter is `$true`, for the rule to be compliant, it needs to exactly match the specified ACE exactly. Any other permissions on the registry key cause the rule to fail.

If set to `$false`, for the rule to be compliant, the specified ACE must exist, and other permissions can exist as well.

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

Specify a custom global condition object to use as the basis for this requirement rule. To get this object, use the [Get-CMGlobalCondition](Get-CMGlobalCondition.md) cmdlet.

To see the list of available **Registry key** global conditions at the site, use the following PowerShell command:

`Get-CMGlobalCondition | Where-Object DataType -eq "RegistryKey" | Select-Object LocalizedDisplayName`

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMRegistryAccessControlEntry](New-CMRegistryAccessControlEntry.md)

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
[New-CMRequirementRuleOperatingSystemValue](New-CMRequirementRuleOperatingSystemValue.md)
[New-CMRequirementRuleOUValue](New-CMRequirementRuleOUValue.md)
[New-CMRequirementRuleScreenResolutionValue](New-CMRequirementRuleScreenResolutionValue.md)
[Get-CMGlobalCondition](Get-CMGlobalCondition.md)
[Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require)
[Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions)
