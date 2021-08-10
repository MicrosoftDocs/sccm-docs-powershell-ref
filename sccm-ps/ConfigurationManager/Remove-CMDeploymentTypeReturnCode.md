---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 07/28/2021
online version:
schema: 2.0.0
---

# Remove-CMDeploymentTypeReturnCode

## SYNOPSIS

Delete return codes from the specified application deployment type.

## SYNTAX

### SearchByReturnCode (Default)
```
Remove-CMDeploymentTypeReturnCode -InputObject <IResultObject> [-ReturnCode <Int32>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByName
```
Remove-CMDeploymentTypeReturnCode -InputObject <IResultObject> [-Name <String>] [-Force]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Starting in version 2107, use this cmdlet to delete return codes from the specified application deployment type. For more general information, see [Deployment type Return Codes](/mem/configmgr/apps/deploy-use/create-applications#bkmk_dt-return).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Remove the 1602 return code from a deployment type

This example removes the `1602` return code from a deployment type of the **CenterApp** application.

```powershell
$appName = "CenterApp"
$dtName = "InterDept - Windows Installer (.msi file)"
$msi_dt = Get-CMDeploymentType -ApplicationName $appName -DeploymentTypeName $dtName

Remove-CMDeploymentTypeReturnCode -InputObject $msi_dt -ReturnCode 1602
```

## PARAMETERS

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

Specify a deployment type object from which to remove a return code. To get this object, use the [Get-CMDeploymentType](Get-CMDeploymentType.md) cmdlet.

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

### -Name

Specify the name of a return code to remove.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ReturnCodeName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReturnCode

Specify the integer value of the return code to remove.

```yaml
Type: Int32
Parameter Sets: SearchByReturnCode
Aliases: ReturnCodeValue

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

[Add-CMDeploymentTypeReturnCode](Add-CMDeploymentTypeReturnCode.md)
[Get-CMDeploymentTypeReturnCode](Get-CMDeploymentTypeReturnCode.md)
[Set-CMDeploymentTypeReturnCode](Set-CMDeploymentTypeReturnCode.md)

[Get-CMDeploymentType](Get-CMDeploymentType.md)
