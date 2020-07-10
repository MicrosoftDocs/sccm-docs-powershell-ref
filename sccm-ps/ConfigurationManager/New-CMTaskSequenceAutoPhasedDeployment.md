---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMTaskSequenceAutoPhasedDeployment

## SYNOPSIS

Use this cmdlet to create a phased deployment for a task sequence by generating two phases with same settings.

## SYNTAX

### SearchByValueMandatory
```
New-CMTaskSequenceAutoPhasedDeployment [-TaskSequence] <IResultObject> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMTaskSequenceAutoPhasedDeployment [-TaskSequenceId] <String> [-FirstCollection <IResultObject>]
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
New-CMTaskSequenceAutoPhasedDeployment [-TaskSequenceName] <String> [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-SecondCollection <IResultObject>]
 [-SecondCollectionId <String>] [-SecondCollectionName <String>] [-CriteriaOption <CriteriaType>]
 [-CriteriaValue <Int32>] [-BeginCondition <BeginConditionType>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-ThrottlingDays <Int32>] [-InstallationChoice <InstallationChoiceType>] [-DeadlineUnit <TimeUnitType>]
 [-DeadlineValue <Int32>] [-AddPhases <Phase[]>] [-InsertAtOrder <Int32>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to create a phased deployment for a task sequence by generating two phases with same settings.

## EXAMPLES

### Example 1: Create a deployment by task sequence name

This example creates a new task sequence phased deployment named **myDPName** for the task sequence **myTaskSequenceName**.

```powershell
New-CMTaskSequenceAutoPhasedDeployment -TaskSequenceName "myTaskSequenceName" -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

### Example 2: Create a deployment by input task sequence object

This example creates a new task sequence phased deployment named **myPDName** for a piped task sequence object.

```powershell
$myTS | New-CMTaskSequenceAutoPhasedDeployment -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
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

Specify a description for the task sequence phased deployment.

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

Specify a name for the task sequence phased deployment.

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

### -TaskSequence

Specify a task sequence object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskSequenceId

Specify a task sequence by ID.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: TaskSequencePackageId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify a task sequence by name.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: 0
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS
