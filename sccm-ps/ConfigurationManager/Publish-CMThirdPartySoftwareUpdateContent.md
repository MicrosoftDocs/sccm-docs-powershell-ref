---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 03/25/2021
online version:
schema: 2.0.0
---

# Publish-CMThirdPartySoftwareUpdateContent

## SYNOPSIS

Publish third-party software update content

## SYNTAX

### SetById (Default)
```
Publish-CMThirdPartySoftwareUpdateContent -CIId <Int32[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValue
```
Publish-CMThirdPartySoftwareUpdateContent -InputObject <IResultObject[]> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Publish-CMThirdPartySoftwareUpdateContent -Name <String[]> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to publish third-party software update content. When you publish an update, the binary files are downloaded from the vendor and placed into the `WSUSContent` directory on the top-level software update point. For more information, see [Publish and deploy third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates#publish-and-deploy-third-party-software-updates).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Get and publish a third-party update

```powershell
Get-CMSoftwareUpdate -Name "third-party update" | Publish-CMThirdPartySoftwareUpdateContent
```

## PARAMETERS

### -CIId

Specify one or more **CI_ID**s for updates to publish.

```yaml
Type: Int32[]
Parameter Sets: SetById
Aliases: CI_ID, CIIds, CI_IDs

Required: True
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

Specify a software update object for a third-party update to publish. To get this object, use the [Get-CMSoftwareUpdate](Get-CMSoftwareUpdate.md) cmdlet.

```yaml
Type: IResultObject[]
Parameter Sets: SetByValue
Aliases: SoftwareUpdate, SoftwareUpdates

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name

Specify the name of one or more updates to publish.

```yaml
Type: String[]
Parameter Sets: SetByName
Aliases: LocalizedDisplayName, LocalizedDisplayNames, Names

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject[]
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMThirdPartyUpdateCatalog](Get-CMThirdPartyUpdateCatalog.md)
[New-CMThirdPartyUpdateCatalog](New-CMThirdPartyUpdateCatalog.md)
[Remove-CMThirdPartyUpdateCatalog](Remove-CMThirdPartyUpdateCatalog.md)
[Set-CMThirdPartyUpdateCatalog](Set-CMThirdPartyUpdateCatalog.md)

[Get-CMThirdPartyUpdateCategory](Get-CMThirdPartyUpdateCategory.md)
[Set-CMThirdPartyUpdateCategory](Set-CMThirdPartyUpdateCategory.md)

[Enable third-party software updates](/mem/configmgr/sum/deploy-use/third-party-software-updates)
