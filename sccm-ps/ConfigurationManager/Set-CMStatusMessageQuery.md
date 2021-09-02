---
description: Changes settings or security scope or deletes messages for a Configuration Manager status message query.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 05/07/2019
schema: 2.0.0
title: Set-CMStatusMessageQuery
---

# Set-CMStatusMessageQuery

## SYNOPSIS
Changes settings or security scope or deletes messages for a Configuration Manager status message query.

## SYNTAX

### SetStatusMessageQueryByObjectMandatory (Default)
```
Set-CMStatusMessageQuery [-Comment <String>] [-Expression <String>] -InputObject <IResultObject>
 [-NewName <String>] [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetStatusMessageQueryByIdMandatory
```
Set-CMStatusMessageQuery [-Comment <String>] [-Expression <String>] -Id <String> [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetStatusMessageQueryByNameMandatory
```
Set-CMStatusMessageQuery [-Comment <String>] [-Expression <String>] -Name <String> [-NewName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteMessageByObjectMandatory
```
Set-CMStatusMessageQuery [-DeleteMessage] -InputObject <IResultObject> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteMessageByNameMandatory
```
Set-CMStatusMessageQuery [-DeleteMessage] -Name <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### DeleteMessageByIdMandatory
```
Set-CMStatusMessageQuery [-DeleteMessage] -Id <String> [-PassThru] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Set-CMStatusMessageQuery** cmdlet changes settings for a Configuration Manager status message query.
Status message queries return status messages from a Configuration Manager site database.
You can modify a comment, a Windows Management Infrastructure (WMI) expression, or the name of a query.

You can use this cmdlet with the *DeleteMessage* parameter to delete messages that this query finds.

This cmdlet can also add or remove a security scope for a message query.
Every status message query must belong to at least one security scope.

You can specify a name or ID for a query or use the [Get-CMStatusMessageQuery](Get-CMStatusMessageQuery.md) cmdlet to obtain a query.

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Add a security scope
```
PS XYZ:\> Set-CMStatusMessageQuery -Name "All Status Messages" -SecurityScopeAction AddMembership -SecurityScopeName "Scope22"
```

This command adds the security scope named Scope22 to the query named All Status Messages.

### Example 2: Delete messages
```
PS XYZ:\> Set-CMStatusMessageQuery -DeleteMessage -Name "All Active Directory Security Groups"
```

This command removes messages found by the query named All Active Directory Security Groups from the Configuration Manager database.

### Example 3: Rename a query
```
PS XYZ:\> Set-CMStatusMessageQuery -Name "All Active Directory Security Groups" -NewName "Western Security Groups"
```

This command renames the query All Active Directory Security Groups.
The new name of the query is Western Security Groups.

## PARAMETERS

### -Comment
```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByObjectMandatory, SetStatusMessageQueryByIdMandatory, SetStatusMessageQueryByNameMandatory
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeleteMessage
Indicates that messages found by this query are deleted from the Configuration Manager database.

```yaml
Type: SwitchParameter
Parameter Sets: DeleteMessageByObjectMandatory, DeleteMessageByNameMandatory, DeleteMessageByIdMandatory
Aliases:

Required: True
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

### -Expression
Specifies an expression in WMI Query Language (WQL).

```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByObjectMandatory, SetStatusMessageQueryByIdMandatory, SetStatusMessageQueryByNameMandatory
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
Specifies an ID for a status message query.

```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByIdMandatory, DeleteMessageByIdMandatory
Aliases: QueryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Specifies a status message query object.
To obtain a status message query object, use the [Get-CMStatusMessageQuery](Get-CMStatusMessageQuery.md) cmdlet.

```yaml
Type: IResultObject
Parameter Sets: SetStatusMessageQueryByObjectMandatory, DeleteMessageByObjectMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Specifies a name for a status message query.

```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByNameMandatory, DeleteMessageByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName
Specifies a new name for a query.

```yaml
Type: String
Parameter Sets: SetStatusMessageQueryByObjectMandatory, SetStatusMessageQueryByIdMandatory, SetStatusMessageQueryByNameMandatory
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
Parameter Sets: DeleteMessageByObjectMandatory, DeleteMessageByNameMandatory, DeleteMessageByIdMandatory
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

[Get-CMStatusMessageQuery](Get-CMStatusMessageQuery.md)

[New-CMStatusMessageQuery](New-CMStatusMessageQuery.md)

[Remove-CMStatusMessageQuery](Remove-CMStatusMessageQuery.md)
