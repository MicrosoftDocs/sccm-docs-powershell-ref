---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834304
schema: 2.0.0
ms.assetid: B8879874-7A8B-4D59-8CA3-B3DC69602546
---

# Get-CMDeployment

## SYNOPSIS
Gets a Configuration Manager deployment.

## SYNTAX

### SearchByName (Default)
```
Get-CMDeployment [-CollectionName <String>] [-FeatureType <DeploymentFeature>] [-ProgramName <String>]
 [-SoftwareName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMDeployment -DeploymentId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
**The Get-CMDeployment** cmdlet gets one or more Microsoft System Center Configuration Manager deployments.
The cmdlet gets summary information about application, Software Update Management (SUM), or classic program deployments.

## EXAMPLES

### Example 1: Get a deployment for a collection
```
PS C:\>Get-CMDeployment -CollectionName "deviceCol1" -FeatureType "Application"
```

This command gets the Application deployment for the device collection named deviceCol1.

## PARAMETERS

### -CollectionName
Specifies the name of the collection associated with the deployment.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentId
Specifies the ID of a deployment.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 
Required: True
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

### -FeatureType
Specifies the feature type of the deployment.
Valid values are:

- Application
- Package
- SoftwareUpdate
- ConfigurationItem
- TaskSequence
- FirewallSetting

```yaml
Type: DeploymentFeature
Parameter Sets: SearchByName
Aliases: 
Accepted values: Application, Package, SoftwareUpdate, ConfigurationItem, TaskSequence, FirewallSetting
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

### -ProgramName
Specifies the name of the program associated with the deployment.
Use this parameter with a legacy distribution program.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SoftwareName
Specifies the name of the software associated with the deployment.
Use this parameter with a software update.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDeploymentStatus](./Get-CMDeploymentStatus.md)

[Get-CMDeploymentType](./Get-CMDeploymentType.md)

[Remove-CMDeployment](./Remove-CMDeployment.md)

[Set-CMDeploymentType](./Set-CMDeploymentType.md)


