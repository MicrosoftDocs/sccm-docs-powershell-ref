---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Remove-CMSoftwareUpdatePhasedDeployment

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

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

### SearchBySoftwareUpdate
```
Remove-CMSoftwareUpdatePhasedDeployment -SoftwareUpdate <IResultObject> [-Force] [-DisableWildcardHandling]
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
Remove-CMSoftwareUpdatePhasedDeployment -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
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
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill Force Description }}

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
{{ Fill ForceWildcardHandling Description }}

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
{{ Fill Id Description }}

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
{{ Fill InputObject Description }}

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
{{ Fill Name Description }}

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
{{ Fill SoftwareUpdate Description }}

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
{{ Fill SoftwareUpdateGroup Description }}

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
{{ Fill SoftwareUpdateGroupId Description }}

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
{{ Fill SoftwareUpdateGroupName Description }}

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
{{ Fill SoftwareUpdateId Description }}

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
{{ Fill SoftwareUpdateName Description }}

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
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
