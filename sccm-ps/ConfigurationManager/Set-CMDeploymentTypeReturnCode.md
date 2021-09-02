---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
online version:
schema: 2.0.0
---

# Set-CMDeploymentTypeReturnCode

## SYNOPSIS

Modify return codes for the specified application deployment type.

## SYNTAX

```
Set-CMDeploymentTypeReturnCode -InputObject <IResultObject> -ReturnCode <Int32> [-CodeType <ExitCodeClass>]
 [-NewName <String>] [-Description <String>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to modify return codes for the specified application deployment type. For more general information, see [Deployment type Return Codes](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-return).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Modify the behavior of the 3010 return code

This example modifies the behavior of the default `3010` return code, which is the **Soft Reboot** type by default. It configures it as a **Hard Reboot** and changes the name and description.

```powershell
$appName = "CenterApp"
$dtName = "InterDept - Windows Installer (.msi file)"
$msi_dt = Get-CMDeploymentType -ApplicationName $appName -DeploymentTypeName $dtName

Add-CMDeploymentTypeReturnCode -InputObject $msi_dt -ReturnCode 3010 -Name "Always reboot" -CodeType HardReboot -Description "Change soft reboot to hard reboot"
```

## PARAMETERS

### -CodeType

Specify the type of return code. This setting defines how Configuration Manager interprets the specified return code from this deployment type. The available types vary based on the deployment type technology.

- `Failure`: The deployment type failed to install.

- `Success`: The deployment type successfully installed, and no reboot is necessary.

- `FastRetry`: Another installation is already in progress on the device. The client retries every two hours, for a total of 10 times.

- `HardReboot`: The deployment type successfully installed, but requires the device to restart. Nothing else can be installed until the device restarts.

- `SoftReboot`: The deployment type successfully installed, but requests the device to restart. Other installations can occur before the device restarts.

```yaml
Type: ExitCodeClass
Parameter Sets: (All)
Aliases:
Accepted values: Failure, Success, FastRetry, HardReboot, SoftReboot

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description

Specify an optional description to help you identify and describe this return code.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReturnCodeDescription

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

### -InputObject

Specify a deployment type object on which to modify the return code. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

### -NewName

Specify a new name to describe this return code.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ReturnCodeName

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

### -ReturnCode

Specify an integer value for the return code that you expect from this deployment type. This value is any positive or negative integer between `-2147483648` and `2147483647`.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ReturnCodeValue

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject

## OUTPUTS

### IResultObject#SMS_Application

## NOTES

For more information on this return object and its properties, see [SMS_Application server WMI class](/mem/configmgr/develop/reference/apps/sms_application-server-wmi-class).

## RELATED LINKS

[Add-CMDeploymentTypeReturnCode](Add-CMDeploymentTypeReturnCode.md)
[Get-CMDeploymentTypeReturnCode](Get-CMDeploymentTypeReturnCode.md)
[Remove-CMDeploymentTypeReturnCode](Remove-CMDeploymentTypeReturnCode.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)
