---
external help file: AdminUI.PS.AppMan.dll-Help.xml
ms.assetid: 0CF8ACEA-3D7A-43E6-AA0B-408012386BEE
online version: https://go.microsoft.com/fwlink/?linkid=834033
schema: 2.0.0
---

# Import-CMApplication

## SYNOPSIS
Imports an application into Configuration Manager.

## SYNTAX

```
Import-CMApplication -FilePath <String> [-ImportActionType <ImportActionType>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

> [!NOTE]
> The -FilePath parameter must be a UNC path.  Importing from a local disk is not supported.

## DESCRIPTION
The **Import-CMApplication** cmdlet imports a package created by the [Export-CMApplication](Export-CMApplication.md) cmdlet.
A package contains one or more applications and related objects, such as catalogs.
If the package contains content, the application package imports the content, or includes a reference to the content.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Import an application
```
PS XYZ:\>Import-CMApplication -FilePath "\\Server1\resource\test.zip" -ImportActionType DirectImport
```

This command imports the application stored in test.zip, including the application objects.

## PARAMETERS

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

### -FilePath
Specifies a file path for the application.  This must be a UNC path.

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

[ConvertFrom-CMApplication](ConvertFrom-CMApplication.md)

[ConvertTo-CMApplication](ConvertTo-CMApplication.md)

[Export-CMApplication](Export-CMApplication.md)

[Get-CMApplication](Get-CMApplication.md)

[New-CMApplication](New-CMApplication.md)

[Remove-CMApplication](Remove-CMApplication.md)

[Resume-CMApplication](Resume-CMApplication.md)

[Set-CMApplication](Set-CMApplication.md)

[Suspend-CMApplication](Suspend-CMApplication.md)
