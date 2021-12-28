---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/28/2021
schema: 2.0.0
title: Get-CMBaseline
---

# Get-CMBaseline

## SYNOPSIS

Get a configuration baseline.

## SYNTAX

### SearchByName (Default)
```
Get-CMBaseline [-Fast] [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMBaseline [-Fast] [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByParentBaseline
```
Get-CMBaseline [-Fast] [-ParentBaseline] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaselineIdMandatory
```
Get-CMBaseline [-Fast] -ParentBaselineId <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByParentBaselineNameMandatory
```
Get-CMBaseline [-Fast] -ParentBaselineName <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more configuration baselines. Use configuration baselines to evaluate compliance of a device. For more information, see [Get started with compliance settings in Configuration Manager](/mem/configmgr/compliance/get-started/get-started-with-compliance-settings).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get configuration baselines by using a parent baseline name

This command gets the child configuration baselines in the parent baseline configuration item named **ParentBaselineContoso01**.

```powershell
Get-CMBaseline -ParentBaselineName "ParentBaselineContoso01"
```

### Example 2: Get configuration baselines by using a parent baseline ID

This command gets the child configuration baselines in the parent baseline configuration item that has the ID **16777357**.

```powershell
Get-CMBaseline -ParentBaselineId "16777357"
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

Specify the ID of a configuration baseline. This value is the same as the **CI_ID** attribute. For example, `33554545`.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of a configuration baseline. This value is the same as the **LocalizedDisplayName** attribute.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ParentBaseline

Specify a configuration baseline object that's a parent baseline.

```yaml
Type: IResultObject
Parameter Sets: SearchByParentBaseline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentBaselineId

Specify the ID of a parent configuration baseline.

```yaml
Type: Int32
Parameter Sets: SearchByParentBaselineIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentBaselineName

Specify the name of a parent configuration baseline.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: SearchByParentBaselineNameMandatory
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

### IResultObject[]#SMS_ConfigurationBaselineInfo
### IResultObject#SMS_ConfigurationBaselineInfo
### IResultObject[]#SMS_ConfigurationItem
### IResultObject#SMS_ConfigurationItem
### IResultObject[]#SMS_SoftwareUpdate
### IResultObject#SMS_SoftwareUpdate

## NOTES

For more information on these return objects and their properties, see the following articles:

- [SMS_ConfigurationBaselineInfo server WMI class](/mem/configmgr/develop/reference/compliance/sms_configurationbaselineinfo-server-wmi-class)
- [SMS_ConfigurationItem server WMI class](/mem/configmgr/develop/reference/compliance/sms_configurationitem-server-wmi-class)
- [SMS_SoftwareUpdate server WMI class](/mem/configmgr/develop/reference/sum/sms_softwareupdate-server-wmi-class)

## RELATED LINKS

[Disable-CMBaseline](Disable-CMBaseline.md)

[Enable-CMBaseline](Enable-CMBaseline.md)

[Export-CMBaseline](Export-CMBaseline.md)

[Import-CMBaseline](Import-CMBaseline.md)

[New-CMBaseline](New-CMBaseline.md)

[Remove-CMBaseline](Remove-CMBaseline.md)

[Set-CMBaseline](Set-CMBaseline.md)

[Get-CMBaselineSummarizationSchedule](Get-CMBaselineSummarizationSchedule.md)

[Get started with compliance settings in Configuration Manager](/mem/configmgr/compliance/get-started/get-started-with-compliance-settings)
