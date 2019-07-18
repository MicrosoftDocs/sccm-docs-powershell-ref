---
external help file: AdminUI.PS.AppModel.dll-Help.xml
ms.assetid: 7FF1D4A7-5522-4CA1-9951-040D47781FB2
online version: https://go.microsoft.com/fwlink/?linkid=834305
schema: 2.0.0
---

# Get-CMDeploymentPackage

## SYNOPSIS
Gets information about deployment packages on a distribution point.

## SYNTAX

```
Get-CMDeploymentPackage [-DeploymentPackageName <String>] -DistributionPointName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMDeploymentPackage** cmdlet gets information about one or more deployment packages on a distribution point.
If you do not specify the *DeploymentPackageName* parameter, Microsoft System Center Configuration Manager returns all the deployment packages on the distribution point that you specify.

A deployment package is a Configuration Manager object that contains the content files and instructions for distributing programs, software updates, boot images, operating system images, and drivers to System Center Configuration Manager clients.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Get all deployment packages for a distribution point
```
PS XYZ:\> Get-CMDeploymentPackage -DistributionPointName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM"
```

This command gets all deployment packages that are distributed to clients from the distribution point named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM.

### Example 2: Get a deployment package for a distribution point
```
PS XYZ:\> Get-CMDeploymentPackage -DistributionPointName "CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM" -DeploymentPackageName "Depack01"
```

This command gets the deployment package named Depack01 that is distributed to clients from the distribution point named CMCEN-DIST02.TSQA.CORP.CONTOSCO.COM.

## PARAMETERS

### -DeploymentPackageName
Specifies an array of names of distribution points that are associated with deployment packages.
If you do not specify this parameter, the cmdlet returns status information about all deployment packages on the distribution point.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
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

### -DistributionPointName
Specifies an array of names of deployment packages.

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMDeployment](Get-CMDeployment.md)

[Get-CMDeploymentStatus](Get-CMDeploymentStatus.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Invoke-CMDeploymentSummarization](Invoke-CMDeploymentSummarization.md)


