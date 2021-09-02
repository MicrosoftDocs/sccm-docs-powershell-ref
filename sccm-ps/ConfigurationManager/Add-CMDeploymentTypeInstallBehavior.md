---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
online version:
schema: 2.0.0
---

# Add-CMDeploymentTypeInstallBehavior

## SYNOPSIS

Add to the specified deployment type the executable files that need to close for the app install to succeed.

## SYNTAX

```
Add-CMDeploymentTypeInstallBehavior -InputObject <IResultObject> -ExeFileName <String> [-DisplayName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to add to the specified application deployment type the executable files that need to close for the app install to succeed. For more general information on the install behavior feature, see [Check for running executable files](/mem/configmgr/apps/deploy-use/check-for-running-executable-files).

If you use PowerShell to deploy the application, use the **AutoCloseExecutable** parameter on either [New-CMApplicationDeployment](New-CMApplicationDeployment.md) or [Set-CMApplicationDeployment](Set-CMApplicationDeployment.md). This parameter enables the application deployment setting for install behaviors.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add notepad is closed for a deployment type

This example works with the deployment type object for the **CenterApp** application. It adds **notepad.exe** as an executable file that needs to be closed for the deployment type to run.

```powershell
$appName = "CenterApp"
$dtName = "InterDept - Windows Installer (.msi file)"
$msi_dt = Get-CMDeploymentType -ApplicationName $appName -DeploymentTypeName $dtName
Add-CMDeploymentTypeInstallBehavior -InputObject $msi_dt -ExeFileName "notepad.exe" -DisplayName "Notepad"
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

### -DisplayName

Specify a friendly name for the application to help you identify it.

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

### -ExeFileName

Specify the name of the target executable file. The Configuration Manager client checks if this file name is running.

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

Specify an application deployment type object to add this setting. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

### IResultObject#SMS_Application

## NOTES

For more information on this return object and its properties, see [SMS_Application server WMI class](/mem/configmgr/develop/reference/apps/sms_application-server-wmi-class).

## RELATED LINKS

[Get-CMDeploymentTypeInstallBehavior](Get-CMDeploymentTypeInstallBehavior.md)
[Remove-CMDeploymentTypeInstallBehavior](Remove-CMDeploymentTypeInstallBehavior.md)
[Set-CMDeploymentTypeInstallBehavior](Set-CMDeploymentTypeInstallBehavior.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)
