---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMApplicationAutoPhasedDeployment

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByValueMandatory
```
New-CMApplicationAutoPhasedDeployment [-Application] <IResultObject> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMApplicationAutoPhasedDeployment [-ApplicationId] <String> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMApplicationAutoPhasedDeployment [-ApplicationName] <String> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -Application
{{ Fill Application Description }}

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ApplicationId
{{ Fill ApplicationId Description }}

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationName
{{ Fill ApplicationName Description }}

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: ApplicationLocalizedDisplayName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BeginCondition
{{ Fill BeginCondition Description }}

```yaml
Type: BeginConditionType
Parameter Sets: (All)
Aliases:
Accepted values: AfterPeriod, Manually

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CriteriaOption
{{ Fill CriteriaOption Description }}

```yaml
Type: CriteriaType
Parameter Sets: (All)
Aliases:
Accepted values: Compliance, Number

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CriteriaValue
{{ Fill CriteriaValue Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DaysAfterPreviousPhaseSuccess
{{ Fill DaysAfterPreviousPhaseSuccess Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeadlineUnit
{{ Fill DeadlineUnit Description }}

```yaml
Type: TimeUnitType
Parameter Sets: (All)
Aliases:
Accepted values: Hours, Days, Weeks, Months

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeadlineValue
{{ Fill DeadlineValue Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
{{ Fill Description Description }}

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

### -FirstCollection
{{ Fill FirstCollection Description }}

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

### -FirstCollectionId
{{ Fill FirstCollectionId Description }}

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

### -FirstCollectionName
{{ Fill FirstCollectionName Description }}

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

### -InstallationChoice
{{ Fill InstallationChoice Description }}

```yaml
Type: InstallationChoiceType
Parameter Sets: (All)
Aliases:
Accepted values: AsSoonAsPossible, AfterPeriod

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SecondCollection
{{ Fill SecondCollection Description }}

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

### -SecondCollectionId
{{ Fill SecondCollectionId Description }}

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

### -SecondCollectionName
{{ Fill SecondCollectionName Description }}

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

### -ThrottlingDays
{{ Fill ThrottlingDays Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

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

### System.Object
## NOTES

## RELATED LINKS
