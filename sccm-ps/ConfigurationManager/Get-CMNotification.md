---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMNotification

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ByName (Default)
```
Get-CMNotification [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ById
```
Get-CMNotification -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### ByType
```
Get-CMNotification -Type <NotificationType[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill Id Description }}

```yaml
Type: String
Parameter Sets: ById
Aliases: TaskId, Task_Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: ByName
Aliases: TaskName, Task_Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
{{ Fill Type Description }}

```yaml
Type: NotificationType[]
Parameter Sets: ByType
Aliases: Types
Accepted values: SiteVersionOutOfSupport, ConsoleVersionMismatch, SiteReadonly, SiteVersionToBeExpired, EvalVersionExpired, EvalVersionApproachExpiration, UpdatePackageAvailable, SiteBusy, CloudConnectorMissing, PushNotificationsStayInformed, PushNotificationsPlanForChange, PushNotificationsFixIssue, OfficeAdrObsoleteChannelName, AzureTenantCertApproachExpiration, AzureTenantCertExpired, ManagementInsightsWin10OutOfSupport, ManagementInsightsWin7OutOfSupport, ConsoleCustomExtensionsFound, CloudConnectivityBroken, AzureTenantCertCloseToExpiration, ManagementInsightsGeneric, CloudAttachOnboard

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

### ConnectionManagerNotificationTaskBase

### ConnectionManagerNotificationTaskBase[]

## NOTES

## RELATED LINKS
