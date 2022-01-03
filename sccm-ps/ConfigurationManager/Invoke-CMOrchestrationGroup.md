---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/27/2021
online version:
schema: 2.0.0
---

# Invoke-CMOrchestrationGroup

## SYNOPSIS

Start orchestration on an orchestration group.

## SYNTAX

### SearchByIdMandatory (Default)
```
Invoke-CMOrchestrationGroup -Id <Int32> [-IgnoreServiceWindow <Boolean>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Invoke-CMOrchestrationGroup -InputObject <IResultObject> [-IgnoreServiceWindow <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Invoke-CMOrchestrationGroup -Name <String> [-IgnoreServiceWindow <Boolean>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to start orchestration on an orchestration group.

For more information, see [Start orchestration](/mem/configmgr/sum/deploy-use/create-orchestration-groups#start-orchestration).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first gets an object for the orchestration group named **IT servers**. It then passes that object through the pipeline to the Invoke-CMOrchestrationGroup cmdlet. It immediately starts the installation and bypasses any maintenance windows.

```powershell
Get-CMOrchestrationGroup -Name "IT servers" | Invoke-CMOrchestrationGroup -IgnoreServiceWindow $true
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

### -Id

Specify the ID of orchestration group to start. This value is the **MOGID** property, which is an integer. For example, `16777217`.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: MOGId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreServiceWindow

Set this parameter to `$true` to start the installation immediately and bypass maintenance windows.

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

### -InputObject

Specify an object for the orchestration group to start. To get this object, use the [Get-CMOrchestrationGroup](Get-CMOrchestrationGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: OrchestrationGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the orchestration group to start.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: OrchestrationGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Get-CMOrchestrationGroup](Get-CMOrchestrationGroup.md)
[New-CMOrchestrationGroup](New-CMOrchestrationGroup.md)
[Remove-CMOrchestrationGroup](Remove-CMOrchestrationGroup.md)
[Set-CMOrchestrationGroup](Set-CMOrchestrationGroup.md)

[About orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/orchestration-groups)
