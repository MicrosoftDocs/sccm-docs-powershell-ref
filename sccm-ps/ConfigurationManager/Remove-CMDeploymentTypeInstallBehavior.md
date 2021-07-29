---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
online version:
schema: 2.0.0
---

# Remove-CMDeploymentTypeInstallBehavior

## SYNOPSIS

Remove from the specified deployment type the executable files that need to close for the app install to succeed.

## SYNTAX

### SearchByExeFileName (Default)
```
Remove-CMDeploymentTypeInstallBehavior -InputObject <IResultObject> [-ExeFileName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByDisplayName
```
Remove-CMDeploymentTypeInstallBehavior -InputObject <IResultObject> [-DisplayName <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to remove from the specified application deployment type the executable files that need to close for the app install to succeed. For more general information on the install behavior feature, see [Check for running executable files](/mem/configmgr/apps/deploy-use/check-for-running-executable-files).

If you use PowerShell to deploy the application, use the **AutoCloseExecutable** parameter on either [New-CMApplicationDeployment](New-CMApplicationDeployment.md) or [Set-CMApplicationDeployment](Set-CMApplicationDeployment.md). This parameter enables the application deployment setting for install behaviors.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove an executable file as an install behavior

This example removes **notepad.exe** from the install behavior list on the **CenterApp** application.

```powershell
$appName = "CenterApp"
$dtName = "InterDept - Windows Installer (.msi file)"
$msi_dt = Get-CMDeploymentType -ApplicationName $appName -DeploymentTypeName $dtName
Remove-CMDeploymentTypeInstallBehavior -InputObject $msi_dt -ExeFileName "notepad.exe"
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

Specify the friendly name of the install behavior to remove.

```yaml
Type: String
Parameter Sets: SearchByDisplayName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExeFileName

Specify the name of the executable file to remove from the application deployment type.

```yaml
Type: String
Parameter Sets: SearchByExeFileName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force

Run the command without asking for confirmation.

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

[Add-CMDeploymentTypeInstallBehavior](Add-CMDeploymentTypeInstallBehavior.md)
[Get-CMDeploymentTypeInstallBehavior](Get-CMDeploymentTypeInstallBehavior.md)
[Set-CMDeploymentTypeInstallBehavior](Set-CMDeploymentTypeInstallBehavior.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)

[Set-CMApplicationDeployment](Set-CMApplicationDeployment.md)
