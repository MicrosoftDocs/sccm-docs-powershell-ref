---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834136
schema: 2.0.0
ms.assetid: 273ECCC5-EF89-4EBA-9714-6142159799A9
---

# Set-CMUpdateGroupDeployment

## SYNOPSIS

## SYNTAX

### ByValueEnable (Default)
```
Set-CMUpdateGroupDeployment [-Enable] -UpdateGroupDeployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameDisable
```
Set-CMUpdateGroupDeployment [-Disable] [-UpdateGroupDeploymentName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByValueDisable
```
Set-CMUpdateGroupDeployment [-Disable] -UpdateGroupDeployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeploymentSummaryValueDisable
```
Set-CMUpdateGroupDeployment [-Disable] -Deployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdDisable
```
Set-CMUpdateGroupDeployment [-Disable] -UpdateGroupDeploymentId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameEnable
```
Set-CMUpdateGroupDeployment [-Enable] [-UpdateGroupDeploymentName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByIdEnable
```
Set-CMUpdateGroupDeployment [-Enable] -UpdateGroupDeploymentId <Int32> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDeploymentSummaryValueEnable
```
Set-CMUpdateGroupDeployment [-Enable] -Deployment <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

## EXAMPLES

### 1:
```
PS C:\>
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Deployment
```yaml
Type: IResultObject
Parameter Sets: ByDeploymentSummaryValueDisable, ByDeploymentSummaryValueEnable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Disable
```yaml
Type: SwitchParameter
Parameter Sets: ByNameDisable, ByValueDisable, ByDeploymentSummaryValueDisable, ByIdDisable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
Indicates that wildcard handling is disabled.

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

### -Enable
```yaml
Type: SwitchParameter
Parameter Sets: ByValueEnable, ByNameEnable, ByIdEnable, ByDeploymentSummaryValueEnable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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

### -UpdateGroupDeployment
```yaml
Type: IResultObject
Parameter Sets: ByValueEnable, ByValueDisable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -UpdateGroupDeploymentId
```yaml
Type: Int32
Parameter Sets: ByIdDisable, ByIdEnable
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UpdateGroupDeploymentName
```yaml
Type: String
Parameter Sets: ByNameDisable, ByNameEnable
Aliases: Name

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS


