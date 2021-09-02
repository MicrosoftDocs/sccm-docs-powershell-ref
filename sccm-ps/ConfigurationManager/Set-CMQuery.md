---
description: Configure a Configuration Manager query.
external help file: AdminUI.PS.dll-Help.xml
Module Name: ConfigurationManager
ms.date: 12/29/2020
schema: 2.0.0
title: Set-CMQuery
---

# Set-CMQuery

## SYNOPSIS

Configure a Configuration Manager query.

## SYNTAX

### SearchByValueMandatory (Default)
```
Set-CMQuery [-Comment <String>] [-Expression <String>] -InputObject <IResultObject>
 [-LimitToCollectionId <String>] [-NewName <String>] [-PassThru] [-TargetClassName <String>]
 [-DisableWildcardHandling] [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByIdMandatory
```
Set-CMQuery [-Comment <String>] [-Expression <String>] -Id <String> [-LimitToCollectionId <String>]
 [-NewName <String>] [-PassThru] [-TargetClassName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Set-CMQuery [-Comment <String>] [-Expression <String>] [-LimitToCollectionId <String>] -Name <String>
 [-NewName <String>] [-PassThru] [-TargetClassName <String>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION

Use this cmdlet to configure a query in Configuration Manager. Configuration Manager queries define a WMI Query Language (WQL) expression to get information from the site database based on the criteria you provide. WQL is similar to SQL, but still goes through the SMS Provider instead of directly to the database. So WQL still abides by your role-based access configuration.

Queries can return most types of Configuration Manager objects, which include computers, sites, collections, applications, and inventory data. For more information, see [Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries).

By default, Configuration Manager includes several queries. You can use the [Get-CMQuery](Get-CMQuery.md) cmdlet to review the default queries. For more examples of WQL expressions, see [Example WQL queries](/mem/configmgr/core/servers/manage/create-queries#BKMK_Example).

> [!NOTE]
> Run Configuration Manager cmdlets from the Configuration Manager site drive, for example `PS XYZ:\>`. For more information, see [getting started](/powershell/sccm/overview).

## EXAMPLES

### Example 1: Rename a query

```powershell
Get-CMQuery -Name "My systems" | Set-CMQuery -NewName "My systems v2"
```

### Example 2: Change the query to prompt for a limiting collection

```powershell
Set-CMQuery -Name "Windows 10" -LimitToCollectionId "<Prompt>"
```

## PARAMETERS

### -Comment

Specify an optional comment to further identify the query in the site.

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

### -Expression

Specify the WQL statement that defines the attributes to display in the results and the criteria to limit the results.

WQL statements often include double quotation marks (`"`), so set this parameter's value as a string enclosed in single quotation marks (`'`).

For more examples, see [Example WQL queries](/mem/configmgr/core/servers/manage/create-queries#BKMK_Example).

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

Specify the ID of the query to configure. For example, `"XYZ00006"`.

```yaml
Type: String
Parameter Sets: SearchByIdMandatory
Aliases: QueryId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject

Specify a query object to configure. To get this object, use the [Get-CMQuery](Get-CMQuery.md) cmdlet.

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

### -LimitToCollectionId

Specify how to configure collection limiting for this query:

- **Not collection limited**: Set this parameter's value to a blank string (`""`). Don't use the `$null` built-in variable.
- **Limit to collection**: Specify the ID of a collection. For example, `"SMSDM003"` for the **All Desktop and Server Clients** collection.
- **Prompt for collection**: Set this parameter's value to `"<Prompt>"`.

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

### -Name

Specify the name of the query to configure.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewName

Specify a new name to rename the query.

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

### -TargetClassName

Specify the name of the object class that you want the query to return. There are many object types available. The following table lists several common class names with the description from the Configuration Manager console:

|Class name  |Description  |
|---------|---------|
|`SMS_R_System`|System resource|
|`SMS_Program`|Program|
|`SMS_R_UserGroup`|User group resource|
|`SMS_R_User`|User resource|
|`SMS_SiteAndSubsites`|Site and subsites|
|`SMS_R_UnknownSystem`|Unknown computer|

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

### -Confirm

Prompts you for confirmation before running the cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
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
Default value: None
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

[Export-CMQuery](Export-CMQuery.md)
[Get-CMQuery](Get-CMQuery.md)
[Import-CMQuery](Import-CMQuery.md)
[Invoke-CMQuery](Invoke-CMQuery.md)
[New-CMQuery](New-CMQuery.md)
[Remove-CMQuery](Remove-CMQuery.md)
[Introduction to queries in Configuration Manager](/mem/configmgr/core/servers/manage/introduction-to-queries)
