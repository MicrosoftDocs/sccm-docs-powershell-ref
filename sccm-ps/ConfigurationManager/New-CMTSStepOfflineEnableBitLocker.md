---
external help file: AdminUI.PS.Osd.dll-Help.xml
Module Name: ConfigurationManager
online version:
ms.date: 07/31/2020
schema: 2.0.0
---

# New-CMTSStepOfflineEnableBitLocker

## SYNOPSIS
Add the **Pre-provision BitLocker** step in a task sequence, to enable BitLocker encryption on a drive while in Windows PE.

## SYNTAX

```
New-CMTSStepOfflineEnableBitLocker [-Disk <Int32>] [-Partition <Int32>] [-Drive <String>]
 [-VariableName <String>] [-EnableSkipWhenTpmInvalid <Boolean>] [-EncryptionMethod <DiskEncryptionMethod>]
 -Name <String> [-Description <String>] [-ContinueOnError] [-Disable] [-Condition <IResultObject[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Add the **Pre-provision BitLocker** step in a task sequence, to enable BitLocker encryption on a drive while in Windows PE. For more information on this task sequence step, see [About task sequence steps](https://docs.microsoft.com/mem/configmgr/osd/understand/task-sequence-steps#BKMK_PreProvisionBitLocker).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

{{ Add example description here }}

```powershell
{{ Add example code here }}
```

## PARAMETERS

### -Condition

Specify a condition object to add to this step.

```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: Conditions

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContinueOnError

Add this parameter to enable the step option **Continue on error**. When you enable this option, if the step fails, the task sequence continues.

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

### -Description

Specify an optional description for this task sequence step.

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

### -Disable

Add this parameter to disable this task sequence step.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: DisableThisStep

Required: False
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

### -Disk

Specify the specific disk number to encrypt. Use this parameter with the **-Partition** parameter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DestinationDisk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Drive

Specify the logical drive letter to encrypt. For example, `C:`

```yaml
Type: String
Parameter Sets: (All)
Aliases: DestinationDrive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSkipWhenTpmInvalid

Set this parameter to `true` to skip this step for computers that don't have a TPM or when the TPM isn't enabled.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionMethod

Applies to version 2006 and later. Use this parameter to specify the disk encryption mode. By default or if not specified, the step continues to use the default encryption method for the OS version.

```yaml
Type: DiskEncryptionMethod
Parameter Sets: (All)
Aliases: DiskEncryptionMethod
Accepted values: DoNotSpecify, AES_128, AES_256, XTS_AES128, XTS_AES256, TotalCount

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

### -Name

Specify a name for this step to identify it in the task sequence.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StepName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Partition

Specify the specific partition number to encrypt. Use this parameter with the **-Disk** parameter.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: DestinationPartition

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VariableName

Specify a task sequence variable to identify the logical drive letter as the destination for BitLocker.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DestinationVariable

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

Shows what would happen if the cmdlet runs. It doesn't run the cmdlet.

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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_OfflineEnableBitLockerAction

## NOTES

## RELATED LINKS

[About task sequence steps - Pre-provision BitLocker](https://docs.microsoft.com/mem/configmgr/osd/understand/task-sequence-steps#BKMK_PreProvisionBitLocker)
