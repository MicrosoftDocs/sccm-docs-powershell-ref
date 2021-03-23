---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/30/2020
online version:
schema: 2.0.0
---

# Get-CMPhase

## SYNOPSIS

Use this cmdlet to get a deployment phase for a specific instance or a phased deployment.

## SYNTAX

### SearchByPhasedDeployment
```
Get-CMPhase [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-Id <String>]
 [-InputObject] <IResultObject> [-Name <String>] [-Order <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPhasedDeploymentId
```
Get-CMPhase [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-Id <String>]
 [-Name <String>] [-Order <Int32>] [-PhasedDeploymentId] <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPhasedDeploymentName
```
Get-CMPhase [-Collection <IResultObject>] [-CollectionId <String>] [-CollectionName <String>] [-Id <String>]
 [-Name <String>] [-Order <Int32>] [-PhasedDeploymentName] <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to get a deployment phase for a specific instance or a phased deployment.

## EXAMPLES

### Example 1: Get phase by ID

This example gets the phase by its ID.

```powershell
Get-CMPhase -Id "66DEDF86-D0CB-457D-88BE-47E3FAC92A47"
```

## PARAMETERS

### -Collection

Specify a collection object for the phase.

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

Specify a collection by ID for the phase.

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

Specify a collection by name for the phase.

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

Specify the ID of the phase.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PhaseId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify the phased deployment object for the phase.

```yaml
Type: IResultObject
Parameter Sets: SearchByPhasedDeployment
Aliases: PhasedDeployment

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the phased deployment.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PhaseName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Order

Specify an integer value for the phase's order.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: PhaseOrder

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PhasedDeploymentId

Specify the ID of the phased deployment.

```yaml
Type: String
Parameter Sets: SearchByPhasedDeploymentId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PhasedDeploymentName

Specify the name of the phased deployment.

```yaml
Type: String
Parameter Sets: SearchByPhasedDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### Microsoft.ConfigurationManager.PhasedDeploymentModel.Phase

## NOTES

## RELATED LINKS

[Create phased deployments](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence)
