---
external help file: AdminUI.PS.Sum.dll-Help.xml
ms.assetid: 0AE20299-BC95-4F7B-9D2C-E57678954D6D
online version: https://go.microsoft.com/fwlink/?linkid=834226
schema: 2.0.0
---

# Remove-CMSoftwareUpdateGroup

## SYNOPSIS
Removes Configuration Manager software update groups.

## SYNTAX

### SearchByIdMandatory (Default)
```
Remove-CMSoftwareUpdateGroup -Id <String[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSoftwareUpdateGroup -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByValueMandatory
```
Remove-CMSoftwareUpdateGroup -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSoftwareUpdateGroup** cmdlet removes software update groups from Microsoft System Center Configuration Manager.
You can specify each software update group that you are removing by using the group IDs or names.
If you remove a software update group, you can use the [Get-CMSoftwareUpdateGroup](./Get-CMSoftwareUpdateGroup.md) cmdlet to return a software update group object and use that object to specify the group that you want to remove.

## EXAMPLES

### Example 1: Remove a software update group by using an ID
```
PS C:\> Remove-CMSoftwareUpdateGroup -Id "ST10000B"
```

This command removes the software update group that has the ID ST10000B.

### Example 2: Remove a software update group by using a name
```
PS C:\> Remove-CMSoftwareUpdateGroup -Name "SUGroupD01"
```

This command removes the software update group named SUGroupD01.

### Example 3: Remove a software update group by using an object variable
```
PS C:\> $SubObj=Get-CMSoftwareUpdateGroup -Id "ST10000B" 
PS C:\> Remove-CMSoftwareUpdateGroup -SoftwareUpdateGroup $SubObj
```

The first command gets the software update group that has the ID ST10000B, and then stores it in the variable $SubObj.

The second command removes the software update group by using the $SubObj variable.

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

### -Force
Forces the command to run without asking for user confirmation.

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

### -Id
Specifies an array of software update group IDs.

```yaml
Type: String[]
Parameter Sets: SearchByIdMandatory
Aliases: CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies the software update group object to remove.
To obtain a software update group object, use **Get-CMSoftwareUpdateGroup**.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of software update group names.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: LocalizedDisplayName

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

[Get-CMSoftwareUpdateGroup](./Get-CMSoftwareUpdateGroup.md)

[New-CMSoftwareUpdateGroup](./New-CMSoftwareUpdateGroup.md)

[Set-CMSoftwareUpdateGroup](./Set-CMSoftwareUpdateGroup.md)


