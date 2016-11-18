---
external help file: AdminUI.PS.Oob.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 98AE4491-7551-417F-9D80-E310C90AE6D9
---

# Import-CMComputerInformation

## SYNOPSIS
Imports computer information into a Configuration Manager database.

## SYNTAX

### ImportSingleComputer (Default)
```
Import-CMComputerInformation [-CollectionName <String>] -ComputerName <String> [-MacAddress <String>]
 [-SMBiosGuid <String>] [-SourceComputerName <String>] [-WindowsToGoUniqueKey <String>]
 [-CollectionId <String>] [-InputObject <IResultObject>] [-UserName <String[]>]
 [-UserAccountMigrationBehavior <MigrationBehavior>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ImportComputerByUsingFile
```
Import-CMComputerInformation [-CollectionName <String>] [-EnableColumnHeading <Boolean>] -FileName <String>
 [-VariableName <String>] [-CollectionId <String>] [-InputObject <IResultObject>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMComputerInformation** cmdlet imports computer information directly into a Microsoft System Center Configuration Manager database.
For System Center Configuration Manager to deploy an operating system to a new computer with no installed operating system, you must add the new computer to System Center Configuration Manager.
After you import the computer information, System Center Configuration Manager can deploy an operating system.

You can import a single computer by specifying the Media Access Control (MAC) address and computer name, along with the name of a collection.
This cmdlet adds this computer to the specified collection.

You can also import several computers by specifying a Comma Separated Values .csv file with computer information, along with the name of a collection.
This cmdlet adds the computers to the specified collection.

You can specify the name of a reference computer.
System Center Configuration Manager migrates user information and settings from the reference computer to the new computer.

## EXAMPLES

### Example 1: Import computers by using a file
```
PS C:\>Import-CMComputerInformation -CollectionName "All Systems" -FileName "\\cmshare\Public\CM\ImportComputers.csv" -EnableColumnHeadings $True
```

This command imports the computers specified in the CVS file into the All Systems collection.
This command includes a value of $True for the *-EnableColumnHeadings* parameter.
The cmdlet ignores the first line of the file.

### Example 2: Import a single computer
```
PS C:\>Import-CMComputerInformation -CollectionName "All Systems" -ComputerName "Computer08" -MacAddress "5F:DA:FA:FA:FA:FA" -SmBiosGuid "AAAAAAAA-AAAA-AAAA-AAAA-AAAAAAAAAAAA"
```

This command imports a specified computer into the All Systems collection.
The command specifies the name, MAC address, and SMBIOS GUID for a computer.

### Example 3: Import a computer using a reference computer
```
PS C:\>Import-CMComputerInformation -CollectionName "All Systems" -ComputerName "Computer08" -MacAddress "5F:DA:FA:FA:FA:FA" -SmBiosGuid "AAAAAAAA-AAAA-AAAA-AAAA-AAAAAAAAAAAA" -SourceComputerName "ResourceComputer01"
```

This command imports a specified computer into the All Systems collection.
The command specifies the name, MAC address, and SMBIOS GUID for a computer.
The command also includes a reference computer to associate with the new computer.

## PARAMETERS

### -CollectionId


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

### -CollectionName
Specifies a name of a Configuration Manager device collection.

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

### -ComputerName
Specifies the name of a computer that this cmdlet imports information from.

```yaml
Type: String
Parameter Sets: ImportSingleComputer
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
Indicates that wildcard handling is disabled.

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

### -EnableColumnHeading


```yaml
Type: Boolean
Parameter Sets: ImportComputerByUsingFile
Aliases: EnableColumnHeadings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileName
Specifies a .csv file that contains computer information.
The file must contain the name and MAC address of each computer to be imported.

```yaml
Type: String
Parameter Sets: ImportComputerByUsingFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceWildcardHandling
Indicates that wildcard handling is enabled.

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


```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: Collection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MacAddress
Specifies a MAC address for a computer in the format (00:00:00:00:00:00).
The Windows Preinstallation Environment (Windows PE) must have a driver for the specified network adapter.

```yaml
Type: String
Parameter Sets: ImportSingleComputer
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SMBiosGuid


```yaml
Type: String
Parameter Sets: ImportSingleComputer
Aliases: SMBIOSID

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceComputerName
Specifies a name of a reference computer.
Configuration Manager migrates user state and settings from the reference computer to the new computer.

```yaml
Type: String
Parameter Sets: ImportSingleComputer
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserAccountMigrationBehavior


```yaml
Type: MigrationBehavior
Parameter Sets: ImportSingleComputer
Aliases: 
Accepted values: CaptureAllUserAccountsAndRestoreSpecifiedAccounts, CaptureAndRestoreSpecifiedUserAccounts

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserName


```yaml
Type: String[]
Parameter Sets: ImportSingleComputer
Aliases: UserNames

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VariableName
Specifies a variable name for an imported column.
When you import a .csv file, you specify the columns to import and assign them to a Configuration Manager field.
A variable allows you to assign a column to a variable.

```yaml
Type: String
Parameter Sets: ImportComputerByUsingFile
Aliases: 

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

### -WindowsToGoUniqueKey


```yaml
Type: String
Parameter Sets: ImportSingleComputer
Aliases: WtgUniqueKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-CMComputerAssociation](./Get-CMComputerAssociation.md)


