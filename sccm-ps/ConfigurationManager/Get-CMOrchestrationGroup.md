---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/27/2021
online version:
schema: 2.0.0
---

# Get-CMOrchestrationGroup

## SYNOPSIS

Get an orchestration group object.

## SYNTAX

### ByName (Default)
```
Get-CMOrchestrationGroup [[-Name] <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### ById
```
Get-CMOrchestrationGroup [-Id] <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get an orchestration group object by name or ID. You can use this object to start, remove, or configure the orchestration group. For these other actions, use the following cmdlets:

- [Invoke-CMOrchestrationGroup](invoke-cmorchestrationgroup.md)
- [Remove-CMOrchestrationGroup](remove-cmorchestrationgroup.md)
- [Set-CMOrchestrationGroup](set-cmorchestrationgroup.md)

Use orchestration groups to better control the deployment of software updates to devices. You may need to carefully manage updates for specific workloads, or automate behaviors in between. For more information, see [About orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/orchestration-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: View details about members of an orchestration group

This example first uses the **Get-CMOrchestrationGroup** cmdlet to get an object for the orchestration group named **IT servers**.

It then loops through each member of the orchestration group, which is stored by its resource ID. It then uses the **Get-CMDevice** cmdlet to display the device name and OS build properties.

```powershell
$og = Get-CMOrchestrationGroup -Name "IT servers"

foreach ( $member in $og.MOGMembers ) {
  Get-CMDevice -Id $member -Fast | Select-Object Name, Build
}
```

### Example 2: Get orchestration groups with unapproved scripts

The following example gets all orchestration groups from the site. It uses the built-in [Where-Object](/powershell/module/microsoft.powershell.core/where-object) cmdlet to filter the results that have either of the script approval state properties with a value of `0`. It uses the pipeline operator again to reduce the returned properties with the built-in [Select-Object](/powershell/module/microsoft.powershell.utility/select-object) cmdlet to only display the name of the orchestration groups.

You can use this example to display all orchestration groups that have either a pre- or post-script that's not approved.

```powershell
Get-CMOrchestrationGroup | Where-Object ( $_.PostScriptApprovalState -eq $false -or $_.PreScriptApprovalState -eq $false ) | Select-Object Name
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

Specify the ID of orchestration group to get. This value is the **MOGID** property, which is an integer. For example, `16777217`.

```yaml
Type: Int32
Parameter Sets: ById
Aliases: MOGID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the orchestration group to get.

```yaml
Type: String
Parameter Sets: ByName
Aliases: OrchestrationGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_MachineOrchestrationGroup

## NOTES

This cmdlet returns an object for the **SMS_MachineOrchestrationGroup** WMI class.

## RELATED LINKS

[Invoke-CMOrchestrationGroup](Invoke-CMOrchestrationGroup.md)
[New-CMOrchestrationGroup](New-CMOrchestrationGroup.md)
[Remove-CMOrchestrationGroup](Remove-CMOrchestrationGroup.md)
[Set-CMOrchestrationGroup](Set-CMOrchestrationGroup.md)

[About orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/orchestration-groups)
