---
external help file: AdminUI.PS.AppModel.dll-Help.xml
online version: https://go.microsoft.com/fwlink/?linkid=833647
schema: 2.0.0
ms.assetid: 8AB81212-FC73-4DA4-A8CB-F9090B6BFE91
---

# Set-CMAppVVirtualEnvironment

## SYNOPSIS
Changes settings for virtual applications that you have deployed by using Configuration Manager.

## SYNTAX

### SetByValue (Default)
```
Set-CMAppVVirtualEnvironment [-InputObject] <IResultObject> [-NewName <String>] [-Description <String>]
 [-AddApplicationGroup <VirtualEnvironmentGroup[]>] [-RemoveApplicationGroup <VirtualEnvironmentGroup[]>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetById
```
Set-CMAppVVirtualEnvironment [-Id] <Int32[]> [-NewName <String>] [-Description <String>]
 [-AddApplicationGroup <VirtualEnvironmentGroup[]>] [-RemoveApplicationGroup <VirtualEnvironmentGroup[]>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMAppVVirtualEnvironment [-Name] <String> [-NewName <String>] [-Description <String>]
 [-AddApplicationGroup <VirtualEnvironmentGroup[]>] [-RemoveApplicationGroup <VirtualEnvironmentGroup[]>]
 [-PassThru] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMAppVVirtualEnvironment** cmdlet changes settings for one or more Microsoft Application Virtualization (App-V) virtual environment objects from Microsoft System Center Configuration Manager.
You can specify App-V environments by name or ID.

## EXAMPLES

### Example 1: Change virtual environment settings by using a name
```
PS C:\>Set-CMAppVVirtualEnvironment -Name "VMWin03" -SecurityScopeAction RemoveMembership -SecurityScopeName "ClientSecGroup01"
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

[Get-CMAppVVirtualEnvironment](./Get-CMAppVVirtualEnvironment.md)

[New-CMAppVVirtualEnvironment](./New-CMAppVVirtualEnvironment.md)

[Remove-CMAppVVirtualEnvironment](./Remove-CMAppVVirtualEnvironment.md)


