---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/31/2020
online version:
schema: 2.0.0
---

# New-CMTSStepEnableBitLocker

## SYNOPSIS
Add the **Enable BitLocker** step to a task sequence, which enables BitLocker encryption on the hard drive.

## SYNTAX

```
New-CMTSStepEnableBitLocker [-CreateKeyOption <CreateKeyType>] [-Drive <String>]
 [-EnableSkipWhenNoValidTpm <Boolean>] [-EncryptFullDisk] [-EncryptionMethod <DiskEncryptionMethod>]
 [-Pin <SecureString>] [-TpmAndPin] [-TpmAndUsb] [-TpmOnly] [-UsbOnly] [-WaitForBitLockerComplete]
 [-Condition <IResultObject[]>] [-ContinueOnError] [-Description <String>] [-Disable] -Name <String>
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
Add the **Enable BitLocker** step to a task sequence, which enables BitLocker encryption on the hard drive. For more information on this task sequence step, see [About task sequence steps](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_EnableBitLocker).

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

Specify a condition object to use with this step.

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

### -CreateKeyOption

Use one of the following values to specify where to create the recovery key:

- `ActiveDirectoryDomainServices`: Create the recovery password and escrow it in Active Directory (recommended)
- `DoNotCreateRecoveryKey`: Encrypt the drive, but don't create a recovery password.

```yaml
Type: CreateKeyType
Parameter Sets: (All)
Aliases:
Accepted values: ActiveDirectoryDomainServices, DoNotCreateRecoveryKey

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

### -Drive

Specify the drive to encrypt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpecificDrive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableSkipWhenNoValidTpm

Applies to version 2006 and later. Set this parameter to `true` to skip this step for computers that don't have a TPM or when the TPM isn't enabled.

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

### -EncryptFullDisk

Applies to version 1906 and later. Add this parameter to use full disk encryption. By default, the **Enable BitLocker** step only encrypts used space on the drive.

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

### -Pin

If you use the parameter **-TpmAndPin**, use this parameter to specify the PIN value. Specify 4-20 integers.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TpmAndPin

Add this parameter to configure key management for the OS drive to use a TPM and a personal identification number (PIN). When you specify this option, BitLocker locks the normal boot process until the user provides the PIN. If you use this parameter, use **-Pin** to specify the PIN value. You can't combine this parameter with **-TpmAndUsb**, **-TpmOnly**, or **-UsbOnly**.

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

### -TpmAndUsb

Add this parameter to configure key management for the OS drive to use a TPM and a startup key stored on a USB flash drive. When you select this option, BitLocker locks the normal boot process until a USB device that contains a BitLocker startup key is attached to the computer. You can't combine this parameter with **-TpmAndPin**, **-TpmOnly**, or **-UsbOnly**.

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

### -TpmOnly

Add this parameter to configure key management for the OS drive to only use a TPM. You can't combine this parameter with **-TpmAndPin**, **-TpmAndUsb**, or **-UsbOnly**.

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

### -UsbOnly

Add this parameter to configure key management for the OS drive to only use a startup key stored on a USB flash drive. When you select this option, BitLocker locks the normal boot process until a USB device that contains a BitLocker startup key is attached to the computer. You can't combine this parameter with **-TpmAndPin**, **-TpmAndUsb**, or **-TpmOnly**.

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

### -WaitForBitLockerComplete

Add this parameter to configure the step to wait for BitLocker to complete the drive encryption process on all drives before continuing task sequence execution.

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

### IResultObject#SMS_TaskSequence_EnableBitLockerAction
## NOTES

## RELATED LINKS

[About task sequence steps - Enable BitLocker](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_EnableBitLocker)
