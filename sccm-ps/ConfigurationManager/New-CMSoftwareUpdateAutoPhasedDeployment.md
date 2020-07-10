---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMSoftwareUpdateAutoPhasedDeployment

## SYNOPSIS

Use this cmdlet to create a phased deployment for software updates by generating two phases with same settings.

## SYNTAX

### SearchByValueMandatory
```
New-CMSoftwareUpdateAutoPhasedDeployment [-SoftwareUpdates] <IResultObject[]>
 [-FirstCollection <IResultObject>] [-FirstCollectionId <String>] [-FirstCollectionName <String>]
 [-SecondCollection <IResultObject>] [-SecondCollectionId <String>] [-SecondCollectionName <String>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>]
 [-DaysAfterPreviousPhaseSuccess <Int32>] [-ThrottlingDays <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMSoftwareUpdateAutoPhasedDeployment [-SoftwareUpdateIds] <String[]> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMSoftwareUpdateAutoPhasedDeployment [-SoftwareUpdateNames] <String[]> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByGroupMandatory
```
New-CMSoftwareUpdateAutoPhasedDeployment [-SoftwareUpdateGroup] <IResultObject>
 [-FirstCollection <IResultObject>] [-FirstCollectionId <String>] [-FirstCollectionName <String>]
 [-SecondCollection <IResultObject>] [-SecondCollectionId <String>] [-SecondCollectionName <String>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>]
 [-DaysAfterPreviousPhaseSuccess <Int32>] [-ThrottlingDays <Int32>]
 [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>]
 [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String> [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByGroupIdMandatory
```
New-CMSoftwareUpdateAutoPhasedDeployment [-SoftwareUpdateGroupId] <String> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByGroupNameMandatory
```
New-CMSoftwareUpdateAutoPhasedDeployment [-SoftwareUpdateGroupName] <String> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to create a phased deployment for software updates by generating two phases with same settings.

## EXAMPLES

### Example 1: Create a deployment by update name

This example creates a new software update phased deployment named **myDPName** for the software update **myUpdateName**.

```powershell
New-CMSoftwareUpdateAutoPhasedDeployment -SoftwareUpdateName "myUpdateName" -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

### Example 2: Create a deployment by input update object

This example creates a new software update phased deployment named **myPDName** for a piped software update object.

```powershell
$myUpdate | New-CMSoftwareUpdateAutoPhasedDeployment -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

## PARAMETERS

### -AddPhases
{{ Fill AddPhases Description }}

```yaml
Type: Phase[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

Specify a description for the software update phased deployment.

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

Specify a collection object for the first phase.

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

Specify a collection ID for the first phase.

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

Specify a collection name for the first phase.

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

### -InsertAtOrder
{{ Fill InsertAtOrder Description }}

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

Specify a name for the application phased deployment.

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

Specify a collection object for the second phase.

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

Specify a collection ID for the second phase.

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

Specify a collection name for the second phase.

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

### -SoftwareUpdateGroup

Specify an object for the software update group.

```yaml
Type: IResultObject
Parameter Sets: SearchByGroupMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId

Specify the software update group by ID.

```yaml
Type: String
Parameter Sets: SearchByGroupIdMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName

Specify the software update group by name.

```yaml
Type: String
Parameter Sets: SearchByGroupNameMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateIds

Specify an array of software update IDs.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateNames

Specify an array of software update names.

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdates

Specify an array of software update objects.

```yaml
Type: IResultObject[]
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
