---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
schema: 2.0.0
title: New-CMSoftwareUpdateDeploymentPackage
---

# New-CMSoftwareUpdateDeploymentPackage

## SYNOPSIS

Create a software update deployment package.

## SYNTAX

```
New-CMSoftwareUpdateDeploymentPackage [-Description <String>] [-Fast] -Name <String> -Path <String>
 [-Priority <Priorities>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to create a software update deployment package. A software update deployment package object contains one or more software updates. For more information, see [Plan software update content](/mem/configmgr/sum/plan-design/plan-for-software-updates#bkmk_content).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Create a deployment package

This example first uses the built-in [Get-Date](/powershell/module/microsoft.powershell.utility/get-date) cmdlet.
It then creates a deployment package using the date string in the name and the path.

```powershell
$date = Get-Date -Format "yyyy-MM-dd"

New-CMSoftwareUpdateDeploymentPackage -Name "Updates for $date" -Path "\\gold\sources\updates\$date"
```

## PARAMETERS

### -Description

Specify an optional description for the deployment package to help identify it.

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

Specify the name for the deployment package.

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

### -Path

Specify the path of a network share to use as the package source for this software update deployment package.

```yaml
Type: String
Parameter Sets: (All)
Aliases: PackageSourcePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Priority

Specify the distribution priority for this deployment package. The site uses this priority to determine the order in which packages are sent to other sites and the distribution points in the same site.

```yaml
Type: Priorities
Parameter Sets: (All)
Aliases:
Accepted values: High, Normal, Low

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

### None

## OUTPUTS

### IResultObject#SMS_SoftwareUpdatesPackage

## NOTES

For more information on this return object and its properties, see [SMS_SoftwareUpdatesPackage server WMI class](/mem/configmgr/develop/reference/sum/sms_softwareupdatespackage-server-wmi-class).

## RELATED LINKS

[Get-CMSoftwareUpdateDeploymentPackage](Get-CMSoftwareUpdateDeploymentPackage.md)

[Remove-CMSoftwareUpdateDeploymentPackage](Remove-CMSoftwareUpdateDeploymentPackage.md)

[Set-CMSoftwareUpdateDeploymentPackage](Set-CMSoftwareUpdateDeploymentPackage.md)

[Save-CMSoftwareUpdate](Save-CMSoftwareUpdate.md)
