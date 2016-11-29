---
external help file: AdminUI.PS.Collections.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834256
schema: 2.0.0
ms.assetid: B4B866B4-15B3-46F0-A742-C892A96B99CD
---

# Remove-CMUser

## SYNOPSIS
Removes a user from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMUser [-Force] [-InputObject] <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMUser [-Name] <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMUser [-ResourceId] <Int32> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMUser** cmdlet removes user accounts from Microsoft System Center Configuration Manager.

## EXAMPLES

### Example 1: Remove a user
```
PS C:\>$User = Get-CMUser -CollectionName "All Users" -Name "Contoso\user01"
PS C:\> Remove-CMUser -InputObject $User -Force
```

The first command gets the user object named user01 from the All Users collection and stores the object in the $User variable.

The second command removes the user account stored in $User.
Specifying the *Force* parameter indicates that the user is not prompted before the user account is removed.

### Example 2: Remove a user by using the pipeline
```
PS C:\>Get-CMUser -CollectionName "All Users" -Name "Contoso\user02" | Remove-CMUser -Force
```

This command gets the user object named user02 from the All Users collection and uses the pipeline operator to pass the object to **Remove-CMUser**, which removes the user account.
Specifying the *Force* parameter indicates that the user is not prompted before the user account is removed.

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
Specifies a Configuration Manager user account object.
To obtain a Configuration Manager user account object, use the Get-CMUser cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SearchByValueMandatory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a user account.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: UserName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Specifies the resource ID of a user account.

```yaml
Type: Int32
Parameter Sets: SearchByIdMandatory
Aliases: Id, UserId

Required: True
Position: 0
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

[Get-CMUser](./Get-CMUser.md)


