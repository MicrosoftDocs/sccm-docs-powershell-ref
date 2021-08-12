---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 08/11/2021
online version:
schema: 2.0.0
---

# New-CMTSStepCaptureSystemImage

## SYNOPSIS

Create an **Capture OS Image** step, which you can add to a task sequence.

## SYNTAX

```
New-CMTSStepCaptureSystemImage [-ImageCreator <String>] [-ImageDescription <String>] [-ImageVersion <String>]
 [-Password <SecureString>] -Path <String> -UserName <String> [-Condition <IResultObject[]>] [-ContinueOnError]
 [-Description <String>] [-Disable] -Name <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

This cmdlet creates a new **Capture OS Image** step object. Then use the [Add-CMTaskSequenceStep](Add-CMTaskSequenceStep.md) cmdlet to add the step to a task sequence. For more information on this step, see [About task sequence steps: Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first uses the **ConvertTo-SecureString** built-in cmdlet to create a secure string for the user password. This method is used here as a simple example, but not the most secure since the plain text password is in the script. For more information on this cmdlet and other options, see [ConvertTo-SecureString](/powershell/module/microsoft.powershell.security/convertto-securestring).

The next line creates an object for the **Capture OS Image** step, using the secure string password variable.

It then gets a task sequence object, and adds this new step to the task sequence at index 11.

```powershell
$Secure_String_Pwd = ConvertTo-SecureString "P@ssW0rD!" -AsPlainText -Force

$step = New-CMTSStepCaptureSystemImage -Name "Capture OS Image" -Path "\\server\share$\images\image.wim" -UserName "contoso\_osdcapture" -Password $Secure_String_Pwd -ImageCreator "Meaghan C" -ImageDescription "The Virginia moon image" -ImageVersion "1.3b"

$tsNameOsd = "Default OS deployment"
$tsOsd = Get-CMTaskSequence -Name $tsNameOsd -Fast

$tsOsd | Add-CMTaskSequenceStep -Step $step -InsertStepStartIndex 11
```

## PARAMETERS

### -Condition

Specify a condition object to use with this step. To get this object, use one of the task sequence condition cmdlets. For example, [Get-CMTSStepConditionVariable](Get-CMTSStepConditionVariable.md).

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

### -ImageCreator

Specify the name of the user that created the OS image. This string is stored in the image file.

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

### -ImageDescription

Specify a description of the captured OS image. This string is stored in the image file.

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

### -ImageVersion

Specify a version number to assign to the captured OS image. This value can be any combination of letters and numbers. It's stored in the image file.

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

### -Password

Specify the password for the **UserName** that has permissions to the network share.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: CapturePassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path

Specify the network path to the location that Configuration Manager uses when storing the captured OS image.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CaptureDestination

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName

Specify the username of the account that has permissions to write to the **Path** location. Also use the **Password** parameter.

For more information on this account, see [Capture OS image account](/mem/configmgr/core/plan-design/hierarchy/accounts#capture-os-image-account).

```yaml
Type: String
Parameter Sets: (All)
Aliases: CaptureUserName

Required: True
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

### None

## OUTPUTS

### IResultObject#SMS_TaskSequence_CaptureSystemImageAction

## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_CaptureSystemImageAction server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_capturesystemimageaction-server-wmi-class).

## RELATED LINKS

[Get-CMTSStepCaptureSystemImage](Get-CMTSStepCaptureSystemImage.md)
[Remove-CMTSStepCaptureSystemImage](Remove-CMTSStepCaptureSystemImage.md)
[Set-CMTSStepCaptureSystemImage](Set-CMTSStepCaptureSystemImage.md)

[About task sequence steps: Capture OS Image](/mem/configmgr/osd/understand/task-sequence-steps#BKMK_CaptureOperatingSystemImage)
