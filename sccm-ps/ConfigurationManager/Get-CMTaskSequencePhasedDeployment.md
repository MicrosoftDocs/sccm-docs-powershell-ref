---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMTaskSequencePhasedDeployment

## SYNOPSIS

Use this cmdlet to get the phased deployment for a task sequence.

## SYNTAX

### SearchByTaskSequence
```
Get-CMTaskSequencePhasedDeployment -TaskSequence <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByTaskSequenceId
```
Get-CMTaskSequencePhasedDeployment -TaskSequenceId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByTaskSequenceName
```
Get-CMTaskSequencePhasedDeployment -TaskSequenceName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMTaskSequencePhasedDeployment -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMTaskSequencePhasedDeployment -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to get the phased deployment for a task sequence.

## EXAMPLES

### Example 1: Get the deployment by name

This example gets a task sequence phased deployment by the name of the phased deployment.

```powershell
Get-CMTaskSequencePhasedDeployment -Name "myPhasedDeploymentName"
```

### Example 2: Get the deployment by task sequence name

This example gets a task sequence phased deployment by the name of the task sequence.

```powershell
Get-CMTaskSequencePhasedDeployment -TaskSequenceName "myTaskSequenceName"
```

## PARAMETERS

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

### -Id

Specify the ID of the phased deployment.

```yaml
Type: String
Parameter Sets: SearchById
Aliases: PhasedDeploymentId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the phased deployment.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequence

Specify a task sequence object.

```yaml
Type: IResultObject
Parameter Sets: SearchByTaskSequence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -TaskSequenceId

Specify the ID for a task sequence.

```yaml
Type: String
Parameter Sets: SearchByTaskSequenceId
Aliases: TaskSequencePackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TaskSequenceName

Specify the name for a task sequence.

```yaml
Type: String
Parameter Sets: SearchByTaskSequenceName
Aliases:

Required: True
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

### IResultObject[]#SMS_PhasedDeployment

## NOTES

## RELATED LINKS
