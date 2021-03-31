---
description: Removes a service connection point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Remove-CMServiceConnectionPoint
---

# Remove-CMServiceConnectionPoint

## SYNOPSIS
Removes a service connection point.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMServiceConnectionPoint [-Force] -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMServiceConnectionPoint [-Force] [-SiteCode <String>] [-SiteSystemServerName] <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMServiceConnectionPoint** cmdlet removes a service connection point role from a site system server.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a service connection point by name
```
PS XYZ:\> Remove-CMServiceConnectionPoint -SiteSystemServerName "SiteSystemServer01.Contoso.com" -SiteCode PS1 -Force
```

This command removes the service connection point role from the site system server named SiteSystemServer01.Contoso.com with the site code PS1.
Specifying the *Force* parameter indicates that the user is not prompted before the service connection point is removed.

### Example 2: Remove a service connection point by using a variable
```
PS XYZ:\> $ConnPoint = Get-CMServiceConnectionPoint -SiteCode PS1 -SiteSystemServerName "SiteSystemServer02.Contoso.com"
PS XYZ:\> Remove-CMServiceConnectionPoint -InputObject $ConnPoint -Force
```

The first command gets the service connection point object for the site system server named SiteSystemServer02.Contoso.com with the site code PS1 and stores the object in the $ConnPoint variable.

The second command removes the service connection point object stored in $ConnPoint.
Specifying the *Force* parameter indicates that the user is not prompted before the service connection point is removed.

### Example 3: Remove a service connection point by using the pipeline
```
PS XYZ:\> Get-CMServiceConnectionPoint -SiteCode PS1 -SiteSystemServerName "SiteSystemServer03.Contoso.com" | Remove-CMServiceConnectionPoint -Force
```

This command gets the service connection point object for the site system server named SiteSystemServer03.Contoso.com with the site code PS1 and uses the pipeline operator to pass the object to **Remove-CMServiceConnectionPoint**, which removes the service connection point object.
Specifying the *Force* parameter indicates that the user is not prompted before the service connection point is removed.

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

### -InputObject
Specifies a service connection point object.
To obtain a service connection point object, use the Get-CMServiceConnectionPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ReportingServicePoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteSystemServerName
Specifies the name of a site system server that hosts the service connection point role.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: Name, ServerName

Required: True
Position: 0
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

### 

## NOTES

## RELATED LINKS

[Add-CMServiceConnectionPoint](Add-CMServiceConnectionPoint.md)

[Get-CMServiceConnectionPoint](Get-CMServiceConnectionPoint.md)

[Set-CMServiceConnectionPoint](Set-CMServiceConnectionPoint.md)


