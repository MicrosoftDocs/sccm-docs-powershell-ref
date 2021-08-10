---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
online version:
schema: 2.0.0
---

# Get-CMDeploymentTypeInstallBehavior

## SYNOPSIS

Get from the specified deployment type the list of executable files that need to close for the app install to succeed.

## SYNTAX

```
Get-CMDeploymentTypeInstallBehavior -InputObject <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to get from the specified application deployment type the list of executable files that need to close for the app install to succeed. For more general information on the install behavior feature, see [Check for running executable files](/mem/configmgr/apps/deploy-use/check-for-running-executable-files).

If you use PowerShell to deploy the application, use the **AutoCloseExecutable** parameter on either [New-CMApplicationDeployment](New-CMApplicationDeployment.md) or [Set-CMApplicationDeployment](Set-CMApplicationDeployment.md). This parameter enables the application deployment setting for install behaviors.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get the install behaviors for a specific deployment type

This example lists the install behaviors for an MSI deployment type of the **CenterApp** application.

```powershell
$appName = "CenterApp"
$dtName = "InterDept - Windows Installer (.msi file)"
$msi_dt = Get-CMDeploymentType -ApplicationName $appName -DeploymentTypeName $dtName
Get-CMDeploymentTypeInstallBehavior -InputObject $msi_dt
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

### -InputObject

Specify an application deployment type object. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### ProcessInformation[]

### ProcessInformation

## NOTES

## RELATED LINKS

[Add-CMDeploymentTypeInstallBehavior](Add-CMDeploymentTypeInstallBehavior.md)
[Remove-CMDeploymentTypeInstallBehavior](Remove-CMDeploymentTypeInstallBehavior.md)
[Set-CMDeploymentTypeInstallBehavior](Set-CMDeploymentTypeInstallBehavior.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)
