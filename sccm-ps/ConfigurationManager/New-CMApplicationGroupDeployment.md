---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMApplicationGroupDeployment

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByValueMandatory (Default)
```
New-CMApplicationGroupDeployment [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-GenerateScomAlertOnFailure <Boolean>]
 [-InputObject] <IResultObject> [-OverrideServiceWindow <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>]
 [-DistributeContent] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-AvailableDateTime <DateTime>] [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMApplicationGroupDeployment [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-GenerateScomAlertOnFailure <Boolean>]
 [-Id] <Int32> [-OverrideServiceWindow <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>]
 [-DistributeContent] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-AvailableDateTime <DateTime>] [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMApplicationGroupDeployment [-DeadlineDateTime <DateTime>] [-DeployAction <DeployActionType>]
 [-DeployPurpose <DeployPurposeType>] [-EnableMomAlert <Boolean>] [-GenerateScomAlertOnFailure <Boolean>]
 [-Name] <String> [-OverrideServiceWindow <Boolean>] [-RebootOutsideServiceWindow <Boolean>]
 [-TimeBaseOn <TimeType>] [-UserNotification <UserNotificationType>] [-DistributeCollectionName <String>]
 [-DistributeContent] [-DistributionPointGroupName <String>] [-DistributionPointName <String>]
 [-AvailableDateTime <DateTime>] [-Comment <String>] [-PersistOnWriteFilterDevice <Boolean>]
 [-SendWakeupPacket <Boolean>] [-UseMeteredNetwork <Boolean>] [-Collection <IResultObject>]
 [-CollectionId <String>] [-CollectionName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -AvailableDateTime
{{ Fill AvailableDateTime Description }}

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Collection
{{ Fill Collection Description }}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionId
{{ Fill CollectionId Description }}

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

### -CollectionName
{{ Fill CollectionName Description }}

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

### -Comment
{{ Fill Comment Description }}

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

### -DeadlineDateTime
{{ Fill DeadlineDateTime Description }}

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: SupersedenceDeadlineDateTime

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeployAction
{{ Fill DeployAction Description }}

```yaml
Type: DeployActionType
Parameter Sets: (All)
Aliases:
Accepted values: Install, Uninstall

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeployPurpose
{{ Fill DeployPurpose Description }}

```yaml
Type: DeployPurposeType
Parameter Sets: (All)
Aliases:
Accepted values: Available, Required

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -DistributeCollectionName
{{ Fill DistributeCollectionName Description }}

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

### -DistributeContent
{{ Fill DistributeContent Description }}

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

### -DistributionPointGroupName
{{ Fill DistributionPointGroupName Description }}

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

### -DistributionPointName
{{ Fill DistributionPointName Description }}

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

### -EnableMomAlert
{{ Fill EnableMomAlert Description }}

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

### -GenerateScomAlertOnFailure
{{ Fill GenerateScomAlertOnFailure Description }}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: RaiseMomAlertsOnFailure

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
{{ Fill Id Description }}

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID, ApplicationGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ApplicationGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, ApplicationGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OverrideServiceWindow
{{ Fill OverrideServiceWindow Description }}

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

### -PersistOnWriteFilterDevice
{{ Fill PersistOnWriteFilterDevice Description }}

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

### -RebootOutsideServiceWindow
{{ Fill RebootOutsideServiceWindow Description }}

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

### -SendWakeupPacket
{{ Fill SendWakeupPacket Description }}

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

### -TimeBaseOn
{{ Fill TimeBaseOn Description }}

```yaml
Type: TimeType
Parameter Sets: (All)
Aliases:
Accepted values: LocalTime, Utc

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseMeteredNetwork
{{ Fill UseMeteredNetwork Description }}

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

### -UserNotification
{{ Fill UserNotification Description }}

```yaml
Type: UserNotificationType
Parameter Sets: (All)
Aliases:
Accepted values: DisplayAll, DisplaySoftwareCenterOnly, HideAll

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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

### IResultObject#SMS_ApplicationGroupAssignment

## NOTES

## RELATED LINKS
