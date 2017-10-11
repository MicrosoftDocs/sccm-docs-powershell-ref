---
external help file: AdminUI.PS.Oob.dll-Help.xml
ms.assetid: 3F0D9D7A-5FD0-436C-BB6D-A28806F8A4F6
online version: https://go.microsoft.com/fwlink/?linkid=834086
schema: 2.0.0
---

# Import-CMUserDeviceAffinity

## SYNOPSIS
Imports a file that contains user and device affinities to Configuration Manager.

## SYNTAX

```
Import-CMUserDeviceAffinity [-EnableColumnHeading <Boolean>] -FileName <String> [-MappingOrder <Mapping[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Import-CMUserDeviceAffinity** cmdlet imports a file that contains user and device affinities to Microsoft System Center Configuration Manager.
User device affinity in System Center Configuration Manager is a method of associating a user with one or more specified devices.

The devices listed in the file that you specify in the *FileName* parameter must already exist as resources in the Configuration Manager database.
If they do not exist, the import will fail.

## EXAMPLES

### Example 1: Import a user device affinity
```
PS C:\>Import-CMUserDeviceAffinity -FileName "Remote_Users.csv" -EnableColumnHeadings $True
```

This command imports the user device affinity in the file named Remote_Users.csv.
The *EnableColumnHeadings* parameter specifies that the import file has column headings for reference purposes.

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

### -EnableColumnHeading
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: EnableColumnHeadings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FileName
Specifies a .csv file that contains a list of users and devices you want to create an affinity between.
Each user and device pair must be on a separate line separated by a comma.
Use the format \<Domain\>\\\<user name\>,\<device NetBIOS name\>.

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

### -MappingOrder
 

```yaml
Type: Mapping[]
Parameter Sets: (All)
Aliases: MappingOrders
Accepted values: Users, Devices, Ignored

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

[Get-CMUserDeviceAffinity](Get-CMUserDeviceAffinity.md)


