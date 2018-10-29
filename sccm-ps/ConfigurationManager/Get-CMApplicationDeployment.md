---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-CMApplicationDeployment

## SYNOPSIS
Gets an application deployment

## SYNTAX

### SearchByName (Default)
```
Get-CMApplicationDeployment [-Name <String>] [-Summary] [-CollectionName <String>] [-CollectionId <String>]
 [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMApplicationDeployment [-SmsObjectId <Int32>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMApplicationDeployment [-DeploymentId <String>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByValue
```
Get-CMApplicationDeployment [-InputObject <IResultObject>] [-Summary] [-CollectionName <String>]
 [-CollectionId <String>] [-Collection <IResultObject>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
```

 

## PARAMETERS

### -Collection
 

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
 

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: AssignmentUniqueID, ApplicationDeploymentID

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
 

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Application

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
 

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ApplicationName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SmsObjectId
 

```yaml
Type: Int32
Parameter Sets: SearchById
Aliases: CI_ID, ApplicationID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Summary
 

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
IResultObject[]#SMS_ApplicationAssignment
IResultObject#SMS_ApplicationAssignment

## NOTES

## RELATED LINKS

