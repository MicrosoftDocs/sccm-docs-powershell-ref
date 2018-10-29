---
external help file: AdminUI.PS.Common.dll-Help.xml
ms.assetid: 1FE8E572-8FBA-48C3-8250-1885951B073D
online version: https://go.microsoft.com/fwlink/?linkid=833880
schema: 2.0.0
---

# ConvertFrom-CMIResultObject

## SYNOPSIS
Converts from an **IResultObject** to a **ManagementBaseObject**.

## SYNTAX

```
ConvertFrom-CMIResultObject -InputObject <IResultObject> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION
The **Convertfrom-CMIResultObject** cmdlet converts from an **IResultObject** to a **ManagementBaseObject**.

## EXAMPLES

### Example 1: Convert an IResultObject to a ManagementBaseObject by getting a site object
```
PS ABC:\> $Site = Get-CMSite -SiteCode PS1
PS ABC:\> ConvertFrom-CMIResultObject -InputObject $Site
```

The first command gets the site object with the code PS1 and stores the object in the $Site variable.

The second command converts the site stored in $Site to a ManagementBaseObject.

### Example 2: Convert an IResultObject to a ManagementBaseObject by getting a site by its code
```
PS ABC:\> ConvertFrom-CMIResultObject -InputObject (Get-CMSite -SiteCode PS2)
```

This command gets the site with the code PS2 and then converts the site to a ManagementBaseObject.

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

### -InputObject
Specifies the **IResultObject** to convert to a **ManagementBaseObject**.

```yaml
Type: IResultObject
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[ConvertTo-CMIResultObject](ConvertTo-CMIResultObject.md)
