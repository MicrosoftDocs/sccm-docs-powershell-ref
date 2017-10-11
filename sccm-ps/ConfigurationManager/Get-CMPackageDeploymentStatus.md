---
external help file: AdminUI.PS.Deployments.dll-Help.xml
online version: 
schema: 2.0.0
---

# Get-CMPackageDeploymentStatus

## SYNOPSIS
Gets the status of classic software distribution deployments.

## SYNTAX

### SearchByName (Default)
```
Get-CMPackageDeploymentStatus [-Name <String>] [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByDeploymentId
```
Get-CMPackageDeploymentStatus -DeploymentId <String> [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPackageId
```
Get-CMPackageDeploymentStatus -PackageId <String> [-StatusType <PackageDeploymentStatusType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByValue
```
Get-CMPackageDeploymentStatus [-StatusType <PackageDeploymentStatusType>] -InputObject <IResultObject>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMPackageDeploymentStatus** cmdlet gets the status of one or more classic software distribution deployments.
A classic software distribution is a legacy software distribution program on a client.

## EXAMPLES

### Example 1
```
PS C:\> Get-CMPackageDeploymentStatus -Name "Depack01"
```

This command gets the status of a deployment that is distributed to Configuration Manager clients by using the deployment package named Depack01.

## PARAMETERS

### -DeploymentId
 

```yaml
Type: String
Parameter Sets: SearchByDeploymentId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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

### -InputObject
 

```yaml
Type: IResultObject
Parameter Sets: SearchByValue
Aliases: Package, Advertisement, Deployment

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
 

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: PackageName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PackageId
 

```yaml
Type: String
Parameter Sets: SearchByPackageId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StatusType
 

```yaml
Type: PackageDeploymentStatusType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Success, InProgress, RequirementsNotMet, Unknown, Error

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Get-CMDeploymentPackage](Get-CMDeploymentPackage.md)

[Invoke-CMDeploymentSummarization](Invoke-CMDeploymentSummarization.md)

[Remove-CMDeployment](Remove-CMDeployment.md)
