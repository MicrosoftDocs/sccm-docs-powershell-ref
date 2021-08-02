---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Remove-CMSoftwareUpdatePhasedDeployment

## SYNOPSIS

Use this cmdlet to remove a phased deployment for software updates.

## SYNTAX

### SearchBySoftwareUpdate
```
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdate <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroup
```
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroup <IResultObject> [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroupId
```
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupId <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateGroupName
```
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupName <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateId
```
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateId <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySoftwareUpdateName
```
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName <String> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValue
```
Remove-CMSoftwareUpdatePhasedDeployment [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Remove-CMSoftwareUpdatePhasedDeployment [-Force] -Id <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Remove-CMSoftwareUpdatePhasedDeployment [-Force] -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2002, use this cmdlet to remove a phased deployment for software updates.

## EXAMPLES

### Example 1: Remove a phased deployment on an update

This example removes the phased deployment from the specified software update.

```powershell
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateName "mySoftwareUpdateName"
```

### Example 2: Remove a phased deployment on an update group

This example removes the phased deployment from the specified software update group.

```powershell
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdateGroupName "mySoftwareUpdateGroupName"
```

### Example 3: Remove a phased deployment by name

This example removes the phased deployment by its name.

```powershell
Remove-CMSoftwareUpdatePhasedDeployment -Name "myPhasedDeploymentName"
```

### Example 4: Force remove a phased deployment from input

This example force removes a piped object phased deployment.

```powershell
$myPhasedDeployment | Remove-CMSoftwareUpdatePhasedDeployment -Force
```

## PARAMETERS

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

### -Force

Force remove the phased deployment.

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

### -Id

Specify the ID of the phased deployment to remove. The value is a GUID format.

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

### -InputObject

Specify an object for the phased deployment to remove.

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: PhasedDeployment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the phased deployment to remove.

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

Remove a phased deployment from the specified software update object.

```yaml
Type: IResultObject
Parameter Sets: SearchBySoftwareUpdate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroup

Remove a phased deployment from the specified software update group object.

```yaml
Type: IResultObject
Parameter Sets: SearchBySoftwareUpdateGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId

Specify the ID of the software update group.

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

Specify the name of the software update group.

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

Specify the ID of the software update.

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

Specify the name of the software update.

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
