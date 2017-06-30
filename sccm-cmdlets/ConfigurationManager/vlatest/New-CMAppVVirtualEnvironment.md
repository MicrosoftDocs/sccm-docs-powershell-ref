---
external help file: AdminUI.PS.AppModel.dll-Help.xml
ms.assetid: 5FB30D79-F7FE-45AD-B888-2B3D5AC7C74E
online version: https://go.microsoft.com/fwlink/?linkid=834252
schema: 2.0.0
---

# New-CMAppVVirtualEnvironment

## SYNOPSIS
Creates an App-V virtual environment.

## SYNTAX

```
New-CMAppVVirtualEnvironment -Name <String> [-Description <String>]
 -ApplicationGroup <VirtualEnvironmentGroup[]> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMAppVVirtualEnvironment** cmdlet creates an Microsoft Application Virtualization (App-V) virtual environment in Microsoft System Center Configuration Manager.
App-V virtual environments in System Center Configuration Manager enable deployed virtual applications to share the same file system and registry on client computers.

## EXAMPLES

### Example 1: Create an App-V virtual environment
```
PS C:\> $Dti = Get-CMAppV5XDeploymentTypeItem -ApplicationName "App01d2012" -DeploymentTypeName "7Zip - Microsoft Application Virtualization 5"
PS C:\> $Veg = New-CMVirtualEnvironmentGroup -Name "Venvgroup01" -DeploymentType $Dti
PS C:\> New-CMAppVVirtualEnvironment -Name "CMAppVenv01" -Description "App-V virtual environment" -ApplicationGroup $Veg
```

This first command uses the **Get-CMAppV5XDeploymentTypeItem** cmdlet gets the deployment type named 7Zip - Microsoft Application Virtualization 5 in the application named App01d2012.
The command stores the result in the $Dti variable.

This second command creates an application group named Venvgroup01 for the deployment type stored in $Dti.
The command stores the result in the $Veg variable.

This third command creates an App-V virtual environment named CMAppVenv01 for the application group stored in $Veg.

## PARAMETERS

### -ApplicationGroup
Specifies an array of application groups to add to the App-V virtual environment.
To obtain an application group, use the New-CMVirtualEnvironmentGroup cmdlet.

```yaml
Type: VirtualEnvironmentGroup[]
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

### -Description
Specifies a description for the App-V virtual environment.

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

### -Name
Specifies a name for the App-V virtual environment.

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

[Get-CMAppVVirtualEnvironment](./Get-CMAppVVirtualEnvironment.md)

[New-CMVirtualEnvironmentGroup](./New-CMVirtualEnvironmentGroup.md)

[Remove-CMAppVVirtualEnvironment](./Remove-CMAppVVirtualEnvironment.md)

[Set-CMAppVVirtualEnvironment](./Set-CMAppVVirtualEnvironment.md)


