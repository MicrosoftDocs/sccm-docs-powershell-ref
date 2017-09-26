---
external help file: AdminUI.PS.Osd.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-CMTSPartitionSetting

## SYNOPSIS
Creates a t s partition setting

## SYNTAX

### PrimaryPartition (Default)
```
New-CMTSPartitionSetting [-PartitionPrimary] [-Name <String>] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-EnableDriveLetterAssignment <Boolean>] [-IsBootPartition <Boolean>] [-EnableQuickFormat <Boolean>]
 [-PartitionFileSystem <FileSystemType>] [-Variable <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### EfiPartition
```
New-CMTSPartitionSetting [-PartitionEfi] [-Name <String>] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ExtendedPartition
```
New-CMTSPartitionSetting [-PartitionExtended] [-Name <String>] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### HiddenPartition
```
New-CMTSPartitionSetting [-PartitionHidden] [-Name <String>] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LogicalPartition
```
New-CMTSPartitionSetting [-PartitionLogical] [-Name <String>] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### MsrPartition
```
New-CMTSPartitionSetting [-PartitionMsr] [-Name <String>] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RecoveryPartition
```
New-CMTSPartitionSetting [-PartitionRecovery] [-Name <String>] [-Size <Int32>] [-SizeUnit <SizeUnitType>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
{{Fill in the Description}}

## EXAMPLES

### Example 1
```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

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

### -EnableDriveLetterAssignment
{{Fill EnableDriveLetterAssignment Description}}

```yaml
Type: Boolean
Parameter Sets: PrimaryPartition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableQuickFormat
{{Fill EnableQuickFormat Description}}

```yaml
Type: Boolean
Parameter Sets: PrimaryPartition
Aliases: 

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

### -IsBootPartition
{{Fill IsBootPartition Description}}

```yaml
Type: Boolean
Parameter Sets: PrimaryPartition
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{Fill Name Description}}

```yaml
Type: String
Parameter Sets: (All)
Aliases: PartitionName, VolumeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionEfi
{{Fill PartitionEfi Description}}

```yaml
Type: SwitchParameter
Parameter Sets: EfiPartition
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionExtended
{{Fill PartitionExtended Description}}

```yaml
Type: SwitchParameter
Parameter Sets: ExtendedPartition
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionFileSystem
{{Fill PartitionFileSystem Description}}

```yaml
Type: FileSystemType
Parameter Sets: PrimaryPartition
Aliases: 
Accepted values: Ntfs, Fat32

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionHidden
{{Fill PartitionHidden Description}}

```yaml
Type: SwitchParameter
Parameter Sets: HiddenPartition
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionLogical
{{Fill PartitionLogical Description}}

```yaml
Type: SwitchParameter
Parameter Sets: LogicalPartition
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionMsr
{{Fill PartitionMsr Description}}

```yaml
Type: SwitchParameter
Parameter Sets: MsrPartition
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionPrimary
{{Fill PartitionPrimary Description}}

```yaml
Type: SwitchParameter
Parameter Sets: PrimaryPartition
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartitionRecovery
{{Fill PartitionRecovery Description}}

```yaml
Type: SwitchParameter
Parameter Sets: RecoveryPartition
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Size
{{Fill Size Description}}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SizeUnit
{{Fill SizeUnit Description}}

```yaml
Type: SizeUnitType
Parameter Sets: (All)
Aliases: 
Accepted values: MB, GB, Percent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Variable
{{Fill Variable Description}}

```yaml
Type: String
Parameter Sets: PrimaryPartition
Aliases: 

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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_PartitionSettings

## NOTES

## RELATED LINKS

