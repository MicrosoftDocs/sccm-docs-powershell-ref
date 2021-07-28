---
description: Get a compliance rule for a configuration item.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/23/2021
schema: 2.0.0
title: Get-CMComplianceRule
---

# Get-CMComplianceRule

## SYNOPSIS

Get a compliance rule for a configuration item.

## SYNTAX

### ById
```
Get-CMComplianceRule [-Fast] [-Id] <Int32> [-PropertyPath <String>] [-RuleName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByValue
```
Get-CMComplianceRule [-Fast] -InputObject <IResultObject> [-PropertyPath <String>] [-RuleName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByName
```
Get-CMComplianceRule [-Fast] [-Name] <String> [-PropertyPath <String>] [-RuleName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Get a compliance rule for a configuration item. Compliance rules specify the conditions that define the compliance of a configuration item setting. Before the client evaluates a setting for compliance, it must have at least one compliance rule. For more information, see [Get started with compliance settings in Configuration Manager](/mem/configmgr/compliance/get-started/get-started-with-compliance-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a compliance rule for a configuration item

```powershell
Get-CMComplianceRule -Name "BitLocker data drive protection" -RuleName "06 must exist" -Fast
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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

Specify the **CI_ID** for the configuration item that has the compliance rule you want to get. For example, `258895`.

```yaml
Type: Int32
Parameter Sets: ById
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a configuration item object that has the compliance rule you want to get. To get this object, use the [Get-CMConfigurationItem](Get-CMConfigurationItem.md).

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the configuration item that has the compliance rule you want to get.

```yaml
Type: String
Parameter Sets: ByName
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PropertyPath
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

### -RuleName

Specify the name of the compliance rule in the configuration item. This value is the same as the **Name** value on the **Compliance Rules** tab of the configuration item properties in the console.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### Microsoft.SystemsManagementServer.DesiredConfigurationManagement.Rules.Rule
## NOTES

## RELATED LINKS

[Get-CMConfigurationItem](Get-CMConfigurationItem.md)

[Get-CMComplianceSetting](Get-CMComplianceSetting.md)
