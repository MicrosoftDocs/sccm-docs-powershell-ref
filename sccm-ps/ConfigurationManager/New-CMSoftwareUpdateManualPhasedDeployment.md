---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMSoftwareUpdateManualPhasedDeployment

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByValueMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdates] <IResultObject[]> -AddPhases <Phase[]>
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateIds] <String[]> -AddPhases <Phase[]> -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SearchByNameMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateNames] <String[]> -AddPhases <Phase[]>
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByGroupMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateGroup] <IResultObject> -AddPhases <Phase[]>
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByGroupIdMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateGroupId] <String> -AddPhases <Phase[]>
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByGroupNameMandatory
```
New-CMSoftwareUpdateManualPhasedDeployment [-SoftwareUpdateGroupName] <String> -AddPhases <Phase[]>
 -Name <String> [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
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

### -AddPhases
{{ Fill AddPhases Description }}

```yaml
Type: Phase[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
{{ Fill Description Description }}

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

### -Name
{{ Fill Name Description }}

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

### -SoftwareUpdateGroup
{{ Fill SoftwareUpdateGroup Description }}

```yaml
Type: IResultObject
Parameter Sets: SearchByGroupMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateGroupId
{{ Fill SoftwareUpdateGroupId Description }}

```yaml
Type: String
Parameter Sets: SearchByGroupIdMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateGroupName
{{ Fill SoftwareUpdateGroupName Description }}

```yaml
Type: String
Parameter Sets: SearchByGroupNameMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateIds
{{ Fill SoftwareUpdateIds Description }}

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateNames
{{ Fill SoftwareUpdateNames Description }}

```yaml
Type: String[]
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdates
{{ Fill SoftwareUpdates Description }}

```yaml
Type: IResultObject[]
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
