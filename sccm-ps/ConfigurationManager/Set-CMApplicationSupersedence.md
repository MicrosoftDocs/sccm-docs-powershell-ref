---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
online version:
schema: 2.0.0
---

# Set-CMApplicationSupersedence

## SYNOPSIS

Set deployment type supersedence for an application.

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

Use this cmdlet to set deployment type supersedence for the specified application.

For more information, see [Supersede applications](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add deployment type supersedence

```powershell
$AppSupersededName = "Superseded app"
$AppSuperseded = New-CMApplication -Name $AppSupersededName
$OriginalDT = Add-CMScriptDeploymentType -ApplicationName $AppSuperseded -DeploymentTypeName "ScriptDT01" -InstallCommand 'appsetup.exe'

$AppSupersedingName = "Superseding app"
$AppSuperseding = New-CMApplication -Name $AppSupersedingName
$AppSupersedingDT = Add-CMScriptDeploymentType -ApplicationName $AppSuperseding -DeploymentTypeName "ScriptDT02" -InstallCommand 'appsetup2.exe'

Set-CMApplicationSupersedence -ApplicationId ($AppSuperseding.CI_ID) -CurrentDeploymentTypeId ($AppSupersedingDT.CI_ID) -SupersededApplicationId ($AppSuperseded.CI_ID) -OldDeploymentTypeId ($OriginalDT.CI_ID)
```

### Example 2: Remove deployment type supersedence

```powershell
Set-CMApplicationSupersedence -ApplicationName $AppSupersedingName -CurrentDeploymentTypeName ($AppSupersedingDT.LocalizedDisplayName) -SupersededApplicationName $AppSupersededName -OldDeploymentTypeName ($OriginalDT.LocalizedDisplayName) -RemoveSupersedence -Force
```

## PARAMETERS

### -CurrentDeploymentType

Specify a deployment type object from the _superseding_ application. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

Specify the ID of a deployment type from the _superseding_ application.

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

Specify the name of a deployment type from the _superseding_ application.

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

Add this parameter to run the command without asking for confirmation.

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

Specify the ID of the current (_superseding_) application.

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

Specify an object for the current (_superseding_) application. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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

Set this parameter to `$true` to uninstall the superseded application before the client installs the superseding application.

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

Specify the localized display name of the current (_superseding_) application.

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

Specify a deployment type object from the _superseded_ application. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

Specify the ID of a deployment type from the _superseded_ application.

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

Specify the name of a deployment type from the _superseded_ application.

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

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

Add this parameter to remove the supersedence relationship.

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

Specify an object for the old (_superseded_) application. To get this object, use the [Get-CMApplication](Get-CMApplication.md) cmdlet.

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

Specify the ID of the old (_superseded_) application.

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

Specify the localized display name of the old (_superseded_) application.

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

[Get-CMApplication](Get-CMApplication.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Supersede applications](/mem/configmgr/apps/deploy-use/revise-and-supersede-applications#supersedence)
