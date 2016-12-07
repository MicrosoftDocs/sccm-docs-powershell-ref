---
external help file: AdminUI.PS.Rba.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=834023
schema: 2.0.0
ms.assetid: 625C4356-E131-46E4-B0AA-A4E1BB6996A7
---

# Set-CMSecurityScope

## SYNOPSIS
Sets a security scope.

## SYNTAX

### SetByValue (Default)
```
Set-CMSecurityScope -InputObject <IResultObject> [-NewName <String>] [-Description <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMSecurityScope -Id <String> [-NewName <String>] [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSecurityScope -Name <String> [-NewName <String>] [-Description <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSecurityScope** cmdlet changes the configuration settings of a security scope.

## EXAMPLES

### Example 1: Get a security scope and update its name
```
PS C:\>$Scope = Get-CMSecurityScope -Name "Scope"
PS C:\> Set-CMSecurityScope -InputObject $Scope -NewName "newScope"
```

The first command gets the security scope object named Scope and stores the object in the $Scope variable.

The second command changes the name of the security scope stored in $Scope to newScope.

### Example 2: Pass a security scope through the pipeline and update its name
```
PS C:\>Get-CMSecurityScope -Name "Scope" | Set-CMSecurityScope -NewName "newScope"
```

This command gets the security scope object named Scope and uses the pipeline operator to pass the object to **Set-CMSecurityScope**, which changes the name of the security scope to newScope.

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

### -Description
Specifies a description for the security scope.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CategoryDescription
Required: False
Position: Named
Default value: None
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
Specifies the ID of a security scope.

```yaml
Type: String
Parameter Sets: SetById
Aliases: CategoryId
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a security scope object.
To obtain a security scope object, use the [Get-CMSecurityScope](./Get-CMSecurityScope.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases: 
Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies the name of a security scope.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: CategoryName
Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for the security scope.

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

[Get-CMSecurityScope](./Get-CMSecurityScope.md)

[New-CMSecurityScope](./New-CMSecurityScope.md)

[Remove-CMSecurityScope](./Remove-CMSecurityScope.md)

[Remove-CMSecurityScopeFromAdministrativeUser](./Remove-CMSecurityScopeFromAdministrativeUser.md)
