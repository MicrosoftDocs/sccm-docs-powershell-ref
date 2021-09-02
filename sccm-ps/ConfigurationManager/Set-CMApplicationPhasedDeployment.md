---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
online version:
schema: 2.0.0
---

# Set-CMApplicationPhasedDeployment

## SYNOPSIS

Configure a phased deployment for an application.

## SYNTAX

### SearchByValue
```
Set-CMApplicationPhasedDeployment [-Description <String>] -InputObject <IResultObject> [-NewName <String>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchById
```
Set-CMApplicationPhasedDeployment [-Description <String>] [-NewName <String>] [-PassThru] -Id <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Set-CMApplicationPhasedDeployment [-Description <String>] [-NewName <String>] [-PassThru] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Applies to version 2006 and later. Configure a phased deployment for an application. For more information, see [Create phased deployments](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence).

## EXAMPLES

### Example 1: Rename a phased deployment

This example renames an application phased deployment that's passed through on the command line.

```powershell
$appPhasedDeployment = Get-CMApplicationPhasedDeployment -Name "myPhasedDeploymentName"

$appPhasedDeployment | Set-CMApplicationPhasedDeployment -NewName "New app phased deployment" -PassThru
```

### Example 2: Change the description

This example changes the description for an application phased deployment targeted by its ID.

```powershell
Set-CMApplicationPhasedDeployment -Id "3b107e52-471b-4c9c-a034-928bcc5f6fc0" -Description "This is an app phased deployment description"
```

## PARAMETERS

### -Description

Specify an optional description to better identify this application phased deployment.

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

Specify the ID of the application phased deployment to configure. The format of this value is a GUID.

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

Specify an object for an application phased deployment to configure. For example, use the [Get-CMApplicationPhasedDeployment](Get-CMApplicationPhasedDeployment.md) cmdlet to get this object.

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

Specify the name of the application phased deployment to configure.

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

### -NewName

Use this parameter to rename the application phased deployment.

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

### -PassThru

Returns an object representing the item with which you're working. By default, this cmdlet may not generate any output.

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

### IResultObject#SMS_PhasedDeployment
## NOTES

## RELATED LINKS

[Get-CMApplicationPhasedDeployment](Get-CMApplicationPhasedDeployment.md)

[New-CMApplicationAutoPhasedDeployment](New-CMApplicationAutoPhasedDeployment.md)

[Remove-CMApplicationPhasedDeployment](Remove-CMApplicationPhasedDeployment.md)

[Get-CMPhase](Get-CMPhase.md)

[Get-CMPhasedDeploymentStatus](Get-CMPhasedDeploymentStatus.md)

[Move-CMPhasedDeploymentToNext](Move-CMPhasedDeploymentToNext.md)

[Resume-CMPhasedDeployment](Resume-CMPhasedDeployment.md)

[Suspend-CMPhasedDeployment](Suspend-CMPhasedDeployment.md)

[Create phased deployments](/mem/configmgr/osd/deploy-use/create-phased-deployment-for-task-sequence)
