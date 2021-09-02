---
description: Remove a maintenance window.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 06/16/2021
schema: 2.0.0
title: Remove-CMMaintenanceWindow
---

# Remove-CMMaintenanceWindow

## SYNOPSIS

Remove a maintenance window.

## SYNTAX

### ByValue (Default)
```
Remove-CMMaintenanceWindow [-Force] [-InputObject] <IResultObject> -MaintenanceWindowName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionId
```
Remove-CMMaintenanceWindow [-CollectionId] <String> [-Force] -MaintenanceWindowName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByCollectionName
```
Remove-CMMaintenanceWindow [-CollectionName] <String> [-Force] -MaintenanceWindowName <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a maintenance window from a collection.

For more information on maintenance windows, see [How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove a maintenance window by name from a collection by ID

This command removes the maintenance window named **Distribution Point Maintenance**. The window is on the collection with ID **XYZ0004D**.

```powershell
Remove-CMMaintenanceWindow -Name "Distribution Point Maintenance" -CollectionId "XYZ0004D"
```

### Example 2: Remove all maintenance windows on a collection

This example first gets a collection object, and then uses the wildcard character to remove all windows without prompting for confirmation.

```powershell
$coll = Get-CMCollection -CollectionId "XYZ0003f"
Remove-CMMaintenanceWindow -InputObject $coll -MaintenanceWindowName "*" -Force
```

## PARAMETERS

### -CollectionId

Specify the ID of a collection from which to remove the maintenance window. This ID is a standard collection ID, for example `XYZ0003F`.

```yaml
Type: String
Parameter Sets: ByCollectionId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CollectionName

Specify the name of a collection from which to remove the maintenance window.

```yaml
Type: String
Parameter Sets: ByCollectionName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

Add this parameter to force the command to run without asking for user confirmation.

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

Specify an object for a collection from which to remove the maintenance window. To get this object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: Collection, Site

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MaintenanceWindowName

Specify the name of a maintenance window to remove from the targeted collection.

You can use wildcard characters:

- `*`: Multiple characters
- `?`: Single character

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -Confirm

Add this parameter to prompt for confirmation before running the cmdlet.

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

[Get-CMMaintenanceWindow](Get-CMMaintenanceWindow.md)

[New-CMMaintenanceWindow](New-CMMaintenanceWindow.md)

[Set-CMMaintenanceWindow](Set-CMMaintenanceWindow.md)

[How to use maintenance windows in Configuration Manager](/mem/configmgr/core/clients/manage/collections/use-maintenance-windows)
