---
description: Starts the cloud distribution point service.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Start-CMCloudDistributionPoint
---

# Start-CMCloudDistributionPoint

## SYNOPSIS
Starts the cloud distribution point service.

## SYNTAX

### SearchByValueMandatory (Default)
```
Start-CMCloudDistributionPoint -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Start-CMCloudDistributionPoint -Id <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Start-CMCloudDistributionPoint -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Start-CMCloudDistributionPoint** cmdlet starts the cloud distribution point service.

You can use the [Stop-CMCloudDistributionPoint](Stop-CMCloudDistributionPoint.md) cmdlet to suspend distribution of content.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Start the cloud distribution point service using an ID
```
PS XYZ:\> Start-CMCloudDistributionPoint -Id "16777242"
```

This command starts the cloud distribution point service for the cloud distribution point that has the specified identifier.

### Example 2: Start the cloud distribution point service using a name
```
PS XYZ:\> Start-CMCloudDistributionPoint -Name "West01"
```

This command starts the cloud distribution point service for the cloud distribution point named West01.

### Example 3: Start the cloud distribution point service using an object
```
PS XYZ:\> $DistPnt = Get-CMCloudDistributionPoint -Id "16777242"
PS XYZ:\> Start-CMCloudDistributionPoint -InputObject $DistPnt
```

The first command uses the **Get-CMCloudDistributionPoint** cmdlet to get the distribution point with the specified identifier, and then saves it in the $DistPnt variable.

The second command starts the cloud distribution point service for the distribution point stored in $DistPnt.

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
Specifies an array of identifiers for cloud distribution points.
You can use a comma-separated list.

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
To obtain a cloud distribution point object, you can use the [Get-CMCloudDistributionPoint](Get-CMCloudDistributionPoint.md) cmdlet.

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

[Remove-CMCloudDistributionPoint](Remove-CMCloudDistributionPoint.md)

[Set-CMCloudDistributionPoint](Set-CMCloudDistributionPoint.md)

[Stop-CMCloudDistributionPoint](Stop-CMCloudDistributionPoint.md)
