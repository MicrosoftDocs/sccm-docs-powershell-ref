---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Remove-CMSoftwareUpdateFromPackage

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### ById_Id (Default)
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateId <String[]> -SoftwareUpdatePackageId <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObject_Id
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdate <IResultObject[]> -SoftwareUpdatePackageId <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObject_Name
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdate <IResultObject[]> -SoftwareUpdatePackageName <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByObject_Object
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdate <IResultObject[]> -SoftwareUpdatePackage <IResultObject>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById_Name
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateId <String[]> -SoftwareUpdatePackageName <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ById_Object
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateId <String[]> -SoftwareUpdatePackage <IResultObject>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName_Id
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateName <String[]> -SoftwareUpdatePackageId <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName_Name
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateName <String[]> -SoftwareUpdatePackageName <String>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByName_Object
```
Remove-CMSoftwareUpdateFromPackage -SoftwareUpdateName <String[]> -SoftwareUpdatePackage <IResultObject>
 [-RefreshDistributionPoint] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
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

### -RefreshDistributionPoint
{{ Fill RefreshDistributionPoint Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RefreshDistributionPointAfterRemoveSoftwareUpdateFromPackage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdate
{{ Fill SoftwareUpdate Description }}

```yaml
Type: IResultObject[]
Parameter Sets: ByObject_Id, ByObject_Name, ByObject_Object
Aliases: SoftwareUpdates

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdateId
{{ Fill SoftwareUpdateId Description }}

```yaml
Type: String[]
Parameter Sets: ById_Id, ById_Name, ById_Object
Aliases: SoftwareUpdateIds

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdateName
{{ Fill SoftwareUpdateName Description }}

```yaml
Type: String[]
Parameter Sets: ByName_Id, ByName_Name, ByName_Object
Aliases: SoftwareUpdateNames

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -SoftwareUpdatePackage
{{ Fill SoftwareUpdatePackage Description }}

```yaml
Type: IResultObject
Parameter Sets: ByObject_Object, ById_Object, ByName_Object
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SoftwareUpdatePackageId
{{ Fill SoftwareUpdatePackageId Description }}

```yaml
Type: String
Parameter Sets: ById_Id, ByObject_Id, ByName_Id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareUpdatePackageName
{{ Fill SoftwareUpdatePackageName Description }}

```yaml
Type: String
Parameter Sets: ByObject_Name, ById_Name, ByName_Name
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
