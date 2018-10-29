---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-CMClientSettingSoftwareInventory

## SYNOPSIS
Sets a client setting software inventory

## SYNTAX

### SetCustomSettingByName (Default)
```
Set-CMClientSettingSoftwareInventory [-Enable <Boolean>] [-Schedule <IResultObject>]
 [-ReportOption <ReportOptionType>] [-FileName <String>] [-FileDisplayName <String>]
 [-FileInventoriedName <String>] [-AddInventoryFileType <Hashtable[]>] [-RemoveInventoryFileType <Hashtable[]>]
 [-CleanInventoryFileType] [-AddCollectFile <Hashtable[]>] [-RemoveCollectFile <Hashtable[]>]
 [-CleanCollectFile] -Name <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SetDefaultSetting
```
Set-CMClientSettingSoftwareInventory [-Enable <Boolean>] [-Schedule <IResultObject>]
 [-ReportOption <ReportOptionType>] [-FileName <String>] [-FileDisplayName <String>]
 [-FileInventoriedName <String>] [-AddInventoryFileType <Hashtable[]>] [-RemoveInventoryFileType <Hashtable[]>]
 [-CleanInventoryFileType] [-AddCollectFile <Hashtable[]>] [-RemoveCollectFile <Hashtable[]>]
 [-CleanCollectFile] [-DefaultSetting] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetCustomSettingByValue
```
Set-CMClientSettingSoftwareInventory [-Enable <Boolean>] [-Schedule <IResultObject>]
 [-ReportOption <ReportOptionType>] [-FileName <String>] [-FileDisplayName <String>]
 [-FileInventoriedName <String>] [-AddInventoryFileType <Hashtable[]>] [-RemoveInventoryFileType <Hashtable[]>]
 [-CleanInventoryFileType] [-AddCollectFile <Hashtable[]>] [-RemoveCollectFile <Hashtable[]>]
 [-CleanCollectFile] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
 

## EXAMPLES

### Example 1
```
PS C:\>  
```

 

## PARAMETERS

### -AddCollectFile
 

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: AddCollectFiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AddInventoryFileType
 

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: AddInventoryFileTypes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanCollectFile
 

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanCollectFiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanInventoryFileType
 

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanInventoryFileTypes

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
Aliases: EnableSoftwareInventory

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileDisplayName
 

```yaml
Type: String
Parameter Sets: (All)
Aliases: SoftwareInventoryFileDisplayName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileInventoriedName
 

```yaml
Type: String
Parameter Sets: (All)
Aliases: SoftwareInventoryFileInventoriedName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileName
 

```yaml
Type: String
Parameter Sets: (All)
Aliases: SoftwareInventoryFileName

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

### -RemoveCollectFile
 

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: RemoveCollectFiles

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RemoveInventoryFileType
 

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: RemoveInventoryFileTypes

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReportOption
 

```yaml
Type: ReportOptionType
Parameter Sets: (All)
Aliases: 
Accepted values: None, ProductOnly, FileOnly, FullDetail

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
Aliases: InventorySchedule, SoftwareInventorySchedule

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

