---
external help file: AdminUI.PS.AppModel.dll-Help.xml
ms.assetid: 63B857FB-228C-497F-BE06-4795E85C2986
online version: https://go.microsoft.com/fwlink/?linkid=833820
schema: 2.0.0
---

# New-CMVirtualEnvironmentGroup

## SYNOPSIS
Creates a virtual environment group.

## SYNTAX

### NewByValue (Default)
```
New-CMVirtualEnvironmentGroup -Name <String> -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewByDTI
```
New-CMVirtualEnvironmentGroup -Name <String> -DeploymentTypeItem <DeploymentTypeItem[]>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMVirtualEnvironmentGroup** cmdlet creates a virtual environment group that specifies deployment type items.

A virtual environment allows two or more Microsoft Application Virtualization (App-V) deployment types to share the same file system and registry on client computers.
When multiple virtual applications modify the same file system or registry values on a client computer, the application with the highest order takes precedence.
When an application is installed or when a client evaluates installed applications, the virtual environment on client computers is added or modified.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Create a virtual environment group
```
PS XYZ:\> New-CMVirtualEnvironmentGroup -DeploymentType "Office_Standard" -Name "Office Remote Apps"
```

This command creates a virtual environment group named Office Remote Apps for the deployment type Office_Standard.

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

### -DeploymentTypeItem
```yaml
Type: DeploymentTypeItem[]
Parameter Sets: NewByDTI
Aliases: DeploymentType

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
Specifies the input to this cmdlet. 
You can use this parameter, or you can pipe the input to this cmdlet. 

```yaml
Type: IResultObject[]
Parameter Sets: NewByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for the virtual environment group.

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

