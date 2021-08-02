---
description: Get a task sequence.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/24/2021
schema: 2.0.0
title: Get-CMTaskSequence
---

# Get-CMTaskSequence

## SYNOPSIS

Get a task sequence.

## SYNTAX

### SearchByName (Default)
```
Get-CMTaskSequence [-Fast] [-Name <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMTaskSequence [-Fast] -TaskSequencePackageId <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a Configuration Manager task sequence. You typically use a task sequence to deploy an OS to a client, but you can use them for various purposes. To create a task sequence, use the [New-CMTaskSequence](New-CMTaskSequence.md) cmdlet, or the Configuration Manager console. For more information, see [Manage task sequences to automate tasks](/mem/configmgr/osd/deploy-use/manage-task-sequences-to-automate-tasks).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get a task sequence by name

This command gets the task sequence named **Upgrade to Windows 10 latest**.

```powershell
Get-CMTaskSequence -Name "Upgrade to Windows 10 latest"
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

### -Name

Specify the name of a task sequence to get.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -TaskSequencePackageId

Specify the package ID of the task sequence to get. This value is a standard package ID, for example, `XYZ007C0`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: PackageId, Id

Required: True
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

### IResultObject[]#SMS_TaskSequence_Step
### IResultObject#SMS_TaskSequence_Step
## NOTES

For more information on this return object and its properties, see [SMS_TaskSequence_Step server WMI class](/mem/configmgr/develop/reference/osd/sms_tasksequence_step-server-wmi-class).

## RELATED LINKS

[New-CMTaskSequence](New-CMTaskSequence.md)
[Set-CMTaskSequence](Set-CMTaskSequence.md)
[Copy-CMTaskSequence](Copy-CMTaskSequence.md)
[Import-CMTaskSequence](Import-CMTaskSequence.md)
[Export-CMTaskSequence](Export-CMTaskSequence.md)
[Remove-CMTaskSequence](Remove-CMTaskSequence.md)

[Manage task sequences to automate tasks](/mem/configmgr/osd/deploy-use/manage-task-sequences-to-automate-tasks)
