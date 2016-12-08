---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834195
schema: 2.0.0
ms.assetid: 10131437-15F6-4126-9E65-82CC58D5503D
---

# Start-CMApplicationDeploymentSimulation

## SYNOPSIS
Starts an application deployment simulation in Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMApplicationDeploymentSimulation -InputObject <IResultObject> -CollectionName <String>
 [-DeploymentAction <DeployActionType>] [-PreDeploy <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Start-CMApplicationDeploymentSimulation -Name <String> -CollectionName <String>
 [-DeploymentAction <DeployActionType>] [-PreDeploy <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Start-CMApplicationDeploymentSimulation -Id <Int32> -CollectionName <String>
 [-DeploymentAction <DeployActionType>] [-PreDeploy <Boolean>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMApplicationDeploymentSimulation** cmdlet starts an application deployment.
Use simulated deployment to test an application deployment without installing an application.

## EXAMPLES

### Example 1: Start an application deployment simulation
```
PS C:\> Start-CMApplicationDeploymentSimulation -CollectionName "All Mobile Devices" -Name "WIN8_UPDATE2" -DeployAction Install
```

This command starts a deployment simulation of the installation of the application named WIN8_UPDATE2 for the target collection named All Mobile Devices.

## PARAMETERS

### -CollectionName
Specifies a name for the target collection.

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

### -DeploymentAction


```yaml
Type: DeployActionType
Parameter Sets: (All)
Aliases: DeployAction
Accepted values: Install, Uninstall
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

### -Id
Specifies an array of IDs.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an application deployment object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PreDeploy
Indicates whether to copy software to a device before installation.

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

[Set-CMApplicationDeployment](./Set-CMApplicationDeployment.md)

[Start-CMApplicationDeployment](./Start-CMApplicationDeployment.md)
