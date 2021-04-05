---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2020
online version:
schema: 2.0.0
---

# New-CMRequirementRuleFileAttributeValue

## SYNOPSIS

Create a requirement rule to verify file attributes.

## SYNTAX

```
New-CMRequirementRuleFileAttributeValue [-FileArchive <AttributeVerificationOption>]
 [-FileCompressed <AttributeVerificationOption>] [-FileEncrypted <AttributeVerificationOption>]
 [-FileHidden <AttributeVerificationOption>] [-FileReadOnly <AttributeVerificationOption>]
 [-FileSystem <AttributeVerificationOption>] [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a requirement rule on an application deployment type that verifies file attributes. For example, **Hidden** or **Read only**. It requires a custom global condition of data type **File**.

> [!TIP]
> For comparison, if you manually create this requirement rule in the Configuration Manager console, select the following options:
>
> - Category: **Custom**
> - Condition: Select a custom global condition of data type **File**
> - Rule type: **Value**
> - Property: **Attributes**

After you use this cmdlet, then use one of the **Add-** or **Set-** cmdlets for deployment types. Pass this requirement rule object to either the **AddRequirement** or **RemoveRequirement** parameters.

For more information, see [Deployment type Requirements](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-require) and [Create global conditions](/mem/configmgr/apps/deploy-use/create-global-conditions).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **Get-CMGlobalCondition** cmdlet to get a custom global condition. Next it creates the requirement rule object to check that the file has the archive, hidden, and system bits turned on. Finally it passes that rule object to the **Set-CMScriptDeploymentType** cmdlet to add the requirement.

```powershell
$myGC = Get-CMGlobalCondition -Name "pagefile.sys"
$myRule = New-CMRequirementRuleFileAttributeValue -GlobalCondition $myGC -FileArchive On -FileHidden On -FileSystem On

Set-CMScriptDeploymentType -ApplicationName "Central app" -DeploymentTypeName "Install" -AddRequirement $myRule
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

### -FileArchive

Set this parameter to `On` to verify the **Archive** bit on the file. By default, the condition doesn't verify the attribute.

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileCompressed

Set this parameter to `On` to verify the **Compressed** bit on the file. By default, the condition doesn't verify the attribute.

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileEncrypted

Set this parameter to `On` to verify the **Encrypted** bit on the file. By default, the condition doesn't verify the attribute.

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileHidden

Set this parameter to `On` to verify the **Hidden** bit on the file. By default, the condition doesn't verify the attribute.

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileReadOnly

Set this parameter to `On` to verify the **Read only** bit on the file. By default, the condition doesn't verify the attribute.

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileSystem

Set this parameter to `On` to verify the **System** bit on the file. By default, the condition doesn't verify the attribute.

```yaml
Type: AttributeVerificationOption
Parameter Sets: (All)
Aliases:
Accepted values: On, Off, DoNotVerify

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

To see the list of available **File** global conditions at the site, use the following PowerShell command:

`Get-CMGlobalCondition | Where-Object DataType -eq "File" | Select-Object LocalizedDisplayName`

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

[New-CMRequirementRuleActiveDirectorySiteValue](New-CMRequirementRuleActiveDirectorySiteValue.md)
[New-CMRequirementRuleBooleanValue](New-CMRequirementRuleBooleanValue.md)
[New-CMRequirementRuleCMSiteValue](New-CMRequirementRuleCMSiteValue.md)
[New-CMRequirementRuleCommonValue](New-CMRequirementRuleCommonValue.md)
[New-CMRequirementRuleDeviceOwnershipValue](New-CMRequirementRuleDeviceOwnershipValue.md)
[New-CMRequirementRuleExistential](New-CMRequirementRuleExistential.md)
[New-CMRequirementRuleExpression](New-CMRequirementRuleExpression.md)
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
