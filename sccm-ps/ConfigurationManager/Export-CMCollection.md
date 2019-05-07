---
external help file: AdminUI.PS.Collections.dll-Help.xml
ms.assetid: CD980A75-6FE0-429E-BCC3-26B98F4C9664
online version: https://go.microsoft.com/fwlink/?linkid=834017
schema: 2.0.0
---

# Export-CMCollection

## SYNOPSIS
Exports a Configuration Manager collection.

## SYNTAX

### SearchByNameMandatory (Default)
```
Export-CMCollection -Name <String> -ExportFilePath <String> [-ExportComment <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Export-CMCollection -CollectionId <String> -ExportFilePath <String> [-ExportComment <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Export-CMCollection -InputObject <IResultObject> -ExportFilePath <String> [-ExportComment <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Export-CMCollection** cmdlet saves a collection object to a specified MOF file in Microsoft System Center Configuration Manager.

Configuration Manager collections provide a way to manage users, computers, and other resources in your organization. They not only give you a means to organize your resources, but they also give you a means to distribute Configuration Manager packages to clients and users.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Export a collection by name
```
PS XYZ:\> Export-CMCollection -Name "testUser" -ExportFilePath "C:\collection.mof"
```

This command exports the collection named testUser to the file named collection.mof.

### Example 2: Get a collection object and export it
```
PS XYZ:\> Get-CMCollection -Name "testUser" | Export-CMCollection -ExportFilePath "C:\collection.mof"
```

This command gets the collection object named testUser and uses the pipeline operator to pass the object to **Export-CMCollection**, which exports the object to the file named collection.mof.

## PARAMETERS

### -CollectionId
Specifies a collection ID.
If you do not specify a collection, all collections in the hierarchy are exported.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: 

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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
DisableWildcardHandling treats wildcard characters as literal character values. Cannot be combined with **ForceWildcardHandling**.

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

### -ExportComment
Specifies a comment for the exported collection.

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

### -ExportFilePath
Specifies the full path for the export file. The file name must end in ".mof".

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
ForceWildcardHandling processes wildcard characters and may lead to unexpected behavior (not recommended). Cannot be combined with **DisableWildcardHandling**.

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
Specifies a collection object.
To obtain a collection object, use the [Get-CMCollection](Get-CMCollection.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a collection.
If you do not specify a collection, all collections in the hierarchy are exported.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Shows what would happen if the cmdlet runs.
The cmdlet is not run.

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
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMCollection](Get-CMCollection.md)

[Import-CMCollection](Import-CMCollection.md)

[New-CMCollection](New-CMCollection.md)

[Remove-CMCollection](Remove-CMCollection.md)

[Set-CMCollection](Set-CMCollection.md)
