---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
online version:
schema: 2.0.0
---

# Set-CMDeploymentTypeInstallBehavior

## SYNOPSIS

Modify the executable files that need to close for the app install to succeed.

## SYNTAX

```
Set-CMDeploymentTypeInstallBehavior -InputObject <IResultObject> -ExeFileName <String>
 [-NewExeFileName <String>] [-DisplayName <String>] [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to modify the executable files that need to close for the app install to succeed. For more general information on the install behavior feature, see [Check for running executable files](/mem/configmgr/apps/deploy-use/check-for-running-executable-files).

If you use PowerShell to deploy the application, use the **AutoCloseExecutable** parameter on either [New-CMApplicationDeployment](New-CMApplicationDeployment.md) or [Set-CMApplicationDeployment](Set-CMApplicationDeployment.md). This parameter enables the application deployment setting for install behaviors.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change the executable file install behavior

This example changes the executable file that's checked on the **CenterApp** application from **notepad.exe** to **calc.exe**.

```powershell
$appName = "CenterApp"
$dtName = "InterDept - Windows Installer (.msi file)"
$msi_dt = Get-CMDeploymentType -ApplicationName $appName -DeploymentTypeName $dtName
Set-CMDeploymentTypeInstallBehavior -InputObject $msi_dt -ExeFileName "notepad.exe" -NewExeFileName "calc.exe" -DisplayName "Calculator"
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

Specify a friendly name for the specified executable to help you identify it.

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

Specify the name of the target executable file. To change this executable file, use the **NewExeFileName** parameter. To change the friendly name, use the **DisplayName** parameter.

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

Specify an application deployment type object to modify this setting. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

### -NewExeFileName

Specify the name of the new target executable file. The Configuration Manager client checks if this file name is running.

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

### IResultObject#SMS_Application

## NOTES

For more information on this return object and its properties, see [SMS_Application server WMI class](/mem/configmgr/develop/reference/apps/sms_application-server-wmi-class).

## RELATED LINKS

[Add-CMDeploymentTypeInstallBehavior](Add-CMDeploymentTypeInstallBehavior.md)
[Get-CMDeploymentTypeInstallBehavior](Get-CMDeploymentTypeInstallBehavior.md)
[Remove-CMDeploymentTypeInstallBehavior](Remove-CMDeploymentTypeInstallBehavior.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)
