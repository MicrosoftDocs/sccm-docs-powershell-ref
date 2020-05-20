---
external help file: AdminUI.PS.Deployments.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMSoftwareUpdatePhasedDeployment

## SYNOPSIS
{{ Fill in the Synopsis }}

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
Accept pipeline input: True (ByValue)
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
Accept pipeline input: True (ByValue)
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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_PhasedDeployment

### IResultObject[]#SMS_PhasedDeployment

## NOTES

## RELATED LINKS
