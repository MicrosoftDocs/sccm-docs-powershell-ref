---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: EA722095-C1A2-4454-9936-19EFB7088C47
online version: https://go.microsoft.com/fwlink/?linkid=834084
schema: 2.0.0
---

# Set-CMSoftwareUpdateDeploymentPackage

## SYNOPSIS
Modifies a software update deployment package.

## SYNTAX

### SetById (Default)
```
Set-CMSoftwareUpdateDeploymentPackage -Id <String> [-NewName <String>] [-Description <String>] [-Path <String>]
 [-Priority <Priorities>] [-RemoveExpired] [-RemoveSuperseded] [-RefreshDistributionPoint] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareUpdateDeploymentPackage -Name <String> [-NewName <String>] [-Description <String>]
 [-Path <String>] [-Priority <Priorities>] [-RemoveExpired] [-RemoveSuperseded] [-RefreshDistributionPoint]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMSoftwareUpdateDeploymentPackage -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-Path <String>] [-Priority <Priorities>] [-RemoveExpired] [-RemoveSuperseded] [-RefreshDistributionPoint]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdateDeploymentPackage** cmdlet modifies a software update deployment package.
A software update deployment package contains one or more software updates for deployment to a collection of computers.

## EXAMPLES

### Example 1: Update the name and description of a software update deployment package
```
PS C:\> Set-CMSoftwareUpdateDeploymentPackage -Id "ST10000C" -Description "Deployment pack 107" -NewName "SDPTest"
```

This command sets a new name and description for the deployment package that has the ID ST10000C.

### Example 2: Add membership to a security scope of a software update deployment package
```
PS C:\> Set-CMSoftwareUpdateDeploymentPackage -Name "DP107" -SecurityScopeAction AddMembership -SecurityScopeName "testScopeName"
```

This command adds membership for the security scope named testScopeName.

### Example 3: Remove membership from a security scope of a software update deployment package
```
PS C:\> Set-CMSoftwareUpdateDeploymentPackage -Name "DP107" -SecurityScopeAction RemoveMembership -SecurityScopeName "testScopeName"
```

This command removes membership for the security scope named testScopeName.

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

### -Description
Specifies a description for the deployment package.

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
Specifies an array of identifiers for the deployment package.

```yaml
Type: String
Parameter Sets: SetById
Aliases: PackageId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMSoftwareUpdateDeploymentPackage** object.
To obtain an **CMSoftwareUpdateDeploymentPackage** object, use the [Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for the deployment package.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the deployment package.

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
Returns the current working object.
By default, this cmdlet does not generate any output.

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

### -Path
Specifies a package source (URL) for the deployment package.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath, PkgSourcePath

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority
Specifies a distribution priority for the deployment package.

```yaml
Type: Priorities
Parameter Sets: (All)
Aliases: 
Accepted values: High, Normal, Low

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RefreshDistributionPoint
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

### -RemoveExpired
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RemoveDownloadedExpiredSoftwareUpdateFromPackage

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveSuperseded
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: RemoveDownloadedSupersededSoftwareUpdateFromPackage

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

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)

[Remove-CMSoftwareUpdateDeploymentPackage](Remove-CMSoftwareUpdateDeploymentPackage.md)
