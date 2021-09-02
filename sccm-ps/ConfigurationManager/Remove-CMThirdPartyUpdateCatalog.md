---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Remove-CMThirdPartyUpdateCatalog

## SYNOPSIS

Remove a third-party software updates catalog.

## SYNTAX

### SearchByName (Default)
```
Remove-CMThirdPartyUpdateCatalog [-Force] [[-Name] <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMThirdPartyUpdateCatalog [-Force] [-Id] <String> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMThirdPartyUpdateCatalog [-Force] [-InputObject] <IResultObject> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to remove a third-party software updates catalog. For more information, see [Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Force remove the catalog by name

This example force removes the third-party update catalog by its name.

```powershell
Remove-CMThirdPartyUpdateCatalog -Name "Contoso updates catalog" -Force
```

### Example 2: Remove the catalog as an object

This example removes the third-party update catalog as an object.

```powershell
$catalog = Get-CMThirdPartyUpdateCatalog -Name "Contoso updates catalog"
Remove-CMThirdPartyUpdateCatalog -ThirdPartyUpdateCatalog $catalog
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

### -Force

Force remove the third-party updates catalog.

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

This parameter processes wildcard characters and may lead to unexpected behavior. It's not recommended. You can't combine it with **DisableWildcardHandling**.

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

Specify the ID of the third-party updates catalog.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CatalogId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify an object for the third-party updates catalog. To get this object, use the [Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: ThirdPartyUpdateCatalog

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of the third-party updates catalog.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: CatalogName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
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

[Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md)
[New-CMThirdPartyUpdateCatalog](New-CMThirdPartyUpdateCatalog.md)
[Set-CMThirdPartyUpdateCatalog](Set-CMThirdPartyUpdateCatalog.md)

[Publish-CMThirdPartySoftwareUpdateContent](Publish-CMThirdPartySoftwareUpdateContent.md)

[Get-CMThirdPartyUpdateCategory](Get-CMThirdPartyUpdateCategory.md)
[Set-CMThirdPartyUpdateCategory](Set-CMThirdPartyUpdateCategory.md)

[Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates)
