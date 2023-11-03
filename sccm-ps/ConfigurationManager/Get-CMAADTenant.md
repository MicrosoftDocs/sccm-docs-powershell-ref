---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/01/2022
schema: 2.0.0
title: Get-CMAADTenant
---

# Get-CMAADTenant

## SYNOPSIS

Get Microsoft Entra tenant connected with the Configuration Manager site.

## SYNTAX

### SetById
```
Get-CMAADTenant -Id <string> [-DisableWildcardHandling] [-ForceWildcardHandling]  [<CommonParameters>]
```

### SetByName
```
Get-CMAADTenant [-Name <string>] [-DisableWildcardHandling] [-ForceWildcardHandling]  [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get Microsoft Entra tenant connected with the Configuration Manager site.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get all Microsoft Entra tenants connected with the Configuration Manager site

```powershell
Get-CMAADTenant

```

### Example 2: Get a Microsoft Entra tenant with name "Contoso" connected with the Configuration Manager site

```powershell
Get-CMAADTenant -Name "Contoso"

```

### Example 2: Get a Microsoft Entra tenant with Id "72f988bf-00ab-11cd-22ef-2d7cd011db00" connected with the Configuration Manager site

```powershell
Get-CMAADTenant -Id "72f988bf-00ab-11cd-22ef-2d7cd011db00"

```

## PARAMETERS

### -DisableWildcardHandling

This parameter treats wildcard characters as literal character values. You can't combine it with **ForceWildcardHandling**.

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

This parameter processes wildcard characters and may lead to unexpected behavior (not recommended). You can't combine it with **DisableWildcardHandling**.

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

Specify the Tenant ID of Microsoft Entra tenant.

```yaml
Type: String
Parameter Sets: SetById
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the Name of Microsoft Entra tenant.

```yaml
Type: String
Parameter Sets: SetByName
Aliases:

Required: False
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

Shows what would happen if the cmdlet runs. The cmdlet doesn't run.

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

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Set-CMCollectionCloudSync](Set-CMCollectionCloudSync.md)
