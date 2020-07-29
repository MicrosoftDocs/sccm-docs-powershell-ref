---
external help file: AdminUI.PS.ClientSettings.dll-Help.xml
Module Name: ConfigurationManager
online version:
schema: 2.0.0
---

# New-CMSoftwareCenterTabItem

## SYNOPSIS

Use this cmdlet to create a custom Software Center tab.

## SYNTAX

```
New-CMSoftwareCenterTabItem -Name <String> -Url <Uri> [-DisableWildcardHandling] [-ForceWildcardHandling]
 [<CommonParameters>]
```

## DESCRIPTION

Starting in version 1906, use this cmdlet to create a custom Software Center tab.

## EXAMPLES

### Example 1: Create a helpdesk tab

This example creates a new Software Center tab named **Helpdesk** that opens the helpdesk website.

```powershell
New-CMSoftwareCenterTabItem -Name "Helpdesk" -Url https://helpdesk.contoso.com
```

## PARAMETERS

### -DisableWildcardHandling

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

### -Name

Specify the name of the custom tab, which displays in the Software Center menu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: CustomTabName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Url

Specify the URL for Software Center to display when a user selects this tab.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: CustomTabUrl

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Object
## NOTES

## RELATED LINKS
