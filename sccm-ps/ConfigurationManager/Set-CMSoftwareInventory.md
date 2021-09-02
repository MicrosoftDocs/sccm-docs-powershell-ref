---
description: Modifies an object that collects software inventory data on files.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSoftwareInventory
---

# Set-CMSoftwareInventory

## SYNOPSIS
Modifies an object that collects software inventory data on files.

## SYNTAX

### SetById (Default)
```
Set-CMSoftwareInventory [-CategoryId <Int32>] [-CleanTag1] [-CleanTag2] [-CleanTag3] [-FamilyId <Int32>]
 -Id <String> [-NewName <String>] [-ParentSoftwareId <String>] [-PassThru] [-Publisher <String>]
 [-Tag1Id <Int32>] [-Tag2Id <Int32>] [-Tag3Id <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareInventory [-CategoryId <Int32>] [-CleanTag1] [-CleanTag2] [-CleanTag3] [-FamilyId <Int32>]
 -Name <String[]> [-NewName <String>] [-ParentSoftwareId <String>] [-PassThru] [-Publisher <String>]
 [-Tag1Id <Int32>] [-Tag2Id <Int32>] [-Tag3Id <Int32>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMSoftwareInventory [-CategoryId <Int32>] [-CleanTag1] [-CleanTag2] [-CleanTag3] [-FamilyId <Int32>]
 -InputObject <IResultObject> [-NewName <String>] [-ParentSoftwareId <String>] [-PassThru]
 [-Publisher <String>] [-Tag1Id <Int32>] [-Tag2Id <Int32>] [-Tag3Id <Int32>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareInventory** cmdlet modifies an object that collects information about files on client devices in Configuration Manager.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Set a software inventory object
```
PS XYZ:\> Set-CMSoftwareInventory -Name "MSXML 6.0 Parser"
```

This command starts collecting software inventory data on the file named MSXML 6.0 Parser.

## PARAMETERS

### -CategoryId
{{ Fill CategoryId Description }}

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanTag1
{{ Fill CleanTag1 Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanLabel1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanTag2
{{ Fill CleanTag2 Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanLabel2

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CleanTag3
{{ Fill CleanTag3 Description }}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: CleanLabel3

Required: False
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

### -FamilyId
Specifies the ID of the family used to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
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

### -Id
Specifies an array of IDs of software files.

```yaml
Type: String
Parameter Sets: SetById
Aliases: SoftwareKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a **CMSoftwareInventory** object.
To obtain a **CMSoftwareInventory** object, use the [Get-CMSoftwareInventory](Get-CMSoftwareInventory.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software files.

```yaml
Type: String[]
Parameter Sets: SetByName
Aliases: CommonName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for inventoried software in Configuration Manager.

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

### -ParentSoftwareId
{{ Fill ParentSoftwareId Description }}

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

### -Publisher
Specifies the name of a software publisher in Configuration Manager.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CommonPublisher

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag1Id
Specifies the ID of a tag to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Label1Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag2Id
Specifies the ID of a tag to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Label2Id

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag3Id
Specifies the ID of a tag to classify inventoried software in Configuration Manager.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: Label3Id

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

### Microsoft.ConfigurationManagement.ManagementProvider.IResultObject
## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS

[Get-CMSoftwareInventory](Get-CMSoftwareInventory.md)

[Undo-CMSoftwareInventory](Undo-CMSoftwareInventory.md)
