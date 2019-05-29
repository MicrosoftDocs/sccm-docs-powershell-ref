---
title: Remove-CMAppVVirtualEnvironment
titleSuffix: Configuration Manager
description: Removes an App-V virtual environment.
ms.date: 05/07/2019
ms.prod: configuration-manager
ms.technology: configmgr-other
ms.topic: conceptual
author: aczechowski
ms.author: aaroncz
manager: dougeby
---

# Remove-CMAppVVirtualEnvironment

## SYNOPSIS
Removes an App-V virtual environment.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMAppVVirtualEnvironment -InputObject <IResultObject> [-Force] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMAppVVirtualEnvironment -Name <String> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Remove-CMAppVVirtualEnvironment -Id <Int32[]> [-Force] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMAppVVirtualEnvironment** cmdlet removes one or more Microsoft Application Virtualization (App-V) virtual environment objects from Microsoft System Center Configuration Manager.
You can specify App-V virtual environments by name or ID, or you can provide an App-V virtual environment object.

## EXAMPLES

### Example 1: Remove a virtual environment by name
```
PS C:\> Remove-CMAppVVirtualEnvironment -Name "Test"
```

This command removes an App-V virtual environment named Test.

### Example 2: Remove a virtual environment by ID
```
PS C:\> Remove-CMAppVVirtualEnvironment -Id "16781806"
```

This command removes an App-V virtual environment that has the ID 16781806.

### Example 3: Remove a virtual environment by name by using a wildcard
```
PS C:\> $AppV = Get-CMAppVVirtualEnvironment -Name "T*"
PS C:\> Remove-CMAppVVirtualEnvironment -InputObject $AppV
```

The first command gets all App-V virtual environments that have names that begin with the letter T and stores them in the $AppV variable.

The second command removes all the environments stored in $AppV.

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
Specifies an array of IDs of virtual environments.

```yaml
Type: Int32[]
Parameter Sets: SearchByIdMandatory
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies an App-V virtual environment object.

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
Specifies an array of names of App-V virtual environment objects.
You can use a wildcard.

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

[Get-CMAppVVirtualEnvironment](Get-CMAppVVirtualEnvironment.md)

[New-CMAppVVirtualEnvironment](New-CMAppVVirtualEnvironment.md)

[Set-CMAppVVirtualEnvironment](Set-CMAppVVirtualEnvironment.md)


