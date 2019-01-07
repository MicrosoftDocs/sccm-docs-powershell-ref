---
title: Remove-CMGlobalCondition
titleSuffix: Configuration Manager
description: Removes a Configuration Manager global condition object.

ms.date: 01/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: reference
author: mumian
ms.author: jgao
manager: dougeby
---

# Remove-CMGlobalCondition

## SYNOPSIS

Removes a Configuration Manager global condition object.

## SYNTAX

### SearchByValueMandatory (Default)

```powershell 
Remove-CMGlobalCondition -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory

```powershell
Remove-CMGlobalCondition -Id <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory

```powershell
Remove-CMGlobalCondition -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

The **Remove-CMGlobalCondition** cmdlet removes a global condition object.

Microsoft System Center Configuration Manager uses global conditions to represent business or technical conditions.
Global conditions specify how to provide and deploy applications to client devices.

You can specify a global condition by name or ID or use the **Get-CMGlobalCondition** cmdlet to obtain a global condition object.
You cannot remove read-only global conditions.

## EXAMPLES

### Example 1: Remove a global condition

```powershell
PS C:\> Remove-CMGlobalCondition -Name "GC56" -Force
```

This command removes a global condition named GC56.
Because the command uses the *Force* parameter, the system does not prompt you before it removes the condition.

### Example 2: Remove a global condition using a variable

```powershell
PS C:\> $CMGC = Get-CMGlobalCondition -Name "GC57"
PS C:\> Remove-CMGlobalCondition -InputObject $CMGC
Remove
Are you sure you wish to remove GlobalCondition: 
LocalizedDisplayName=" GC57"?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
```

The first command uses the **Get-CMGlobalCondition** cmdlet to get the global condition named GC57 and stores it in the $CMGC variable.

The second command removes the global condition stored in that variable.
This command does not use the *Force* parameter, so it prompts you for confirmation before it removes the global condition.

## PARAMETERS

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

Performs the action without a confirmation message.

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

Specifies an array of identifiers of global conditions.
This value corresponds to the **CI_ID** property of a global condition object.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: CIId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specifies a global condition object.
To obtain a global condition object, use the **Get-CMGlobalCondition** cmdlet.

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

Specifies an array of names for global conditions.
This value corresponds to the **LocalizedDisplayName** property of a global condition object.

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

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## RELATED LINKS

- [New-CMGlobalCondition](./Get-CMGlobalCondition.md)
- [Get-CMGlobalCondition](./Set-CMGlobalCondition.md)
- [Set-CMGlobalCondition](./Remove-CMGlobalCondition.md)