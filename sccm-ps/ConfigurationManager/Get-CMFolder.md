---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# Get-CMFolder

## SYNOPSIS
{{ Fill in the Synopsis }}

## SYNTAX

### SearchByName (Default)
```
Get-CMFolder [[-Name] <String>] [-InputObject <IResultObject>] [-ParentFolderPath <String>]
 [-TypeName <String>] [-IsEmpty <Boolean>] [-IsSearchFolder <Boolean>] [-SiteCode <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByIdMandatory
```
Get-CMFolder -Id <Int32> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByGuidMandatory
```
Get-CMFolder -Guid <Guid> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

### SearchByPathMandatory
```
Get-CMFolder -FolderPath <String> [-DisableWildcardHandling] [-ForceWildcardHandling] [<CommonParameters>]
```

## DESCRIPTION
{{ Fill in the Description }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Add example code here }}
```

{{ Add example description here }}

## PARAMETERS

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

### -FolderPath
{{ Fill FolderPath Description }}

```yaml
Type: String
Parameter Sets: SearchByPathMandatory
Aliases:

Required: True
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

### -Guid
{{ Fill Guid Description }}

```yaml
Type: Guid
Parameter Sets: SearchByGuidMandatory
Aliases: FolderGuid

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
{{ Fill Id Description }}

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: ContainerNodeID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
{{ Fill InputObject Description }}

```yaml
Type: IResultObject
Parameter Sets: SearchByName
Aliases: ParentContainerNode

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -IsEmpty
{{ Fill IsEmpty Description }}

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IsSearchFolder
{{ Fill IsSearchFolder Description }}

```yaml
Type: Boolean
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
{{ Fill Name Description }}

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### -ParentFolderPath
{{ Fill ParentFolderPath Description }}

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
{{ Fill SiteCode Description }}

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: SourceSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeName
{{ Fill TypeName Description }}

```yaml
Type: String
Parameter Sets: SearchByName
Aliases: ObjectTypeName

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

### IResultObject[]#SMS_ObjectContainerNode

### IResultObject#SMS_ObjectContainerNode

## NOTES

## RELATED LINKS
