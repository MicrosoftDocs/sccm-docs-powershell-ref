---
description: Changes settings for virtual applications that you have deployed by using Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMAppVVirtualEnvironment
---

# Set-CMAppVVirtualEnvironment

## SYNOPSIS
Changes settings for virtual applications that you have deployed by using Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMAppVVirtualEnvironment [-AddApplicationGroup <VirtualEnvironmentGroup[]>] [-Description <String>]
 [-InputObject] <IResultObject> [-NewName <String>] [-PassThru]
 [-RemoveApplicationGroup <VirtualEnvironmentGroup[]>] [-DisableWildcardHandling] [-ForceWildcardHandling]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMAppVVirtualEnvironment [-AddApplicationGroup <VirtualEnvironmentGroup[]>] [-Description <String>]
 [-Id] <Int32[]> [-NewName <String>] [-PassThru] [-RemoveApplicationGroup <VirtualEnvironmentGroup[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMAppVVirtualEnvironment [-AddApplicationGroup <VirtualEnvironmentGroup[]>] [-Description <String>]
 [-Name] <String> [-NewName <String>] [-PassThru] [-RemoveApplicationGroup <VirtualEnvironmentGroup[]>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAppVVirtualEnvironment** cmdlet changes settings for one or more Microsoft Application Virtualization (App-V) virtual environment objects from Configuration Manager.
You can specify App-V environments by name or ID.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Change virtual environment settings by using a name
```
PS XYZ:\> Set-CMAppVVirtualEnvironment -Name "VMWin03" -SecurityScopeAction RemoveMembership -SecurityScopeName "ClientSecGroup01"
```

This command removes the virtual environment named VMWin03 from the security scope named ClientSecGroup01.

## PARAMETERS

### -AddApplicationGroup
Specifies an array of application groups to add.
Application groups contain multiple App-V deployment types that run in the same environment.

```yaml
Type: VirtualEnvironmentGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Description
Specifies a description for the App-V virtual environment.

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
Specifies an array of IDs of virtual environments.

```yaml
Type: Int32[]
Parameter Sets: SetById
Aliases: CIId, CI_ID

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a virtual environment object for Configuration Manager.
To obtain a virtual environment object, use the Get-CMAppVVirtualEnvironment cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValue
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of virtual environments.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for a virtual environment.

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

### -RemoveApplicationGroup
Specifies an array of application groups to remove.
Application groups contain multiple App-V deployment types that run in the same environment.

```yaml
Type: VirtualEnvironmentGroup[]
Parameter Sets: (All)
Aliases:

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

[Get-CMAppVVirtualEnvironment](Get-CMAppVVirtualEnvironment.md)

[New-CMAppVVirtualEnvironment](New-CMAppVVirtualEnvironment.md)

[Remove-CMAppVVirtualEnvironment](Remove-CMAppVVirtualEnvironment.md)
