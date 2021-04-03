---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/26/2021
online version:
schema: 2.0.0
---

# New-CMCoManagementPolicy

## SYNOPSIS

Create a co-management policy for a site.

## SYNTAX

```
New-CMCoManagementPolicy -AutoEnroll <Boolean> [-CAWorkloadEnabled <Boolean>]
 [-ClientAppsWorkloadEnabled <Boolean>] [-CoManagementPolicyName <String>] [-DCWorkloadEnabled <Boolean>]
 [-EPWorkloadEnabled <Boolean>] [-O365WorkloadEnabled <Boolean>] [-RAWorkloadEnabled <Boolean>]
 [-WufbWorkloadEnabled <Boolean>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a co-management policy for a site. You can also switch workloads at the same time. For more information, see [How to enable co-management in Configuration Manager](/mem/configmgr/comanage/how-to-enable).

After you create this policy, use the [New-CMConfigurationPolicyDeployment](New-CMConfigurationPolicyDeployment.md) cmdlet to deploy it to a collection.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example creates a co-management policy that enables auto-enrollment, but doesn't switch any workloads. It then deploys the policy to the collection with ID **XYZ00042**.

```powershell
$CoMgmtPolicyName = "CoMgmtSettingsProd"

New-CMCoManagementPolicy -CoManagementPolicyName $CoMgmtPolicyName -AutoEnroll $true -CAWorkloadEnabled $false -RAWorkloadEnabled $false -WufbWorkloadEnabled $false -EPWorkloadEnabled $false -DCWorkloadEnabled $false -O365WorkloadEnabled $false -ClientAppsWorkloadEnabled $false

New-CMConfigurationPolicyDeployment -CoManagementPolicyName $CoMgmtPolicyName -CollectionId "XYZ00042"
```

## PARAMETERS

### -AutoEnroll

Set this parameter to **$true** to enable automatic client enrollment in Intune for existing Configuration Manager clients.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CAWorkloadEnabled

Set this parameter to **$true** to switch the **Compliance policies** workload to Intune. For more information, see [Co-management workloads](/mem/configmgr/comanage/workloads).

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

### -ClientAppsWorkloadEnabled

Set this parameter to **$true** to switch the **Client apps** workload to Intune. For more information, see [Co-management workloads](/mem/configmgr/comanage/workloads).

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

### -CoManagementPolicyName

Specify the name for the policy to create.

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

### -DCWorkloadEnabled

Set this parameter to **$true** to switch the **Device configuration** workload to Intune. For more information, see [Co-management workloads](/mem/configmgr/comanage/workloads).

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

### -EPWorkloadEnabled

Set this parameter to **$true** to switch the **Endpoint protection** workload to Intune. For more information, see [Co-management workloads](/mem/configmgr/comanage/workloads).

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

### -O365WorkloadEnabled

Set this parameter to **$true** to switch the **Office Click-to-Run apps** workload to Intune. For more information, see [Co-management workloads](/mem/configmgr/comanage/workloads).

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

### -RAWorkloadEnabled

Set this parameter to **$true** to switch the **Resource access policies** workload to Intune. For more information, see [Co-management workloads](/mem/configmgr/comanage/workloads).

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

### -WufbWorkloadEnabled

Set this parameter to **$true** to switch the **Windows Update policies** workload to Intune. For more information, see [Co-management workloads](/mem/configmgr/comanage/workloads).

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### IResultObject#SMS_ConfigurationPolicy

## NOTES

For more information on this return object and its properties, see [SMS_ConfigurationPolicy server WMI class](/mem/configmgr/develop/reference/compliance/sms_configurationpolicy-server-wmi-class).

## RELATED LINKS

[New-CMConfigurationPolicyDeployment](New-CMConfigurationPolicyDeployment.md)

[Get-CMConfigurationPolicy](Get-CMConfigurationPolicy.md)
[Remove-CMConfigurationPolicy](Remove-CMConfigurationPolicy.md)

[How to enable co-management in Configuration Manager](/mem/configmgr/comanage/how-to-enable)
[Co-management workloads](/mem/configmgr/comanage/workloads)
