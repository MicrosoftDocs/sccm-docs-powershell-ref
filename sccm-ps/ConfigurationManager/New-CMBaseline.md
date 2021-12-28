---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: New-CMBaseline
---

# New-CMBaseline

## SYNOPSIS

Create a configuration baseline.

## SYNTAX

```
New-CMBaseline [-AllowComanagedClients] [-Category <String[]>] [-Description <String>] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a configuration baseline. A baseline is a collection of configuration items that Configuration Manager uses to evaluate whether a computer complies with software requirements. For more information, see [Create configuration baselines in Configuration Manager](/mem/configmgr/compliance/deploy-use/create-configuration-baselines).

After you create a baseline, use the [Set-CMBaseline](Set-CMBaseline.md) cmdlet to add configuration items. Then use the [New-CMBaselineDeployment](New-CMBaselineDeployment.md) cmdlet to deploy the baseline to a collection. When deployed, devices in that collection download the configuration baseline and assess compliance with it.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a configuration baseline

This command creates a baseline for compliance named **Accounting Department baseline**.
The command specifies a description for the baseline.

```powershell
New-CMBaseline -Name "Accounting Department baseline" -Description "Compliance standards for Accounting computers."
```

## PARAMETERS

### -AllowComanagedClients

Add this parameter to always apply this baseline even for co-managed clients.

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

### -Category

Specify an array of configuration category names to add to the configuration baselines. These categories improve searching and filtering. By default, the site includes the following categories for configuration baselines:

- Client
- IT Infrastructure
- Line of Business
- Server

To use another category, first add it with the [New-CMCategory](New-CMCategory.md) cmdlet and `-CategoryType BaselineCategories` parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: LocalizedCategoryInstanceNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description for the baseline to help identify it.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

Required: False
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

### -Name

Specify a name for the configuration baseline.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDisplayName

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

### None

## OUTPUTS

### IResultObject#SMS_ConfigurationBaselineInfo

## NOTES

For more information on this return object and its properties, see [SMS_ConfigurationBaselineInfo server WMI class](/mem/configmgr/develop/reference/compliance/sms_configurationbaselineinfo-server-wmi-class).

## RELATED LINKS

[Disable-CMBaseline](Disable-CMBaseline.md)

[Enable-CMBaseline](Enable-CMBaseline.md)

[Export-CMBaseline](Export-CMBaseline.md)

[Get-CMBaseline](Get-CMBaseline.md)

[Import-CMBaseline](Import-CMBaseline.md)

[Remove-CMBaseline](Remove-CMBaseline.md)

[Set-CMBaseline](Set-CMBaseline.md)

[New-CMBaselineDeployment](New-CMBaselineDeployment.md)

[Create configuration baselines in Configuration Manager](/mem/configmgr/compliance/deploy-use/create-configuration-baselines)
