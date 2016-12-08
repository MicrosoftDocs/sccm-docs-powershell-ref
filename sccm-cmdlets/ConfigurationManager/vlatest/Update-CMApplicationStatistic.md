---
external help file: AdminUI.PS.AppMan.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834284
schema: 2.0.0
ms.assetid: BCE2CE97-4F41-42C4-8CDE-37F5FC704AF2
---

# Update-CMApplicationStatistic

## SYNOPSIS
Updates the statistics for an application.

## SYNTAX

### SearchByValueMandatory (Default)
```
Update-CMApplicationStatistic [-InputObject] <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Update-CMApplicationStatistic [-Name] <String> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Update-CMApplicationStatistic [-Id] <Int32> [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Update-CMApplicationStatistic** cmdlet updates the statistics for a Microsoft System Center Configuration Manager application.

## EXAMPLES

### Example 1: Update statistics for an application by ID
```
PS C:\>Update-CMApplicationStatistic -Id "16781415"
```

This command updates statistics for an application that has the ID 16781415.

### Example 2: Update statistics for an application by name
```
PS C:\>Update-CMApplicationStatistic -Name "Test"
```

This command updates statistics for an application named Test.

### Example 3: Update statistics for an application by name by using a variable
```
PS C:\>$App = Get-CMApplication -Name "Test"
PS C:\> Update-CMApplicationStatistic -InputObject $App
```

The first command gets the application object named Test and stores the object in the $App variable.

The second command updates statistics for the application stored in $App.

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

### -Id
Specifies an array of IDs of applications.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a Configuration Manager application statistic object.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: Application
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of applications.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName, ApplicationName
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Returns an object representing the item with which you are working.
By default, this cmdlet does not generate any output.

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

[Get-CMApplication](./Get-CMApplication.md)


