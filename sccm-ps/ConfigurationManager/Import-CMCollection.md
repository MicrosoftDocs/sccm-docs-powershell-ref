---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2021
schema: 2.0.0
title: Import-CMCollection
---

# Import-CMCollection

## SYNOPSIS

Import a collection.

## SYNTAX

```
Import-CMCollection [-ImportFilePath] <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to import a previously exported collection from a managed object format (`.mof`) file.

You can use this export/import process to backup custom collections, or for development lifecycle. For example, you develop a new collection in a lab environment. Export the collection from the test environment, and then import it into the production hierarchy.

For more information, see [How to manage collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/manage-collections).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import a collection

This command imports the collection from the **collection.mof** file.

```powershell
Import-CMCollection -ImportFilePath "c:\path\collection.mof"
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

### -ImportFilePath

Specify the full path of the MOF file for the collection to import.

You can't import from a file that defines a collection that already exists. For example, if you export the **All Systems** collection, you can't import it. The cmdlet returns the following error: `An object with the specified name already exists.`

```yaml
Type: String
Parameter Sets: (All)
Aliases: FileName, FilePath, Path

Required: True
Position: 0
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object

## NOTES

## RELATED LINKS

[Copy-CMCollection](Copy-CMCollection.md)
[Export-CMCollection](Export-CMCollection.md)
[Get-CMCollection](Get-CMCollection.md)
[Get-CMCollectionMember](Get-CMCollectionMember.md)
[Get-CMCollectionSetting](Get-CMCollectionSetting.md)
[Import-CMCollection](Import-CMCollection.md)
[Invoke-CMCollectionUpdate](Invoke-CMCollectionUpdate.md)
[New-CMCollection](New-CMCollection.md)
[Remove-CMCollection](Remove-CMCollection.md)
[Set-CMCollection](Set-CMCollection.md)

[How to create collections in Configuration Manager](/mem/configmgr/core/clients/manage/collections/create-collections)
