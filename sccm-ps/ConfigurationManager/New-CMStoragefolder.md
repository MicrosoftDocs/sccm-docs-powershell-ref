---
external help file: AdminUI.PS.HS.dll-Help.xml
ms.assetid: 1B4D2568-7D6A-4DFF-891B-9EDB54B3DFF0
online version: https://go.microsoft.com/fwlink/?linkid=833790
schema: 2.0.0
---

# New-CMStorageFolder

## SYNOPSIS
Creates a new storage folder in Configuration Manager.

## SYNTAX

```
New-CMStorageFolder -StorageFolderName <String> [-MaximumClientNumber <Int32>] [-MinimumFreeSpace <Int32>]
 [-SpaceUnit <MinSpaceType>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## DESCRIPTION
The **New-CMStoragefolder** cmdlet creates a new storage folder to store user migration data in Microsoft System Center Configuration Manager.

A storage folder identifies a location on a state migration point site system to store user migration data.
Use this cmdlet in conjunction with the [Add-CMStateMigrationPoint](Add-CMStateMigrationPoint.md) cmdlet to create a new state migration point with storage folders.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive. For more information, see the [getting started documentation](https://docs.microsoft.com/powershell/sccm/overview).


### Example 1: Create a new storage folder
```
PS XYZ:\> New-CMStoragefolder -MaximumClientNumber 80 -MinimumFreeSpace 10 -SpaceUnit Megabyte -StorageFolderName "D:\Contoso-Mobile-Users"
```

This command creates a new storage folder for migration data by using the maximum number of clients, minimum free space, and storage folder path parameters.

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

### -MaximumClientNumber
Specifies the maximum number of clients that the storage folder can hold.
The storage folder contains user state migration data in Configuration Manager.
Valid values are: numbers between 1 and 99999.

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

### -MinimumFreeSpace
Specifies the minimum amount of free space for storage of user state migration data.
Valid values are: numbers between 1 - 99999 when specifying a byte value, or numbers between 1 - 100 when specifying a percentage.

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

### -SpaceUnit
Specifies the storage units for the *MinimumFreeSpace* parameter.

```yaml
Type: MinSpaceType
Parameter Sets: (All)
Aliases: 
Accepted values: Megabyte, Gigabyte, Percent

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageFolderName
Specifies a local path for the storage folder.
The associated state migration point site system role in Configuration Manager uses this path.

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

