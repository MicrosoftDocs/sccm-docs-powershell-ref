---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-CMSoftwareUpdateDeployment

## SYNOPSIS
Gets a software update deployment

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateDeployment [-Name <String>] [-Summary] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMSoftwareUpdateDeployment [-SmsObjectId <Int32>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMSoftwareUpdateDeployment [-DeploymentId <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMSoftwareUpdateDeployment [-InputObject <IResultObject>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -Collection
{{Fill Collection Description}}

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
{{Fill CollectionId Description}}

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
{{Fill CollectionName Description}}

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

### -DeploymentId
{{Fill DeploymentId Description}}

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentUniqueID, SoftwareUpdateDeploymentID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -InputObject
{{Fill InputObject Description}}

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: SoftwareUpdate

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
{{Fill Name Description}}

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: SoftwareUpdateName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SmsObjectId
{{Fill SmsObjectId Description}}

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, SoftwareUpdateID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Summary
{{Fill Summary Description}}

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject[]#SMS_DeploymentSummary
IResultObject#SMS_DeploymentSummary
IResultObject[]#SMS_UpdateAssignment
IResultObject#SMS_UpdateAssignment

## NOTES

## RELATED LINKS

