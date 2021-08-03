---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/31/2021
online version:
schema: 2.0.0
---

# Get-CMApplicationGroup

## SYNOPSIS

Get an application group.

## SYNTAX

### SearchByName (Default)
```
Get-CMApplicationGroup [[-Name] <String>] [-ShowHidden] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMApplicationGroup -Id <Int32> [-ShowHidden] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

### SearchByModelName
```
Get-CMApplicationGroup -ModelName <String> [-ShowHidden] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to get an application group. Use an application group to deploy multiple applications to a collection as a single deployment. The metadata you specify about the app group is seen in Software Center as a single entity. You can order the apps in the group so that the client installs them in a specific order. For more information, see [Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

This example gets an app group named **Central app**.

```powershell
Get-CMApplicationGroup -Name 'Central app'
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

### -Id

Specify the ID of the app group to get. This value is the same as the **CI_ID**, for example `1025866`.

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

### -ModelName

Specify the application model identifier of the app group to get. This value is also known as the **CI Unique ID**. For example, `ScopeId_0D7D8B60-F2F9-484A-B9F3-4A8B68D14D59/ApplicationGroup_047fbf05-55f4-42ab-9581-e63fd0337fed`.

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

Specify the name of the app group to get.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: LocalizedDisplayName, ApplicationGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ShowHidden

Add this parameter to show hidden application groups. A hidden app group has the **IsHidden** property set to `$true`. A hidden app group doesn't display in the Configuration Manager console, and it only returns with this cmdlet when you specify this parameter.

To hide an app group, use the following commands:



$appGroup = Get-CMApplicationGroup -Name "test app group"
$appGroup.IsHidden = $true
$appGroup.Put()

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

### None
## OUTPUTS

### IResultObject[]#SMS_ApplicationGroup
### IResultObject#SMS_ApplicationGroup
## NOTES

This cmdlet returns the **SMS_ApplicationGroup** WMI class object.

## RELATED LINKS

[New-CMApplicationGroup](New-CMApplicationGroup.md)
[Remove-CMApplicationGroup](Remove-CMApplicationGroup.md)
[Set-CMApplicationGroup](Set-CMApplicationGroup.md)

[Get-CMApplicationGroupDeployment](Get-CMApplicationGroupDeployment.md)
[New-CMApplicationGroupDeployment](New-CMApplicationGroupDeployment.md)
[Remove-CMApplicationGroupDeployment](Remove-CMApplicationGroupDeployment.md)
[Set-CMApplicationGroupDeployment](Set-CMApplicationGroupDeployment.md)

[Create application groups](/mem/configmgr/apps/deploy-use/create-app-groups)
