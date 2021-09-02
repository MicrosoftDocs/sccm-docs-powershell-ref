---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMApplicationAutoPhasedDeployment

## SYNOPSIS

Use this cmdlet to create a phased deployment for an application by generating two phases with same settings.

## SYNTAX

### SearchByValueMandatory
```
New-CMApplicationAutoPhasedDeployment [-Application] <IResultObject> [-BeginCondition <BeginConditionType>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>] [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-InstallationChoice <InstallationChoiceType>]
 [-SecondCollection <IResultObject>] [-SecondCollectionId <String>] [-SecondCollectionName <String>]
 [-ThrottlingDays <Int32>] [-Description <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMApplicationAutoPhasedDeployment [-ApplicationId] <String> [-BeginCondition <BeginConditionType>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>] [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-InstallationChoice <InstallationChoiceType>]
 [-SecondCollection <IResultObject>] [-SecondCollectionId <String>] [-SecondCollectionName <String>]
 [-ThrottlingDays <Int32>] [-Description <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMApplicationAutoPhasedDeployment [-ApplicationName] <String> [-BeginCondition <BeginConditionType>]
 [-CriteriaOption <CriteriaType>] [-CriteriaValue <Int32>] [-DaysAfterPreviousPhaseSuccess <Int32>]
 [-DeadlineUnit <TimeUnitType>] [-DeadlineValue <Int32>] [-FirstCollection <IResultObject>]
 [-FirstCollectionId <String>] [-FirstCollectionName <String>] [-InstallationChoice <InstallationChoiceType>]
 [-SecondCollection <IResultObject>] [-SecondCollectionId <String>] [-SecondCollectionName <String>]
 [-ThrottlingDays <Int32>] [-Description <String>] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to create a phased deployment for an application by generating two phases with same settings. This cmdlet's behavior is the same as the **Create Phased Deployment** wizard on an application, when you select the option to **Automatically create a default two phase deployment**.

> [!NOTE]
> Before you create a phased deployment, make sure to distribute the application's content to a distribution point.

## EXAMPLES

### Example 1: Create a deployment by app name

This example creates a new application phased deployment named **myDPName** for the application **myApp**.

```powershell
New-CMApplicationAutoPhasedDeployment -ApplicationName "myApp" -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

### Example 2: Create a deployment by input app object

This example creates a new application phased deployment named **myPDName** for a piped application object.

```powershell
$myApp | New-CMApplicationAutoPhasedDeployment -Name "myPDName" -FirstCollectionID "SMSDM001" -SecondCollectionID "SMSDM003" -CriteriaOption Compliance -CriteriaValue 1 -BeginCondition AfterPeriod -DaysAfterPreviousPhaseSuccess 2 -ThrottlingDays 3 -InstallationChoice AfterPeriod -DeadlineUnit Hours -DeadlineValue 4 -Description "MyDescription"
```

## PARAMETERS

### -Application

Specify an application object for the phased deployment.

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

Specify an application ID for the phased deployment.

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

Specify an application name for the phased deployment.

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

Specify an option for beginning the second phase of deployment after success of the first phase:

- `AfterPeriod`: This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Automatically begin this phase after a deferral period (in days)**. If you specify this value, use **DaysAfterPreviousPhaseSuccess** to configure the period of time.

- `Manually`: This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Manually begin the second phase deployment**.

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

Specify an option to choose the criteria for success of the first phase:

- `Compliance`: This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Deployment success percentage**. Specify the percentage value with the **CriteriaValue** parameter.

- `Number`: This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Number of devices successfully deployed**. Specify the number of devices with the **CriteriaValue** parameter.

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

This integer value depends upon the value that you specify for **CriteriaOption**:

- `Compliance`: Specify the percentage

- `Number`: Specify the number of devices

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

Specify an integer value for the number of days after success of the first phase to begin the second phase. This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Automatically begin this phase after a deferral period (in days)**.

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

Specify the type of deadline period. Use this parameter with **DeadlineValue**.

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

This parameter is only used if you specify `AfterPeriod` with the **InstallationChoice** parameter.

Specify an integer value for the period of time for the deadline. Use the **DeadlineUnit** parameter to specify the type of period: `Hours`, `Days`, `Weeks`, `Months`. This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Installation is required after this period of time**.

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

Specify a description for the application phased deployment.

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify an option for the behavior relative to when the software is made available:

- `AsSoonAsPossible`: This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Installation is required as soon as possible**.

- `AfterPeriod`: This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Installation is required after this period of time**. If you specify this value, use **DeadlineUnit** and **DeadlineValue** to configure the period of time.

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

### -ThrottlingDays

Specify an integer value for the number of days to gradually make this software available. This parameter is the same as the following setting on the **Settings** page of the **Create Phased Deployment** wizard in the console: **Gradually make this software available over this period of time (in days)**.

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

### IResultObject#SMS_PhasedDeployment
## NOTES

## RELATED LINKS
