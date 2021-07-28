---
description: Get Configuration Manager alerts.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/23/2021
schema: 2.0.0
title: Get-CMAlert
---

# Get-CMAlert

## SYNOPSIS

Get Configuration Manager alerts.

## SYNTAX

### SearchByName (Default)
```
Get-CMAlert [-Fast] [[-Name] <String>] [-TypeId <Int32>] [-TypeInstanceId <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMAlert [-Fast] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get one or more Configuration Manager alerts. You can get a specific alert by specifying the name or ID of the alert.

Configuration Manager generates alerts from certain operations when a specific condition occurs. Typically, it generates alerts when an error occurs that you need to resolve. For more information, see [Configure alerts in Configuration Manager](/mem/configmgr/core/servers/manage/configure-alerts).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all alerts

This command gets all alerts that Configuration Manager manages.

```powershell
Get-CMAlert
```

### Example 2: Get alerts by using name

This command gets all alerts that have a name that begins with the character `$`.

```powershell
Get-CMAlert -Name "$*" | Select-Object Id, Name, AlertState
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

Specify an alert ID. For example, `33554436`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify an alert name. You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

Alerts whose name begins with the `$` character are default, system alerts.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -TypeId

Specify the identifier for this type of alert.

```yaml
Type: Int32
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -TypeInstanceId

Specify the user-defined identifier.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_Alert
### IResultObject#SMS_CHAlert
### IResultObject#SMS_EPAlert
## NOTES

For more information on these return objects and their properties, see the following articles:

- [SMS_Alert server WMI class](/mem/configmgr/develop/reference/core/servers/manage/sms_alert-server-wmi-class)
- [SMS_CHAlert server WMI class](/mem/configmgr/develop/reference/core/servers/manage/sms_chalert-server-wmi-class)
- [SMS_EPAlert server WMI class](/mem/configmgr/develop/reference/core/servers/manage/sms_epalert-server-wmi-class)

## RELATED LINKS

[Enable-CMAlert](Enable-CMAlert.md)

[Remove-CMAlert](Remove-CMAlert.md)

[Set-CMAlert](Set-CMAlert.md)

[Suspend-CMAlert](Suspend-CMAlert.md)

[Disable-CMAlert](Disable-CMAlert.md)

[Configure alerts in Configuration Manager](/mem/configmgr/core/servers/manage/configure-alerts)
