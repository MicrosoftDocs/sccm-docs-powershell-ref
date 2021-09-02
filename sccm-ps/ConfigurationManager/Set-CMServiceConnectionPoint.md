---
description: Sets a service connection point.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMServiceConnectionPoint
---

# Set-CMServiceConnectionPoint

## SYNOPSIS
Sets a service connection point.

## SYNTAX

### ByValue (Default)
```
Set-CMServiceConnectionPoint -InputObject <IResultObject> [-Mode <ServiceConnectionPointMode>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMServiceConnectionPoint [-Mode <ServiceConnectionPointMode>] [-PassThru] [-SiteCode <String>]
 [-SiteSystemServerName] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMServiceConnectionPoint** updates the settings of a connection service point.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a service connection point
```
PS XYZ:\> Set-CMServiceConnectionPoint -SiteSystemServerName "SiteSystemServer01.Contoso.com" -SiteCode PS1 -Mode Offline
```

This command sets the mode for the site system server named SiteSystemServer01.Contoso.com to offline.

### Example 2: Set a service connection point by using a variable
```
PS XYZ:\> $Server = Get-CMServiceConnectionPoint -SiteCode PS1 -SiteSystemServerName "SiteSystemServer02.Contoso.com"
PS XYZ:\> Set-CMServiceConnectionPoint -InputObject $Server -Mode Offline
```

The first command gets the site system server object named SiteSystemServer02.Contoso.com with the site code PS1 and stores the object in the $Server variable.

The second command sets the mode for the site system server stored in $Server to offline.

### Example 3: Set a service connection point by using the pipeline
```
PS XYZ:\> Get-CMServiceConnectionPoint -SiteCode PS1 -SiteSystemServerName "SiteSystemServer03.Contoso.com" | Set-CMServiceConnectionPoint -Mode Offline
```

This command gets the site system server object named SiteSystemServer03.Contoso.com with the site code PS1 and uses the pipeline operator to pass the object to **Set-CMServiceConnectionPoint**, which sets the mode for the server object to offline.

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

### -InputObject
Specifies a service connection point object.
To obtain a service connection point object, use the Get-CMServiceConnectionPoint cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: ServiceConnectionPoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Mode
Specifies a mode for the service connection point.
Valid values are:

- Online
- Offline

```yaml
Type: ServiceConnectionPointMode
Parameter Sets: (All)
Aliases:
Accepted values: Online, Offline

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### -SiteCode
Specifies the site code for a Configuration Manager site.

```yaml
Type: String
Parameter Sets: ByName
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
Parameter Sets: ByName
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

### IResultObject#SMS_SCI_SysResUse
## NOTES

## RELATED LINKS

[Add-CMServiceConnectionPoint](Add-CMServiceConnectionPoint.md)

[Get-CMServiceConnectionPoint](Get-CMServiceConnectionPoint.md)

[Remove-CMServiceConnectionPoint](Remove-CMServiceConnectionPoint.md)


