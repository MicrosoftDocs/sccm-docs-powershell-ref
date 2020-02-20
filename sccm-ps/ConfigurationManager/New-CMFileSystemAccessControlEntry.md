---
external help file: AdminUI.PS.Dcm.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMFileSystemAccessControlEntry

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

```
New-CMFileSystemAccessControlEntry -GroupOrUserName <String> [-AccessOption <AccessType>]
 [-Permission <FileSystemPermissions[]>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS XYZ:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -AccessOption
{{ Fill AccessOption Description }}

```yaml
Type: AccessType
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWildcardHandling
{{ Fill DisableWildcardHandling Description }}

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
{{ Fill ForceWildcardHandling Description }}

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

### -GroupOrUserName
{{ Fill GroupOrUserName Description }}

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

### -Permission
{{ Fill Permission Description }}

```yaml
Type: FileSystemPermissions[]
Parameter Sets: (All)
Aliases: Permissions
Accepted values: ListFolderContentsOrReadData, CreateFilesOrWriteData, CreateFoldersOrAppendData, ReadExtendedAttributes, WriteExtendedAttributes, TraverseFolderOrExecuteFile, DeleteSubfoldersAndFiles, ReadAttributes, WriteAttributes, Write, Delete, ReadPermissions, Read, Execute, ChangePermissions, TakeOwnership, FullControl

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

### System.Object
## NOTES

## RELATED LINKS
