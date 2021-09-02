---
description: Changes configuration settings for software update groups in Configuration Manager.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMSoftwareUpdateGroup
---

# Set-CMSoftwareUpdateGroup

## SYNOPSIS
Changes configuration settings for software update groups in Configuration Manager.

## SYNTAX

### SetById (Default)
```
Set-CMSoftwareUpdateGroup [-AddSoftwareUpdate <IResultObject[]>] [-ClearExpiredSoftwareUpdate]
 [-ClearSoftwareUpdate] [-ClearSupersededSoftwareUpdate] [-Description <String>] -Id <Int32>
 [-NewName <String>] [-PassThru] [-RemoveSoftwareUpdate <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByValueMandatory
```
Set-CMSoftwareUpdateGroup [-AddSoftwareUpdate <IResultObject[]>] [-ClearExpiredSoftwareUpdate]
 [-ClearSoftwareUpdate] [-ClearSupersededSoftwareUpdate] [-Description <String>] -InputObject <IResultObject>
 [-NewName <String>] [-PassThru] [-RemoveSoftwareUpdate <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByName
```
Set-CMSoftwareUpdateGroup [-AddSoftwareUpdate <IResultObject[]>] [-ClearExpiredSoftwareUpdate]
 [-ClearSoftwareUpdate] [-ClearSupersededSoftwareUpdate] [-Description <String>] -Name <String>
 [-NewName <String>] [-PassThru] [-RemoveSoftwareUpdate <IResultObject[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMSoftwareUpdateGroup** cmdlet changes the name or description of one or more Configuration Manager software update groups, or it adds or removes software update groups for one or more security scopes.

A software update group is a collection of one or more software updates.
You can add software updates to a software update group and then deploy the group to clients.
After you deploy a software update group, you can add new software updates to the group and Configuration Manager automatically deploys them.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a software update group to a security scope
```
PS XYZ:\> Set-CMSoftwareUpdateGroup -SecurityScopeAction AddMembership -SecurityScopeName "ScopeNameD02" -Name "SUGroup01"
```

This command adds a software update group named SUGroup01 as a member of the security scope named ScopeNameD02.

### Example 2: Remove a software update group from a security scope
```
PS XYZ:\> Set-CMSoftwareUpdateGroup -SecurityScopeAction RemoveMembership -SecurityScopeName "ScopeNameD17" -Name "SUGroup01"
```

This command removes the software update group named SUGroup01 from membership in the security scope named ScopeNameD17.

## PARAMETERS

### -AddSoftwareUpdate
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: AddSoftwareUpdates

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ClearExpiredSoftwareUpdate
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

### -ClearSoftwareUpdate
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

### -ClearSupersededSoftwareUpdate
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

### -Description
Specifies a description for a software update group.

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocalizedDescription

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
Specifies an array of IDs of software update groups.

```yaml
Type: Int32
Parameter Sets: SetById
Aliases: CIId, CI_ID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a software group object.
To obtain a software group object, use the [Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetByValueMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies an array of names of software update groups.

```yaml
Type: String
Parameter Sets: SetByName
Aliases: LocalizedDisplayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a name for a software update group.
This name replaces the current name of the group.

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

### -RemoveSoftwareUpdate
```yaml
Type: IResultObject[]
Parameter Sets: (All)
Aliases: RemoveSoftwareUpdates

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

[Get-CMSoftwareUpdateGroup](Get-CMSoftwareUpdateGroup.md)

[New-CMSoftwareUpdateGroup](New-CMSoftwareUpdateGroup.md)

[Remove-CMSoftwareUpdateGroup](Remove-CMSoftwareUpdateGroup.md)
