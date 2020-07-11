---
description: Sets a client setting hardware inventory.
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMClientSettingHardwareInventory
---

# Set-CMClientSettingHardwareInventory

## SYNOPSIS
Sets a client setting hardware inventory.

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingHardwareInventory [-Enable <Boolean>] [-Schedule <IResultObject>]
 [-InventoryReportId <String>] [-CleanInventoryReportClass] [-RemoveInventoryReportClassById <String[]>]
 [-AddInventoryReportClass <IResultObject[]>] [-MaxRandomDelayMins <Int32>] [-MaxThirdPartyMifSize <Int32>]
 [-CollectMifFile <MifCollectionType>] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingHardwareInventory [-Enable <Boolean>] [-Schedule <IResultObject>]
 [-InventoryReportId <String>] [-CleanInventoryReportClass] [-RemoveInventoryReportClassById <String[]>]
 [-AddInventoryReportClass <IResultObject[]>] [-MaxRandomDelayMins <Int32>] [-MaxThirdPartyMifSize <Int32>]
 [-CollectMifFile <MifCollectionType>] [-DefaultSetting] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingHardwareInventory [-Enable <Boolean>] [-Schedule <IResultObject>]
 [-InventoryReportId <String>] [-CleanInventoryReportClass] [-RemoveInventoryReportClassById <String[]>]
 [-AddInventoryReportClass <IResultObject[]>] [-MaxRandomDelayMins <Int32>] [-MaxThirdPartyMifSize <Int32>]
 [-CollectMifFile <MifCollectionType>] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

> [!NOTE]
> Configuration Manager cmdlets must be run from the Configuration Manager site drive.
> The examples in this article use the site name **XYZ**. For more information, see the
> [getting started](/powershell/sccm/overview) documentation.

## EXAMPLES

### Example 1
```
PS XYZ:\>
```

## PARAMETERS

### -AddInventoryReportClass
{{ Fill AddInventoryReportClass Description }}

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanInventoryReportClass
{{ Fill CleanInventoryReportClass Description }}

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

### -CollectMifFile
```yaml
Type: MifCollectionType
Parameter Sets: (All)
Aliases: CollectMifFiles
Accepted values: None, CollectNoIdMifFile, CollectIdMifFile, CollectIdMifAndNoIdMifFile

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultSetting
```yaml
Type: SwitchParameter
Parameter Sets: SetDefaultSetting
Aliases:

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

### -Enable
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableHardwareInventory

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
```yaml
Type: IResultObject
Parameter Sets: SetCustomSettingByValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -InventoryReportId
```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxRandomDelayMins
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumRandomDelayMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxThirdPartyMifSize
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaximumThirdPartyMifSize

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
```yaml
Type: String
Parameter Sets: SetCustomSettingByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working. By default, this cmdlet may not generate any output.

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

### -RemoveInventoryReportClassById
{{ Fill RemoveInventoryReportClassById Description }}

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Schedule
```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: InventorySchedule, HardwareInventorySchedule

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
Default value: None
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
Default value: None
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
