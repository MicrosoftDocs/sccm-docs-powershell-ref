---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/27/2021
online version:
schema: 2.0.0
---

# New-CMOrchestrationGroup

## SYNOPSIS

Create a new orchestration group.

## SYNTAX

```
New-CMOrchestrationGroup [-Name] <String> -SiteCode <String> [-Description <String>]
 -OrchestrationType <OrchestrationTypeValue> [-OrchestrationValue <Int32>] [-OrchestrationTimeOutMin <Int32>]
 [-MaxLockTimeOutMin <Int32>] [-PreScript <String>] [-PreScriptTimeoutSec <Int32>] [-PostScript <String>]
 [-PostScriptTimeoutSec <Int32>] -MemberResourceIds <Int32[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a new orchestration group.

Use orchestration groups to better control the deployment of software updates to devices. You may need to carefully manage updates for specific workloads, or automate behaviors in between. For more information, see [Create and use orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/create-orchestration-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example first [splats](/powershell/module/microsoft.powershell.core/about/about_splatting) the cmdlet parameters into the **parameters** variable. It's not required to splat the parameters, it just makes it easier to read the parameters for such a long command line.

It assumes that you have objects for the devices to add to the orchestration group in the **device** variables.

The command creates an orchestration group with the default settings and simple scripts for testing purposes.

```powershell
$parameters = @{
  Name = "IT servers"
  SiteCode = "XYZ"
  Description = "An OG for IT servers with default settings"
  OrchestrationType = "Number"
  OrchestrationValue = 1
  OrchestrationTimeOutMin = 720
  MaxLockTimeOutMin = 60
  PreScript = "Write-Host 'Pre-install script'"
  PreScriptTimeoutSec = 120
  PostScript = "Write-Host 'POST-install script'"
  PostScriptTimeoutSec = 120
  MemberResourceIds = $device1.ResourceID, $device2.ResourceID
}

New-CMOrchestrationGroup @parameters
```

## PARAMETERS

### -Description

Specify an optional description for the orchestration group to help identify it.

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

### -MaxLockTimeOutMin

Specify an integer value for the orchestration group member timeout in minutes. This value is the time limit for a single device in the group to install the updates.

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

### -MemberResourceIds

Specify an array of resource IDs for the devices to add as members of this orchestration group. The resource ID is an integer, for example, `16777220`. It's the **ResourceId** property on a device or resource object. To get a device object, use the [Get-CMDevice](Get-CMDevice.md) or [Get-CMResource](Get-CMResource.md) cmdlets.

When you set the **OrchestrationType** parameter to `Sequence`, use this parameter to determine the order.

```yaml
Type: Int32[]
Parameter Sets: (All)
Aliases: MogMembers

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify a name for the orchestration group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: OrchestrationGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrchestrationTimeOutMin

Specify an integer value for the orchestration group timeout in minutes. This value is the time limit for all group members to install the updates.

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

### -OrchestrationType

Specify one of the following values for the type of orchestration group:

- `Number`: Allow a number of the devices to update at the same time. Use this setting to always limit to a specific number of devices, whatever the overall size of the orchestration group. To specify the number of devices, use the **OrchestrationValue** parameter.

- `Percentage`: Allow a percentage of the devices to update at the same time. Use this setting to allow for future flexibility of the size of the orchestration group. To specify the percentage, use the **OrchestrationValue** parameter.

- `Sequence`: Explicitly define the order in which devices run the software update deployment. The order is determined by the sort of the device resource IDs in the **MemberResourceIds** parameter.

```yaml
Type: OrchestrationTypeValue
Parameter Sets: (All)
Aliases:
Accepted values: Number, Percentage, Sequence

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OrchestrationValue

Specify an integer for the number or percentage of devices to update at the same time. Use this parameter when you set the **OrchestrationType** parameter to `Number` or `Percentage`.

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

### -PostScript

Specify the PowerShell script to run on each device _after_ the deployment runs and the device restarts, if required.

This string value is the text of the script itself. If you have a script in a file that you want to use, first read it into a variable. For example, use the built-in [Get-Content](/powershell/module/microsoft.powershell.management/get-content) cmdlet.

The scripts should return a value of `0` for success. Any non-zero value is considered a script failure. You can't use a script with parameters. The maximum script length is 50,000 characters.

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

### -PostScriptTimeoutSec

Specify the integer value for the allowed time in seconds for the post-script to run before it times out.

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

### -PreScript

Specify the PowerShell script to run on each device _before_ the deployment runs.

This string value is the text of the script itself. If you have a script in a file that you want to use, first read it into a variable. For example, use the built-in [Get-Content](/powershell/module/microsoft.powershell.management/get-content) cmdlet.

The scripts should return a value of `0` for success. Any non-zero value is considered a script failure. You can't use a script with parameters. The maximum script length is 50,000 characters.

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

### -PreScriptTimeoutSec

Specify the integer value for the allowed time in seconds for the pre-script to run before it times out.

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

### -SiteCode

Specify the site code for this orchestration group and its members.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
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

### None

## OUTPUTS

### IResultObject#SMS_MachineOrchestrationGroup

## NOTES

This cmdlet returns an object for the **SMS_MachineOrchestrationGroup** WMI class.

## RELATED LINKS

[Get-CMOrchestrationGroup](Get-CMOrchestrationGroup.md)
[Invoke-CMOrchestrationGroup](Invoke-CMOrchestrationGroup.md)
[Remove-CMOrchestrationGroup](Remove-CMOrchestrationGroup.md)
[Set-CMOrchestrationGroup](Set-CMOrchestrationGroup.md)

[About orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/orchestration-groups)
