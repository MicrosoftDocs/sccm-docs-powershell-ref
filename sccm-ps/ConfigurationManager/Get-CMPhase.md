---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/30/2021
online version:
schema: 2.0.0
---

# Get-CMPhase

## SYNOPSIS

Get a deployment phase for a specific instance of a phased deployment.

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

Use this cmdlet to get a deployment phase for a specific instance of a phased deployment.

For more information, see [Create phased deployments with Configuration Manager](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get phase by ID

This example gets the phase by its ID.

```powershell
Get-CMPhase -Id "66DEDF86-D0CB-457D-88BE-47E3FAC92A47"
```

## PARAMETERS

### -Collection

Specify a collection object for the phase. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

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

### -ForceWildcardHandling

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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
