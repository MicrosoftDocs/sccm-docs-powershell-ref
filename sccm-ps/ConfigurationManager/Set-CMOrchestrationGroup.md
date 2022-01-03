---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/27/2021
online version:
schema: 2.0.0
---

# Set-CMOrchestrationGroup

## SYNOPSIS

Configure an orchestration group.

## SYNTAX

### ByValue (Default)
```
Set-CMOrchestrationGroup [-InputObject] <IResultObject> [-NewName <String>] [-Description <String>]
 [-OrchestrationType <OrchestrationTypeValue>] [-OrchestrationValue <Int32>] [-OrchestrationTimeOutMin <Int32>]
 [-MaxLockTimeOutMin <Int32>] [-PreScript <String>] [-PreScriptTimeoutSec <Int32>] [-PostScript <String>]
 [-PostScriptTimeoutSec <Int32>] [-MemberResourceIds <Int32[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ById
```
Set-CMOrchestrationGroup [-Id] <Int32> [-NewName <String>] [-Description <String>]
 [-OrchestrationType <OrchestrationTypeValue>] [-OrchestrationValue <Int32>] [-OrchestrationTimeOutMin <Int32>]
 [-MaxLockTimeOutMin <Int32>] [-PreScript <String>] [-PreScriptTimeoutSec <Int32>] [-PostScript <String>]
 [-PostScriptTimeoutSec <Int32>] [-MemberResourceIds <Int32[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByName
```
Set-CMOrchestrationGroup [-Name] <String> [-NewName <String>] [-Description <String>]
 [-OrchestrationType <OrchestrationTypeValue>] [-OrchestrationValue <Int32>] [-OrchestrationTimeOutMin <Int32>]
 [-MaxLockTimeOutMin <Int32>] [-PreScript <String>] [-PreScriptTimeoutSec <Int32>] [-PostScript <String>]
 [-PostScriptTimeoutSec <Int32>] [-MemberResourceIds <Int32[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure an orchestration group.

Use orchestration groups to better control the deployment of software updates to devices. You may need to carefully manage updates for specific workloads, or automate behaviors in between. For more information, see [Create and use orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/create-orchestration-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the type and specify the sequence

This example first uses the **Get-CMOrchestrationGroup** cmdlet to get an object for the orchestration group named **IT servers**. It stores this object in the **og** variable.

The next command defines an array named **devices**. It loops through each member of the **IT servers** orchestration group (`$og.MOGMembers`), and passes the member's ID to the **Get-CMDevice** cmdlet. The returned device object is appended to the **devices** array.

The next command sorts the array by device name, and returns the device resource IDs into the **sortedIDs** variable.

It then [splats](/powershell/module/microsoft.powershell.core/about/about_splatting) the cmdlet parameters into the **parameters** variable. It's not required to splat the parameters, it just makes it easier to read the parameters for such a long command line.

The last command configures the specified orchestration group with a defined order of sequence. It's using the **MemberResourceIds** parameter to set the sequence, not add or remove members.

```powershell
$og = Get-CMOrchestrationGroup -Name "IT servers"

$devices = @()
foreach ( $id in $og.MOGMembers ) {
  $devices += Get-CMDevice -Id $id -Fast
}

$sortedIDs = ( $devices | Sort-Object -Property Name | Select-Object ResourceId ).ResourceId

$parameters = @{
  InputObject = $og
  Description = "Change type and sequence"
  OrchestrationType = "Sequence"
  MemberResourceIds = $sortedIDs
}

Set-CMOrchestrationGroup @parameters
```

This example shows how to do a programmatic sort of the existing members. If the membership of the orchestration group doesn't change, it uses the following general process:

1. Use the existing member resource IDs.
1. Get more information about each resource.
1. Sort the list on that information.
1. Return the resource IDs for the newly sorted list.

This example uses **Get-CMDevice** to get more information, but you can replace it with any cmdlet that uses the device resource ID as an input. You can also replace the sorting mechanism with another function.

### Example 2: Get script content from a file

This example uses the built-in [Get-Content](/powershell/module/microsoft.powershell.management/get-content) cmdlet to read the script text from a local file. It stores the script text in the **postScript** variable. The second command configures the orchestration group with the new post-script.

```powershell
$postScript - Get-Content -Path "D:\Scripts\OG\Post1.ps1"
Set-CMOrchestrationGroup -InputObject $og -PostScript $postScript
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

### -Id

Specify the ID of orchestration group to configure. This value is the **MOGID** property, which is an integer. For example, `16777217`.

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

### -InputObject

Specify an object for the orchestration group to configure. To get this object, use the [Get-CMOrchestrationGroup](Get-CMOrchestrationGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: ByValue
Aliases: OrchestrationGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
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

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of the orchestration group to configure.

```yaml
Type: String
Parameter Sets: ByName
Aliases: OrchestrationGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specify a new name for this orchestration group. Use this parameter to rename the orchestration group.

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

Required: False
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

### IResultObject#SMS_MachineOrchestrationGroup

## NOTES

This cmdlet returns an object for the **SMS_MachineOrchestrationGroup** WMI class.

## RELATED LINKS

[Get-CMOrchestrationGroup](Get-CMOrchestrationGroup.md)
[Invoke-CMOrchestrationGroup](Invoke-CMOrchestrationGroup.md)
[New-CMOrchestrationGroup](New-CMOrchestrationGroup.md)
[Remove-CMOrchestrationGroup](Remove-CMOrchestrationGroup.md)

[About orchestration groups in Configuration Manager](/mem/configmgr/sum/deploy-use/orchestration-groups)
