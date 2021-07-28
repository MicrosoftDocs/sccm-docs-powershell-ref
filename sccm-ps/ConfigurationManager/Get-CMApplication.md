---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/31/2021
schema: 2.0.0
title: Get-CMApplication
---

# Get-CMApplication

## SYNOPSIS

Get an application.

## SYNTAX

### SearchByName (Default)
```
Get-CMApplication [-Fast] [[-Name] <String>] [-ShowHidden] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMApplication [-Fast] -Id <Int32> [-ShowHidden] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByDeploymentType
```
Get-CMApplication [-Fast] -InputObject <IResultObject> [-ShowHidden] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByModelName
```
Get-CMApplication [-Fast] -ModelName <String> [-ShowHidden] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get a Configuration Manager application. A Configuration Manager application defines the metadata about app. An application has one or more deployment types. These deployment types include the installation files and information that are required to install software on devices. A deployment type also has rules, such as detection methods and requirements. These rules specify when and how the client installs the software.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get an application by name

This command gets the application object named **Application1**.

```powershell
Get-CMApplication -Name "Application1"
```

### Example 2: Get the application for a deployment type

The first command gets the deployment type object named **DT2** for the application named **Application1** and stores the object in the **$DeploymentType** variable. The second command uses the pipeline operator to pass the deployment type stored in **$DeploymentType** to **Get-CMApplication**, which gets the application for the deployment type.

```powershell
$DeploymentType = Get-CMDeploymentType -DeploymentTypeName "DT2" -ApplicationName "Application1"
$DeploymentType | Get-CMApplication
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

### -Id

Specify the **CI_ID** of an application to get. For example, `136846`.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a deployment type object to get the associated application. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByDeploymentType
Aliases: DeploymentType

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ModelName

Specify the **ModelID** of an application to get. For example, `136846`.

```yaml
Type: String
Parameter Sets: SearchByModelName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

Specify the name of an application to get.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName, ApplicationName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ShowHidden

Add this parameter to show hidden applications. A hidden application has the **IsHidden** property set to `$true`. A hidden app doesn't display in the Configuration Manager console, and it only returns with this cmdlet when you specify this parameter.

To hide an application, use the following commands:



$app = Get-CMApplication -Name "test app"
$app.IsHidden = $true
$app.Put()

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

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### IResultObject[]#SMS_ApplicationLatest
### IResultObject#SMS_ApplicationLatest
### IResultObject#SMS_Application
## NOTES

For more information on these return object and their properties, see the following articles:

- [SMS_Application server WMI class](/mem/configmgr/develop/reference/apps/sms_application-server-wmi-class)
- [SMS_ApplicationLatest server WMI class](/mem/configmgr/develop/reference/apps/sms_applicationlatest-server-wmi-class)

## RELATED LINKS

[Convert-CMApplication](Convert-CMApplication.md)

[ConvertFrom-CMApplication](ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](ConvertTo-CMApplication.md)

[Export-CMApplication](Export-CMApplication.md)

[Import-CMApplication](Import-CMApplication.md)

[New-CMApplication](New-CMApplication.md)

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Set-CMApplication](Set-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)
