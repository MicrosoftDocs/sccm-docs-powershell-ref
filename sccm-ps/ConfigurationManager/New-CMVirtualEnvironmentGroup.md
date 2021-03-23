---
description: Creates a virtual environment group.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: New-CMVirtualEnvironmentGroup
---

# New-CMVirtualEnvironmentGroup

## SYNOPSIS
Creates a virtual environment group.

## SYNTAX

### NewByValue (Default)
```
New-CMVirtualEnvironmentGroup -InputObject <IResultObject[]> -Name <String> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### NewByDTI
```
New-CMVirtualEnvironmentGroup -DeploymentTypeItem <DeploymentTypeItem[]> -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMVirtualEnvironmentGroup** cmdlet creates a virtual environment group that specifies deployment type items.

A virtual environment allows two or more Microsoft Application Virtualization (App-V) deployment types to share the same file system and registry on client computers.
When multiple virtual applications modify the same file system or registry values on a client computer, the application with the highest order takes precedence.
When an application is installed or when a client evaluates installed applications, the virtual environment on client computers is added or modified.

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1: Create a virtual environment group
```
PS XYZ:\> New-CMVirtualEnvironmentGroup -DeploymentType "Office_Standard" -Name "Office Remote Apps"
```

This command creates a virtual environment group named Office Remote Apps for the deployment type Office_Standard.

## PARAMETERS

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
