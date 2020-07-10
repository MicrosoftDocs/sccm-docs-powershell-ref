---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMSoftwareUpdatePhasedDeployment

## SYNOPSIS

Use this cmdlet to get the phased deployment for software updates.

## SYNTAX

### SearchBySoftwareUpdateGroup
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroup <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroupId
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroupName
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdate
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdate <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateId
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateId <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchBySoftwareUpdateName
```
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchById
```
Get-CMSoftwareUpdatePhasedDeployment -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByName
```
Get-CMSoftwareUpdatePhasedDeployment -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to get the phased deployment for software updates.

## EXAMPLES

### Example 1: Get deployment by name

This example gets the software update phased deployment by its name.

```powershell
Get-CMSoftwareUpdatePhasedDeployment -Name "myPhasedDeploymentName"
```

### Example 2: Get deployment by software update name

This example gets the software update phased deployment by the name of the software update.

```powershell
Get-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName "myUpdateName"
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

### -SoftwareUpdate

Specify a software update object.

```yaml
Type: IResultObject
Parameter Sets: SearchBySoftwareUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroup

Specify a software update group object.

```yaml
Type: IResultObject
Parameter Sets: SearchBySoftwareUpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId

Specify the ID of a software update group.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateGroupId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName

Specify the name of a software update group.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateId

Specify the ID of a software update.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName

Specify the name of a software update.

```yaml
Type: String
Parameter Sets: SearchBySoftwareUpdateName
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
