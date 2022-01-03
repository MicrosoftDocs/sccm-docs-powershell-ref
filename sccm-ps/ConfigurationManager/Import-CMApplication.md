---
description: Imports an application into Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/05/2019
schema: 2.0.0
title: Import-CMApplication
---

# Import-CMApplication

## SYNOPSIS
Imports an application into Configuration Manager.

## SYNTAX

```
Import-CMApplication -FilePath <String> [-ImportActionType <ImportActionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMApplication** cmdlet imports a package created by the [Export-CMApplication](Export-CMApplication.md) cmdlet.
A package contains one or more applications and related objects, such as catalogs.
If the package contains content, the application package imports the content, or includes a reference to the content.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Import an application
```
PS XYZ:\>Import-CMApplication -FilePath "\\Server1\resource\test.zip" -ImportActionType DirectImport
```

This command imports the application stored in test.zip, including the application objects.

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

### -FilePath
Specifies a file path for the application.

```yaml
Type: String
Parameter Sets: (All)
Aliases: FileName, ImportFilePath, Path

Required: True
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

### -ImportActionType
Specifies an import action type for the application.
If this application already exists in the Software Library, Configuration Manager adds a revision to the existing application unless you modify the action to create a new application.
Valid values are:

- Skip.
This option is not supported.
- NotSet.
No action is specified.
The default behavior is:
    - If there is a conflict with the application model ID, a new revision is added to the existing application.
    - If there is a conflict with the application name, a new application is created with a new name.
- DirectImport.
Imports the application objects.
The default behavior is:
    - If there is a conflict with the application model ID, the error is displayed.
    - If there is a conflict with the application name, a new application is created with a new name.
- Rename.
This option is not supported.
- Overwrite.
Maps objects despite name or scope duplication.
If the revision of the application does not match the revision of the application to import, then a new revision is added to the existing application.
- ImportFail.
This option is not supported.

```yaml
Type: ImportActionType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Skip, DirectImport, Rename, Overwrite, ImportFail

Required: False
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

[ConvertFrom-CMApplication](ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](ConvertTo-CMApplication.md)

[Export-CMApplication](Export-CMApplication.md)

[Get-CMApplication](Get-CMApplication.md)

[New-CMApplication](New-CMApplication.md)

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Set-CMApplication](Set-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)
