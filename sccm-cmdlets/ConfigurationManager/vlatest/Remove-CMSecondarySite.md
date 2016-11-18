---
external help file: AdminUI.PS.HS.dll-Help.xml
online version: 
schema: 2.0.0
ms.assetid: 44AF985A-0AC1-46CC-A021-0BEE66558953
---

# Remove-CMSecondarySite

## SYNOPSIS
Removes a secondary site from Configuration Manager.

## SYNTAX

### SearchByValueMandatory (Default)
```
Remove-CMSecondarySite -InputObject <IResultObject> [-Force] -Action <ActionType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchBySiteCodeMandatory
```
Remove-CMSecondarySite -SiteCode <String> [-Force] -Action <ActionType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SearchByNameMandatory
```
Remove-CMSecondarySite -Name <String> [-Force] -Action <ActionType> [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **Remove-CMSecondarySite** cmdlet removes a secondary site from Microsoft System Center Configuration Manager.
A secondary site has no site database of its own.
Instead it is connected to a primary site and sends client data to the primary site for storage.

## EXAMPLES

### Example 1: Remove a secondary site upgrade by using a site name
```
PS C:\>Remove-CMSecondarySite -Action Delete -SiteName "ClientSecSiteUpgrade03"
```

This command deletes a secondary site named ClientSecSiteUpgrade03.
Because the *Force* parameter is not specified, you must confirm the action before it is performed.

## PARAMETERS

### -Action
Specifies an action type for the deletion.
The acceptable values for this parameter are:

- Delete.
Removes the reference to the secondary site from the database.
- Uninstall.
Removes the reference to the secondary site from the database and triggers an uninstall action at the secondary site server.

```yaml
Type: ActionType
Parameter Sets: (All)
Aliases: 
Accepted values: Uninstall, Delete

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
Specifies a secondary site object.
To obtain this object, use the New-CMSecondarySite cmdlet.

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
Specifies the name of a secondary site.

```yaml
Type: String
Parameter Sets: SearchByNameMandatory
Aliases: SiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SiteCode
Specifies a code for a secondary site.

```yaml
Type: String
Parameter Sets: SearchBySiteCodeMandatory
Aliases: 

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

[Invoke-CMSecondarySiteUpgrade](./Invoke-CMSecondarySiteUpgrade.md)

[New-CMSecondarySite](./New-CMSecondarySite.md)


