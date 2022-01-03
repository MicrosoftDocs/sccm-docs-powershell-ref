---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
online version:
schema: 2.0.0
---

# Get-CMFolder

## SYNOPSIS

Get one or more folders in the console.

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

Use this cmdlet to get all customized folders or folders from the specified parent path.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
$parentPath = 'DeviceCollection'
$name = 'Folder1'
$name2 = 'Folder2'
$name3 = 'Folder3'
$root = New-CMFolder -ParentFolderPath $parentPath -Name $name
$folder = Get-CMFolder -FolderPath ($parentPath + '\' + $name + '\' + $name2 + '\' +$name3)
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

### -FolderPath

Specify the path to the console folder. For example, `DeviceCollection\Folder1`

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

### -Guid

Specify the GUID of the console folder.

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

Specify the ID of the console folder.

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

Specify a folder object for the parent container.

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

Set this parameter to `$true` to filter the results by empty folders.

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

Set this parameter to `$true` to filter the results by search folders.

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

Specify the name of the console folder.

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

Specify the path of the parent folder.

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

Specify the three-character code for the site.

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

Specify the type to filter the results. For example:

- `SMS_Collection_Device`
- `SMS_Package`
- `SMS_Driver`

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

For more information on this return object and its properties, see [SMS_ObjectContainerNode server WMI class](/mem/configmgr/develop/reference/core/servers/console/sms_objectcontainernode-server-wmi-class).

## RELATED LINKS

[New-CMFolder](New-CMFolder.md)

[Remove-CMFolder](Remove-CMFolder.md)

[Set-CMFolder](Set-CMFolder.md)
