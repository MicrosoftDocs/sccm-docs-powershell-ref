---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/03/2021
online version:
schema: 2.0.0
---

# Get-CMPersistentUserSettingsGroup

## SYNOPSIS

Get the list of site-wide settings that you've stored.

## SYNTAX

```
Get-CMPersistentUserSettingsGroup [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to get the list of site-wide settings that you've stored. These settings follow you on different devices.

For example, [Configuration Manager console notifications](/mem/configmgr/core/servers/manage/admin-console-notifications) that are active or you've dismissed.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
Get-CMPersistentUserSettingsGroup
```

```output
SmsProviderObjectPath : SMS_PersistentUserSettingsGroup.GroupName="NotificationTasks"
GroupName             : NotificationTasks
LastModified          : 8/2/2021 09:38:11
SettingsBlob          : {
                          "ActiveTasks": "{\"2F738517-E6AC-4434-B601-A7DD2989A2D2\":\"2021-08-02T16:38:13.6451945Z\",\"
                        3142F9C1-E52C-426B-BFFC-6E2EC65E8799\":\"2021-07-13T18:25:38.062348Z\",\"5B059EC9-C45C-47C7-AD7
                        F-902848392274\":\"2021-08-02T16:38:13.6451945Z\",\"9B01B74C-A549-4223-A349-60CE6544845C\":\"20
                        21-07-19T17:45:28.0732112Z\",\"E1288582-4428-4E35-BCF3-23770253099C\":\"2021-08-02T16:38:13.645
                        1945Z\",\"99E42B9A-12DF-4D9D-9FE0-1F96140B8727\":\"2021-07-27T21:13:48.7410716Z\"}",
                          "SiteVersion": "\"5.0.9058.800\""
                        }
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

### -Name
{{ Fill Name Description }}
<!-- 10519922 -->


```yaml
Type: String
Parameter Sets: (All)
Aliases: GroupName

Required: False
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

### IResultObject#SMS_PersistentUserSettingsGroup

## NOTES

## RELATED LINKS

[Remove-CMPersistentUserSettingsGroup](Remove-CMPersistentUserSettingsGroup.md)
