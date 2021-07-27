---
description: Get component status messages in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/25/2020
schema: 2.0.0
title: Get-CMComponentStatusMessage
---

# Get-CMComponentStatusMessage

## SYNOPSIS

Get component status messages in Configuration Manager.

## SYNTAX

```
Get-CMComponentStatusMessage [-ComponentName <String>] [-ComputerName <String>] [-Severity <Severity>]
 [-SiteCode <String>] -StartTime <DateTime> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMComponentStatusMessage** cmdlet gets component status messages for a specified period.

Configuration Manager indicates whether operations succeed or fail and include other information in component status messages.
Threads or processes send component status messages to Configuration Manager sites, which are identified by site codes.

You can define which messages to get by the severity of the message, the component that created the message, the computer that hosts that component, or the Configuration Manager server that receives the message.
Always specify a viewing period as a **TimeSpan** object.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get error messages for a site

This example gets all messages with the error severity from a specific start time.

```powershell
Get-CMComponentStatusMessage -StartTime "2/1/2013 12:00 AM" -Severity Error
```

### Example 2: Get warning messages for a site within the last 24 hours

This example gets all warnings for a specific site in the last day.

```powershell
Get-CMComponentStatusMessage -StartTime $(Get-Date).AddHours(-24) -Severity Warning -SiteCode "CM1"
```

### Example 3: Get summary of messages for all components within last 24 hours

This example first uses the **Get-CMSiteComponent** cmdlet to get a list of all components from the current site. It pipes this list through several cmdlets to format the list, and then loops through each component. For each component, it gets the error and warning status messages for the last day. It then summarizes the number of errors and warnings for each component in the last day.

> [!NOTE]
> This command can take several minutes to run.

```powershell
PS OPC:\> Get-CMSiteComponent | Select-Object -ExpandProperty ComponentName -Unique | Sort-Object ComponentName | ForEach-Object {
    $errs  = $(Get-CMComponentStatusMessage -ComponentName $_ -Severity Error -StartTime $(Get-Date).AddHours(-24)).Count
    $warns = $(Get-CMComponentStatusMessage -ComponentName $_ -Severity Warning -StartTime $(Get-Date).AddHours(-24)).Count
    [pscustomobject]@{
        Component  = $_
        Errors     = $errs
        Warnings   = $warns
    }
}

Component                             Errors Warnings
---------                             ------ --------
SMS_AD_SECURITY_GROUP_DISCOVERY_AGENT    742        0
SMS_WSUS_SYNC_MANAGER                     90        0
SMS_WSUS_CONFIGURATION_MANAGER             0        0
SMS_WSUS_CONTROL_MANAGER                  62        0
SMS_AD_SYSTEM_DISCOVERY_AGENT              0        0
SMS_CLIENT_HEALTH                          0        0
SMS_CLOUD_PROXYCONNECTOR                   0        0
SMS_AD_USER_DISCOVERY_AGENT                0      612
...
```

## PARAMETERS

### -ComponentName

Specifies the name of a thread or process. A thread or process sends a component status message.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Component

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputerName

Scope the status messages results and specify the name of a computer that hosts a component.

```yaml
Type: String
Parameter Sets: (All)
Aliases: MachineName

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

### -Severity

Specifies the severity of component status messages to get.

> [!NOTE]
> This parameter currently doesn't work with the `All` value, but also doesn't return any values if omitted.

```yaml
Type: Severity
Parameter Sets: (All)
Aliases:
Accepted values: All, Error, Warning, Information

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode

Specifies a site code from which to get component status messages.

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

### -StartTime

Specify a time for the start of the viewing period for the component status messages.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: ViewingPeriod

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject[]#SMS_StatusMessage
### IResultObject#SMS_StatusMessage
## NOTES

## RELATED LINKS

[Get-CMComponentStatusSetting](Get-CMComponentStatusSetting.md)

[Get-CMSiteComponent](Get-CMSiteComponent.md)
