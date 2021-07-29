---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
online version:
schema: 2.0.0
---

# Get-CMDeploymentTypeReturnCode

## SYNOPSIS

Get the list of return codes from the specified application deployment type.

## SYNTAX

```
Get-CMDeploymentTypeReturnCode -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to get the list of return codes from the specified application deployment type. For more general information, see [Deployment type Return Codes](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-return).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: List the return codes for the specified deployment type

The following example lists all of the return codes for a deployment type of the **CenterApp** application, and formats them in a table.

```powershell
$appName = "CenterApp"
$dtName = "InterDept - Windows Installer (.msi file)"
Get-CMDeploymentType -ApplicationName $appName -DeploymentTypeName $dtName | Get-CMDeploymentTypeReturnCode | Format-Table
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

Specify a deployment type object for which to view the return codes. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

### ExitCode[]

### ExitCode

## NOTES

## RELATED LINKS

[Add-CMDeploymentTypeReturnCode](Add-CMDeploymentTypeReturnCode.md)
[Remove-CMDeploymentTypeReturnCode](Remove-CMDeploymentTypeReturnCode.md)
[Set-CMDeploymentTypeReturnCode](Set-CMDeploymentTypeReturnCode.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)
