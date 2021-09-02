---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 04/26/2021
schema: 2.0.0
title: Disconnect-CMTrackedObject
---

# Disconnect-CMTrackedObject

## SYNOPSIS

Clean up unused PowerShell objects to avoid SMS Provider quota violation errors.

## SYNTAX

### ByValue (Default)
```
Disconnect-CMTrackedObject [-Force] -InputObject <IDisposable[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByAll
```
Disconnect-CMTrackedObject [-All] [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

When you use **Start-CMObjectTracking** to track SMS Provider objects used by the PowerShell runtime, use this cmdlet to clean up these resources when they're no longer needed.

When you run **Start-CMObjectTracking**, the PowerShell runtime tracks **IResultObject** objects created by Configuration Manager cmdlets. For objects that aren't manually cleaned up with `.Dispose()`, reclaim them by using **Disconnect-CMTrackedObject** against an individual object.

Once an object is reclaimed, it can no longer be reused or passed to another cmdlet through the object pipeline.

**Stop-CMObjectTracking** can be used to turn off object tracking. Previously allocated objects remain active.

Unclaimed resources can cause the SMS Provider to raise quota violation errors. These quota issues typically manifest from working with large sets of SMS Provider objects or in long-running environments.

> [!NOTE]
> This feature is experimental and may be subject to change or removal in a future release.
>
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

The first command turns on object tracking. The second command reclaims a single object specified by the **$obj** variable. The third command reclaims all tracked objects. The last command turns off object tracking.

```powershell
Start-CMObjectTracking

# Reclaim a single tracked object
$obj | Disconnect-CMTrackedObject -Force

# Reclaim all tracked objects
Disconnect-CMTrackedObject -All

Stop-CMObjectTracking
```

## PARAMETERS

### -All

Add this parameter to reclaim all tracked objects.

```yaml
Type: SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: True
Position: Named
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

Add this parameter to run the command without asking for confirmation.

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

Specify any **IResultObject** that you previously created with a Configuration Manager cmdlet.

```yaml
Type: IDisposable[]
Parameter Sets: ByValue
Aliases: InputObjects

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm

Add this parameter to prompt for confirmation before the cmdlet runs.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### System.IDisposable[]
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Start-CMObjectTracking](Start-CMObjectTracking.md)
[Stop-CMObjectTracking](Stop-CMObjectTracking.md)
