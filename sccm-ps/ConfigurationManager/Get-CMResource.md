---
description: Get a Configuration Manager resource.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 10/01/2020
schema: 2.0.0
title: Get-CMResource
---

# Get-CMResource

## SYNOPSIS

Get a Configuration Manager resource.

## SYNTAX

```
Get-CMResource [-Fast] [[-ResourceId] <Int32>] [-ResourceType <ResourceType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

The **Get-CMResource** cmdlet gets a Configuration Manager resource, such as a device or a user.

For more complete data, use [Get-CMDevice](Get-CMDevice.md) or [Get-CMUser](Get-CMUser.md). For devices, it queries the **SMS_R_System** class. If you use `Get-CMDevice -Resource` the output is the same as **Get-CMResource**.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a resource by ID

This command gets the resource with the ID **2097152000** and doesn't return lazy properties.

```powershell
Get-CMResource -ResourceID "2097152000" -Fast
```

### Example 2: Get all user resources

This command gets all user resources.

```powershell
Get-CMResource -ResourceType User
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

### -Fast

Add this parameter to not automatically refresh lazy properties. Lazy properties contain values that are relatively inefficient to retrieve. Getting these properties can cause additional network traffic and decrease cmdlet performance.

If you don't use this parameter, the cmdlet displays a warning. To disable this warning, set `$CMPSSuppressFastNotUsedCheck = $true`.

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

### -ResourceId

Specifies the ID of a resource. For example, `16780010`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceType

Specifies the resource type.

```yaml
Type: ResourceType
Parameter Sets: (All)
Aliases:
Accepted values: None, UnknownResource, UserGroup, User, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None
## OUTPUTS

### IResultObject#SMS_Resource
## NOTES

## RELATED LINKS

[Remove-CMResource](Remove-CMResource.md)

[Get-CMDevice](Get-CMDevice.md)

[Get-CMUser](Get-CMUser.md)
