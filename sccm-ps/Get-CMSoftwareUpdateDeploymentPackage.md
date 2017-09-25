---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 183D4DE8-9632-41D4-94D3-94CAED832637
online version: https://go.microsoft.com/fwlink/?linkid=833909
schema: 2.0.0
---

# Get-CMSoftwareUpdateDeploymentPackage

## SYNOPSIS
Retrieves a deployment package.

## SYNTAX

### SearchByName (Default)
```
Get-CMSoftwareUpdateDeploymentPackage [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMSoftwareUpdateDeploymentPackage -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMSoftwareUpdateDeploymentPackage** cmdlet retrieves a deployment package for a software update.
A **CMSoftwareUpdateDeploymentPackage** object contains one or more software updates.

## EXAMPLES

### Example 1: Get a deployment package by using a name
```
PS C:\> Get-CMSoftwareUpdateDeploymentPackage -Name "Asdset"
```

This command gets a deployment package named Asdset.

### Example 2: Get a deployment package by using an ID
```
PS C:\> Get-CMSoftwareUpdateDeploymentPackage -Id "ST10000C"
```

This command gets a deployment package that has the ID ST10000C.

## PARAMETERS

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

### -Id
Specifies an array of IDs for the deployment package.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies a name for the deployment package.

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

[Remove-CMSoftwareUpdateDeploymentPackage](Remove-CMSoftwareUpdateDeploymentPackage.md)

[Set-CMSoftwareUpdateDeploymentPackage](Set-CMSoftwareUpdateDeploymentPackage.md)


