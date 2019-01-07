---
---

# New-CMGlobalConditionFile

## SYNOPSIS

{{Fill in the Synopsis}}

## SYNTAX

### NewFileSystem (Default)

```
New-CMGlobalConditionFile [-IsFolder] -Path <String> -FileOrFolderName <String> [-IncludeSubfolder <Boolean>]
 [-Is64Bit <Boolean>] -Name <String> [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling]
```

### NewFileSystemFile

```
New-CMGlobalConditionFile -FilePath <String> [-IncludeSubfolder <Boolean>] [-Is64Bit <Boolean>] -Name <String>
 [-Description <String>] [-DisableWildcardHandling] [-ForceWildcardHandling]
```

## DESCRIPTION

{{Fill in the Description}}

## EXAMPLES

### Example 1

```
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

### -Description

{{Fill Description Description}}

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

### -DisableWildcardHandling

{{Fill DisableWildcardHandling Description}}

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

### -FileOrFolderName

{{Fill FileOrFolderName Description}}

```yaml
Type: String
Parameter Sets: NewFileSystem
Aliases: FileName, FolderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FilePath

{{Fill FilePath Description}}

```yaml
Type: String
Parameter Sets: NewFileSystemFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling

{{Fill ForceWildcardHandling Description}}

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

### -IncludeSubfolder

{{Fill IncludeSubfolder Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: IncludeSubfolders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Is64Bit

{{Fill Is64Bit Description}}

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsFolder

{{Fill IsFolder Description}}

```yaml
Type: SwitchParameter
Parameter Sets: NewFileSystem
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name

{{Fill Name Description}}

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

### -Path

{{Fill Path Description}}

```yaml
Type: String
Parameter Sets: NewFileSystem
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

### None


## OUTPUTS

### System.Object

## NOTES

