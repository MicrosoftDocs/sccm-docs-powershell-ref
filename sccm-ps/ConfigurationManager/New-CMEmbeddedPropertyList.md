---
external help file: AdminUI.PS.Common.dll-Help.xml
ms.assetid: E4BEA20B-43B6-4297-8A2A-AA28CB1841E0
online version: https://go.microsoft.com/fwlink/?linkid=833649
schema: 2.0.0
---

# New-CMEmbeddedPropertyList

## SYNOPSIS
Creates an embedded property list.

## SYNTAX

```
New-CMEmbeddedPropertyList -PropertyListName <String> [-Value <Object[]>] [-DisableWildcardHandling]
 [-ForceWildcardHandling] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRIPTION
The **New-CMEmbeddedPropertyList** cmdlet creates an embedded property list.

## EXAMPLES

> [!NOTE]
> Configuration Manager CmdLets must be run from the Configuration Manager site drive.  For more information see the [getting started documentation](https://docs.microsoft.com/en-us/powershell/sccm/overview).


### Example 1: Create an embedded property list
```
PS ABC:\> New-CMEmbeddedPropertyList -PropertyListName "AD Containers" -Value "LDAP://CN=Computers,DC=Contoso,DC=com","LDAP://OU=testUnit,DC=Contoso,DC=com"
```

This command creates an embedded property list with the name AD Containers, and adds the specified LDAP values.

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

### -PropertyListName
Specifies a name for the property list.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Value
Specifies an array of values for the property list.

```yaml
Type: Object[]
Parameter Sets: (All)
Aliases: Values

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

[New-CMEmbeddedObjectInstance](New-CMEmbeddedObjectInstance.md)

[New-CMEmbeddedProperty](New-CMEmbeddedProperty.md)
