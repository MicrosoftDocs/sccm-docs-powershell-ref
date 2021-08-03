---
description: Gets a Windows 10 servicing plan.
external help file: AdminUI.PS.psm1-help.xml
Module Name: ConfigurationManager
ms.date: 05/02/2019
schema: 2.0.0
title: Get-CMWindowsServicingPlan
---

# Get-CMWindowsServicingPlan

## SYNOPSIS
Gets a Windows 10 servicing plan.

## SYNTAX

### SearchByNameMandatory (Default)
```
Get-CMWindowsServicingPlan [[-Name] <String>] [-Fast] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMWindowsServicingPlan [-Id] <Int32> [-Fast] [<CommonParameters>]
```

## DESCRIPTION
The **Get-CMWindowsServicingPlan** cmdlet gets a Windows 10 servicing plan.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all servicing plans
```
PS XYZ:\> Get-CMWindowsServicingPlan -Fast
```

This command gets all Windows 10 servicing plans.
The command does not return lazy properties.

### Example 2: Get a servicing plan by name
```
PS XYZ:\> Get-CMWindowsServicingPlan -Name "SvcPlan01"
```

This command returns the Windows 10 servicing plan named SvcPlan01.

## PARAMETERS

### -Fast
Indicates that the cmdlet does not automatically refresh lazy properties.

Lazy properties contain values that are relatively inefficient to retrieve which can cause additional network traffic and decrease cmdlet performance.
If lazy properties are not used, this parameter should be specified.

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
Specifies the AutoDeploymentID of a servicing plan.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: AutoDeploymentId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Specifies the name of a servicing plan.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[New-CMWindowsServicingPlan](New-CMWindowsServicingPlan.md)


