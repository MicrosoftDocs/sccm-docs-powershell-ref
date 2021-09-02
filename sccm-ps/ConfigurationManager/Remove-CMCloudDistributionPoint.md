---
description: Removes cloud-based distribution points.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMCloudDistributionPoint
---

# Remove-CMCloudDistributionPoint

## SYNOPSIS
Removes cloud-based distribution points.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMCloudDistributionPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMCloudDistributionPoint [-Force] -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMCloudDistributionPoint [-Force] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMCloudDistributionPoint** cmdlet removes specified cloud-based distribution points.

When you remove a distribution point, Configuration Manager deletes all the content stored there.
If you want to suspend a distribution point temporarily, use the [Stop-CMCloudDistributionPoint](Stop-CMCloudDistributionPoint.md) cmdlet.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove all distribution points
```
PS XYZ:\> Remove-CMCloudDistributionPoint
```

This command removes all the cloud distribution points from Configuration Manager.
Unless you use the *Force* parameter, the cmdlet prompts you for confirmation.

### Example 2: Remove a distribution point using a name
```
PS XYZ:\> Remove-CMCloudDistributionPoint -Name "West01"
```

This command removes the cloud distribution point named West01.
Unless you use the *Force* parameter, the cmdlet prompts you for confirmation.

### Example 3: Remove a distribution point using an ID
```
PS XYZ:\> Remove-CMCloudDistributionPoint -Id "16777236"
```

This command removes the cloud distribution point that has the specified identifier.
Unless you use the *Force* parameter, the cmdlet prompts you for confirmation.

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

### -Force
Forces the command to run without asking for user confirmation.

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
Specifies an array of identifiers for cloud distribution points.
You can use a comma separated list.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: AzureServiceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a cloud distribution point object.
To obtain a cloud distribution point object, you can use the Get-CMCloudDistributionPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a cloud distribution point.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMCloudDistributionPoint](Get-CMCloudDistributionPoint.md)

[New-CMCloudDistributionPoint](New-CMCloudDistributionPoint.md)

[Set-CMCloudDistributionPoint](Set-CMCloudDistributionPoint.md)

[Start-CMCloudDistributionPoint](Start-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](Stop-CMCloudDistributionPoint.md)


