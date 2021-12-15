---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Set-CMApplicationSupersedence

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SetById
```
Set-CMApplicationSupersedence [-Id] <Int32> [-CurrentDeploymentTypeId <Int32>]
 [-CurrentDeploymentTypeName <String>] [-CurrentDeploymentType <IResultObject>]
 [-SupersededApplicationId <Int32>] [-SupersededApplicationName <String>]
 [-SupersededApplication <IResultObject>] [-OldDeploymentTypeId <Int32>] [-OldDeploymentTypeName <String>]
 [-OldDeploymentType <IResultObject>] [-IsUninstall <Boolean>] [-RemoveSupersedence] [-Force] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMApplicationSupersedence [-Name] <String> [-CurrentDeploymentTypeId <Int32>]
 [-CurrentDeploymentTypeName <String>] [-CurrentDeploymentType <IResultObject>]
 [-SupersededApplicationId <Int32>] [-SupersededApplicationName <String>]
 [-SupersededApplication <IResultObject>] [-OldDeploymentTypeId <Int32>] [-OldDeploymentTypeName <String>]
 [-OldDeploymentType <IResultObject>] [-IsUninstall <Boolean>] [-RemoveSupersedence] [-Force] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValue
```
Set-CMApplicationSupersedence [-InputObject] <IResultObject> [-CurrentDeploymentTypeId <Int32>]
 [-CurrentDeploymentTypeName <String>] [-CurrentDeploymentType <IResultObject>]
 [-SupersededApplicationId <Int32>] [-SupersededApplicationName <String>]
 [-SupersededApplication <IResultObject>] [-OldDeploymentTypeId <Int32>] [-OldDeploymentTypeName <String>]
 [-OldDeploymentType <IResultObject>] [-IsUninstall <Boolean>] [-RemoveSupersedence] [-Force] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
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

### -CurrentDeploymentType
{{ Fill CurrentDeploymentType Description }}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: ReplacementDeploymentType, SupersedingDeploymentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CurrentDeploymentTypeId
{{ Fill CurrentDeploymentTypeId Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CurrentDeploymentTypeCIId, CurrentDeploymentTypeCI_ID, ReplacementDeploymentTypeId, ReplacementDeploymentTypeCIId, ReplacementDeploymentTypeCI_ID, SupersedingDeploymentTypeId, SupersedingDeploymentTypeCIId, SupersedingDeploymentTypeCI_ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CurrentDeploymentTypeName
{{ Fill CurrentDeploymentTypeName Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReplacementDeploymentTypeName, SupersedingDeploymentTypeName

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
Type: Int32
Parameter Sets: SetById
Aliases: ApplicationId, CurrentApplicationId, CurrentApplicationCIId, CurrentApplicationCI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: Application, CurrentApplication

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsUninstall
{{ Fill IsUninstall Description }}

```yaml
Type: Boolean
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
Parameter Sets: SetByName
Aliases: ApplicationName, LocalizedDisplayName, CurrentApplicationName, CurrentApplicationLocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OldDeploymentType
{{ Fill OldDeploymentType Description }}

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: SupersededDeploymentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OldDeploymentTypeId
{{ Fill OldDeploymentTypeId Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: OldDeploymentTypeCIId, OldDeploymentTypeCI_ID, SupersededDeploymentTypeId, SupersededDeploymentTypeCIId, SupersededDeploymentTypeCI_ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OldDeploymentTypeName
{{ Fill OldDeploymentTypeName Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: SupersededDeploymentTypeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
{{ Fill PassThru Description }}

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

### -RemoveSupersedence
{{ Fill RemoveSupersedence Description }}

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

### -SupersededApplication
{{ Fill SupersededApplication Description }}

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

### -SupersededApplicationId
{{ Fill SupersededApplicationId Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: SupersededApplicationCIId, SupersededApplicationCI_ID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SupersededApplicationName
{{ Fill SupersededApplicationName Description }}

```yaml
Type: String
Parameter Sets: (All)
Aliases: SupersededApplicationLocalizedDisplayName

Required: False
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
