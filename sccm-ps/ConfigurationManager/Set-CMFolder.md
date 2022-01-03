---
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/16/2021
online version:
schema: 2.0.0
---

# Set-CMFolder

## SYNOPSIS

Configure a folder in the console.

## SYNTAX

### SearchByName (Default)
```
Set-CMFolder -Name <String> [-ParentContainerNode <IResultObject>] [-ParentFolderPath <String>]
 [-NewName <String>] [-MoveToPath <String>] [-MoveToFolder <IResultObject>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMFolder -Id <Int32> [-NewName <String>] [-MoveToPath <String>] [-MoveToFolder <IResultObject>] [-PassThru]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByGuidMandatory
```
Set-CMFolder -Guid <Guid> [-NewName <String>] [-MoveToPath <String>] [-MoveToFolder <IResultObject>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByPathMandatory
```
Set-CMFolder -FolderPath <String> [-NewName <String>] [-MoveToPath <String>] [-MoveToFolder <IResultObject>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByObjectMandatory
```
Set-CMFolder -InputObject <IResultObject> [-NewName <String>] [-MoveToPath <String>]
 [-MoveToFolder <IResultObject>] [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure the specified folder. For example, rename it or move it to another folder.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1

```powershell
$parentPath = 'DeviceCollection'
$name =  'Folder1'
$name2 =  'Folder2'
$name3 =  'Folder3'
$root = New-CMFolder -ParentFolderPath $parentPath -Name $name
Set-CMFolder -Name $name2 -ParentContainerNode (Get-CMFolder -Name $name) -NewName $newName 
```

### Example 2

```powershell
(Get-CMFolder -Name $newName) | Set-CMFolder -NewName $name2
```

### Example 3

```powershell
$folder = Set-CMFolder -Name $name3 -ParentFolderPath ($parentPath + '\' + $name + '\' + $name2) -MoveToFolder $root
```

### Example 4

```powershell
$folder = Set-CMFolder -Guid $sub2.FolderGuid -MoveToPath ($parentPath + '\' + $name + '\' + $name2)
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

Specify the GUID of the console folder to configure.

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

Specify the ID of the console folder to configure.

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

Specify a folder object to configure. To get this object, use the [Get-CMFolder](Get-CMFolder.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByObjectMandatory
Aliases: ContainerNode

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MoveToFolder

To move a folder, specify the target folder object. To get this object, use the [Get-CMFolder](Get-CMFolder.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MoveToPath

To move a folder, specify the path to the target folder.

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

### -Name

Specify the name of the console folder to configure.

```yaml
Type: String
Parameter Sets: SearchByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Use this parameter to rename the folder.

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

### -ParentContainerNode

Specify a folder object for the parent container. To get this object, use the [Get-CMFolder](Get-CMFolder.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
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

### -PassThru

Add this parameter to return an object that represents the item with which you're working. By default, this cmdlet may not generate any output.

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

[Get-CMFolder](Get-CMFolder.md)

[New-CMFolder](New-CMFolder.md)

[Remove-CMFolder](Remove-CMFolder.md)
