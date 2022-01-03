---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Set-CMBaseline
---

# Set-CMBaseline

## SYNOPSIS

Change the settings of configuration baselines.

## SYNTAX

### SetByIdMandatory (Default)
```
Set-CMBaseline [-AddBaseline <String[]>] [-AddCategory <String[]>] [-AddOptionalConfigurationItem <String[]>]
 [-AddOSConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddSoftwareUpdate <String[]>] [-AllowComanagedClients <Boolean>]
 [-ClearBaseline] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearRequiredConfigurationItem] [-ClearSoftwareUpdate]
 [-Description <String>] [-DesiredConfigurationDigestPath <String>] -Id <Int32> [-NewName <String>] [-PassThru]
 [-RemoveBaseline <String[]>] [-RemoveCategory <String[]>] [-RemoveOptionalConfigurationItem <String[]>]
 [-RemoveOSConfigurationItem <String[]>] [-RemoveProhibitedConfigurationItem <String[]>]
 [-RemoveRequiredConfigurationItem <String[]>] [-RemoveSoftwareUpdate <String[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByNameMandatory
```
Set-CMBaseline [-AddBaseline <String[]>] [-AddCategory <String[]>] [-AddOptionalConfigurationItem <String[]>]
 [-AddOSConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddSoftwareUpdate <String[]>] [-AllowComanagedClients <Boolean>]
 [-ClearBaseline] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearRequiredConfigurationItem] [-ClearSoftwareUpdate]
 [-Description <String>] [-DesiredConfigurationDigestPath <String>] -Name <String> [-NewName <String>]
 [-PassThru] [-RemoveBaseline <String[]>] [-RemoveCategory <String[]>]
 [-RemoveOptionalConfigurationItem <String[]>] [-RemoveOSConfigurationItem <String[]>]
 [-RemoveProhibitedConfigurationItem <String[]>] [-RemoveRequiredConfigurationItem <String[]>]
 [-RemoveSoftwareUpdate <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMBaseline [-AddBaseline <String[]>] [-AddCategory <String[]>] [-AddOptionalConfigurationItem <String[]>]
 [-AddOSConfigurationItem <String[]>] [-AddProhibitedConfigurationItem <String[]>]
 [-AddRequiredConfigurationItem <String[]>] [-AddSoftwareUpdate <String[]>] [-AllowComanagedClients <Boolean>]
 [-ClearBaseline] [-ClearOptionalConfigurationItem] [-ClearOSConfigurationItem]
 [-ClearProhibitedConfigurationItem] [-ClearRequiredConfigurationItem] [-ClearSoftwareUpdate]
 [-Description <String>] [-DesiredConfigurationDigestPath <String>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-RemoveBaseline <String[]>] [-RemoveCategory <String[]>]
 [-RemoveOptionalConfigurationItem <String[]>] [-RemoveOSConfigurationItem <String[]>]
 [-RemoveProhibitedConfigurationItem <String[]>] [-RemoveRequiredConfigurationItem <String[]>]
 [-RemoveSoftwareUpdate <String[]>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to change the settings of a configuration baseline in Configuration Manager. A configuration baseline can include the following types of configuration data:

- Configuration items
- Other configuration baselines
- Software updates

The Configuration Manager client evaluates its compliance against this baseline. If all of the specified items are compliant, then the baseline itself is assessed as compliant. You can also include optional items, which are only evaluated if the relevant application or setting exists on the device.

For more information, see [Create configuration baselines in Configuration Manager](/mem/configmgr/compliance/deploy-use/create-configuration-baselines).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Configure a configuration baseline

This example first uses the [Get-CMConfigurationItem](Get-CMConfigurationItem.md) cmdlet to get a series of configuration items (CIs).

It then [splats](/powershell/module/microsoft.powershell.core/about/about_splatting) the cmdlet parameters into the **parameters** variable. It's not required to splat the parameters, it just makes it easier to read the parameters for such a long command line.

The last command configures the **PSTestBaseLine** baseline with a new name and description, removes a category, and adds the CIs.

```powershell
$objPSTestWinAppCI = Get-CMConfigurationItem -Name PSTestWinAppCI
$objPSTestWinAppCI2 = Get-CMConfigurationItem -Name PSTestWinAppCI2
$objPSTestWinOSCI = Get-CMConfigurationItem -Name PSTestWinOSCI
$objPSTestWinAppCI3 = Get-CMConfigurationItem -Name PSTestWinAppCI3
$objPSTestWinAppCI4 = Get-CMConfigurationItem -Name PSTestWinAppCI4
$objPSTestMDCI = Get-CMConfigurationItem -Name PSTestMDCI
$objPSTestMacCI = Get-CMConfigurationItem -Name PSTestMacCI

$parameters = @{
  Name = "PSTestBaseLine"
  NewName = "PSTestBaseLineNew"
  Description = "DCM Testing New"
  RemoveCategory = ("IT Infrastructure")
  AddRequiredConfigurationItems = ($objPSTestWinAppCI4.CI_ID,$objPSTestMDCI.CI_ID)
  AddProhibitedConfigurationItems = ($objPSTestWinAppCI.CI_ID)
  AddOSConfigurationItems = ($objPSTestWinOSCI.CI_ID,$objPSTestMacCI.CI_ID)
  AddOptionalConfigurationItems = ($objPSTestWinAppCI2.CI_ID,$objPSTestWinAppCI3.CI_ID)
}

Set-CMBaseline @parameters
```

### Example 2: Add a custom category

This example first uses the **New-CMCategory** cmdlet to create a custom baseline category **Accounting**.
It then configures the **Accounting baseline** to add the new category.

```powershell
$category = New-CMCategory -CategoryType BaselineCategories -Name "Accounting"
Set-CMBaseline -Name "Accounting baseline" -AddCategory $category.LocalizedCategoryInstanceName
```

## PARAMETERS

### -AddBaseline

Specify an array of baseline IDs to add as configuration data to the target baseline. This value is the **CI_ID** property of the baseline, for example, `16777516`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddBaselines

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddCategory

Specify an array of configuration category names to add to the configuration baselines. These categories improve searching and filtering. By default, the site includes the following categories for configuration baselines:

- Client
- IT Infrastructure
- Line of Business
- Server

To use another category, first add it with the [New-CMCategory](New-CMCategory.md) cmdlet and `-CategoryType BaselineCategories` parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOptionalConfigurationItem

Specify an array of configuration item IDs to add with an _optional_ purpose. The Configuration Manager client only evaluates optional items if the relevant application exists on the device.

This value is the **CI_ID** property of the configuration item, for example, `16777514`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddOptionalConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddOSConfigurationItem

Specify an array of configuration item IDs to add of type _OS_. This value is the **CI_ID** property of the configuration item, for example, `16777514`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddOSConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddProhibitedConfigurationItem

Specify an array of configuration item IDs to add with a _prohibited_ purpose. This value is the **CI_ID** property of the configuration item, for example, `16777514`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddProhibitedConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddRequiredConfigurationItem

Specify an array of configuration item IDs to add with a _required_ purpose. This value is the **CI_ID** property of the configuration item, for example, `16777514`.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddRequiredConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddSoftwareUpdate

Specify an array of software update IDs to add.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: AddSoftwareUpdates

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AllowComanagedClients

Set this parameter to `$true` to always apply this baseline even for co-managed clients.

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

### -ClearBaseline

Add this parameter to remove all baselines as evaluation conditions from the target baseline. To remove individual baselines, use the **RemoveBaseline** parameter.

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

### -ClearOptionalConfigurationItem

Add this parameter to remove all _optional_ configuration items as evaluation conditions from the target baseline. To remove individual optional CIs, use the **RemoveOptionalConfigurationItem** parameter.

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

### -ClearOSConfigurationItem

Add this parameter to remove all _OS_ configuration items as evaluation conditions from the target baseline. To remove individual OS CIs, use the **RemoveOSConfigurationItem** parameter.

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

### -ClearProhibitedConfigurationItem

Add this parameter to remove all _prohibited_ configuration items as evaluation conditions from the target baseline. To remove individual prohibited CIs, use the **RemoveProhibitedConfigurationItem** parameter.

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

### -ClearRequiredConfigurationItem

Add this parameter to remove all _required_ configuration items as evaluation conditions from the target baseline. To remove individual required CIs, use the **RemoveRequiredConfigurationItem** parameter.

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

### -ClearSoftwareUpdate

Add this parameter to remove all software updates as evaluation conditions from the target baseline. To remove individual software updates, use the **RemoveSoftwareUpdate** parameter.

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

### -Description

Specify an optional description of the configuration baseline to help identify it.

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

### -DesiredConfigurationDigestPath

Specify a path to the configuration data stored as an XML digest.

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

Specify the **CI_ID** of the configuration baseline to configure. For example, `16777516`.

```yaml
Type: Int32
Parameter Sets: SetByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a configuration baseline object to configure. To get this object, use the [Get-CMBaseline](Get-CMBaseline.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the configuration baseline to configure.

```yaml
Type: String
Parameter Sets: SetByNameMandatory
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specify a new name for the configuration baseline. Use this parameter to rename the target baseline.

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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -RemoveBaseline

Specify an array of baseline IDs to remove as configuration data from the target baseline. This value is the **CI_ID** property of the baseline, for example, `16777516`. To remove all baselines as configuration data from this baseline, use the **ClearBaseline** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveBaselines

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveCategory

Specify an array of configuration category names to remove from the configuration baseline.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOptionalConfigurationItem

Specify an array of _optional_ CI IDs to remove as configuration data from the target baseline. This value is the **CI_ID** property of the configuration item, for example, `16777514`. To remove all optional configuration items from this baseline, use the **ClearOptionalConfigurationItem** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveOptionalConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveOSConfigurationItem

Specify an array of _OS_ CI IDs to remove as configuration data from the target baseline. This value is the **CI_ID** property of the configuration item, for example, `16777514`. To remove all OS configuration items from this baseline, use the **ClearOSConfigurationItem** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveOSConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveProhibitedConfigurationItem

Specify an array of _prohibited_ CI IDs to remove as configuration data from the target baseline. This value is the **CI_ID** property of the configuration item, for example, `16777514`. To remove all prohibited configuration items from this baseline, use the **ClearProhibitedConfigurationItem** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveProhibitedConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveRequiredConfigurationItem

Specify an array of _required_ CI IDs to remove as configuration data from the target baseline. This value is the **CI_ID** property of the configuration item, for example, `16777514`. To remove all required configuration items from this baseline, use the **ClearRequiredConfigurationItem** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveRequiredConfigurationItems

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSoftwareUpdate

Specify an array of software update IDs to remove as configuration data from the target baseline. To remove all software updates from this baseline, use the **ClearSoftwareUpdate** parameter.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: RemoveSoftwareUpdates

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Disable-CMBaseline](Disable-CMBaseline.md)

[Enable-CMBaseline](Enable-CMBaseline.md)

[Export-CMBaseline](Export-CMBaseline.md)

[Get-CMBaseline](Get-CMBaseline.md)

[Import-CMBaseline](Import-CMBaseline.md)

[New-CMBaseline](New-CMBaseline.md)

[Remove-CMBaseline](Remove-CMBaseline.md)

[Get-CMBaselineXMLDefinition](Get-CMBaselineXMLDefinition.md)

[Get-CMBaselineSummarizationSchedule](Get-CMBaselineSummarizationSchedule.md)

[Create configuration baselines in Configuration Manager](/mem/configmgr/compliance/deploy-use/create-configuration-baselines)
